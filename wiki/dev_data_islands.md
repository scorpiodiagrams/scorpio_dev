!!Polyglot
# Data Islands
```json
{ "func": "quick_plot", 
  "data":
[
["step", "action", "data", "totalData", "params", "flops"],
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
## Data Island API
Data islands provide data to plotting and drawing functions. They are usually used for tabular data.

Currently the header has a 'func' field which says which data island function to call to format the data. 

