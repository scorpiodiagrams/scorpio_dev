!!Polyglot
# Data Islands
```json
{ "func": "quick_plot", 
  "data":
[
["step", "action", "stage state", "total state", "total params", "total FLOPs"],
[1, "Init", 150528, 150528, 0, 0],
[2, "Conv", 279936, 430464, 11616, 67744512],
[3, "ReLu", 279936, 710400, 11616, 68024448],
[4, "Pool", 64896, 775296, 11616, 68608512],
[5, "Conv", 173056, 948352, 18016, 77261312],
[6, "ReLu", 173056, 1121408, 18016, 77434368],
[7, "Pool", 36864, 1158272, 18016, 77766144],
[8, "Conv", 55296, 1213568, 21472, 78761472],
[9, "ReLu", 55296, 1268864, 21472, 78816768],
[10, "Conv", 55296, 1324160, 24928, 79812096],
[11, "ReLu", 55296, 1379456, 24928, 79867392],
[12, "Conv", 36864, 1416320, 27232, 80530944],
[13, "ReLu", 36864, 1453184, 27232, 80567808],
[14, "Pool", 6400, 1459584, 27232, 80625408],
[15, "Full", 4096, 1463680, 26241632, 133054208],
[16, "ReLu", 4096, 1467776, 26241632, 133058304],
[17, "Full", 4096, 1471872, 43018848, 166612736],
[18, "ReLu", 4096, 1475968, 43018848, 166616832],
[19, "Full", 1000, 1476968, 47114848, 174808832]
]
}
```

#Caption These figures are based on a RT 7900 XTX, which does 61 TFLOPs, has 24GB of VRAM, talks PCIe 4 at 30 GB/s, and can fill its VRAM in 800 ms.

The rows are progressing through stages in the pipeline. The numbers are times for compute or data transfer. 'Stage State' is just for the state variables after that stage. 'Total State' includes all state variables up to that point. 'Total params' is all parameters/weights up to that stage. FLOPs is calculation time. The FLOP times and data transfer times assume f32 parameters and calculations done in f32.


* Time to set up for one image is 6.28 ms for the parameters plus 0.04 ms for the image input to stage 1. 6.32 ms total.
* 800 ms of data fit in the card. Even storing the full state we use only 6.282 ms plus 0.197 ms = 6.479 ms. Lots of room for more instances of data or more parameters (bigger model)
* FLOP time is close to the parameter loading time. We can do two inferences in the time for each loading of params.

The RTX 7900 XTX is massively overpowered for this model. Entire 188MB model can fit 127 times in one 24GB card.

If the model were 200x bigger, then we'd need 573 ms of FLOP time, and 1256 ms to load the model. But... we'd only have 800ms of model space. We could split the model after the stage 16 ReLU, which is 700ms of parameters. The stage state would be 0.109 ms, so we could have about 900 instances in flight at ReLU stage 16, load in the remaining parameters and run those to completion.  

That would be 515 seconds of compute, 1.25s of parameter loading and 3.6s of image loading. 99% of the time is for compute.

Reducing everything to ms makes it easy to see whether it is cheaper to recompute or to store.

For example, doing training, we need double the space for total parameters, as we need a copy to update for gradients. So we split 15, as 15a and 15b, each with half the fully connected weights. But, naively, we also need space for total state, so that we can back propagate the gradients. Similarly we must split 17 into 17a and 17b.

If we store up to the end of 5-Conv, it costs us 25ms &times; 2 to save and reload that state, which is cheaper than the 253ms for recomputing. We can then regenerate to end of 14-Pool at a cost of 11ms, cheaper than the 28 to save and reload that additional state.

From 14-Pool onwards, we're able to get the 99% compute behaviour, and we can have 900 instances in flight. 900 samples should cost 1030s of compute in total, allowing for back-prop cost. The backprop could cost us an additional 900 &times; 264ms = 237s, if recomputing, or 70s if reloading. The combi-strategy though costs 900 &times; 61ms = 55s. A total of 1085s, 2.1x the cost of inference. 

## Data Island API
Data islands provide data to plotting and drawing functions. They are usually used for tabular data.

Currently the header has a 'func' field which says which data island function to call to format the data. 

