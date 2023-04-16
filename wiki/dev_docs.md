## More Documentation
~~~Polyglot

### Mini Graphs
The `\graph` command, also `\half-graph` and `\quarter-graph` for narrower versions, draws small graphs. You specify y values for x=0 and x=1 and also slopes after the command. You can string a number of these together to make a longer graph. The slopes are usually given using `/`, `\ ` and `=` for +1, -1 and 0 slopes. For example `\graph 1\1/` is 1 at 0 and 1, dips down then rises. 

> [!info]- Extended Syntax for \graph
You can instead use a slightly different syntax and separate the various components with a `:`. With that syntax you can use numbers for the slopes rather than the symbols. That's the way to get slopes other than +1, -1 and 0. `\graph 0.5:0.1:0.5:-0.1` is a graph at height 0.5 with a very slight rise in the middle.

The `\graph` command can give many more points on the curve. `\graph 0.5/0.5\0.5/0.5\0.5/0.5\0.5/0.5\` is an undulating graph at an average value of 0.5.
)

> [!info]- \UFO Future plans for \graph
> There's a much extended syntax in the works that gives more what you'd expect from a plotting library. It's not high priority because there are already good tools for doing graphs.)

The mini graphs are for very quick illustrations, such as ReLU, a cumulative distribution, Hermite polynomials in blending, illustration of square wave, triangular wave, sine wave, and so on.

~~~Scorpio
##Annotated
caption: Using \graph
bounding_boxes: 
:A: $$ \graph 1=0.5/ \ \graph 0.5/0.7/ \ \graph 0.7/1\
:B: $$ \half-graph 1\0/ \ \half-graph 1=0/ \ \half-graph 1/0/ \ \half-graph 1\0= \ \half-graph 1=0= \ \half-graph 1/0= \ \half-graph 1\0\ \ \half-graph 1=0\ \ \half-graph 1/0\
:C: $$ \half-graph 1\1/ \ \half-graph 1=1/ \ \half-graph 1/1/ \ \half-graph 1\1= \ \half-graph 1=1= \ \half-graph 1/1= \ \half-graph 1\1\ \ \half-graph 1=1\ \ \half-graph 1/1\
:D: $$ \graph 0/1/ \\ + \\ \graph 0=0\ \\ = \\ \graph 0/1=
:E: $$ x \\ + \ - x\sup 3 + x\sup 2 \ = \  - x \sup 3 + x \sup 2 + x
:F: $$ \kbd { several \ graphs \ in  \ a \ sequence }
:G: $$ \kbd { \slash graph \ 0/1= }
:H: Starts at 0
*:I: (0 )
*:J: ( )
:K: Slope is \nupwards
*:L: ( / )
:M: Ends at 1
*:N: ( 1 )
*:O: ( )
:P: Slope is \nhorizontal
*:Q: (= )
:R: $$ \kbd {Various \ graphs \ using \ \slash half-graph}
:S: $$ \graph 0/1=
:A: at: 66,22
:B: at: 326,166
:C: at: 325,255
:D: at: 351,21
:E: at: 410,95
:F: at: 44,105
:G: at: 19,147
:H: at: 44,267
:I: at: 80,180
:J: at: 123,386
:K: at: 116,307
:L: at: 95,180
:M: at: 155,246
:N: at: 110,180
:O: at: 191,318
:P: at: 235,261
:Q: at: 125,180
:R: at: 354,347
:S: at: 120,317
link: K J
link: P O
~~~Polyglot

### Twisty
The JaTeX command `\twisty` was originally designed just for Penrose notation. It shows how the order of items, indices for a tensor, is to change between its top and bottom edge. It can also draw the flat and squiggly lines needed to show symmetrisation and antisymmetrisation of tensors.

Originally `\twisty` was for two edges `\twisty top-bottom`, and you could specify the index order for the top, or the bottom, or both. However, it was natural to also offer connections between left and right edges. `\twisty top-bottom-left-right`. `\twisty` now gives us a general purpose tile for connecting things up. It can be used for electronics diagrams and some other things that involve connections.

Another extension to `twisty` is the option to use a `.` for an absent connection. This is mostly intended for wiring diagrams of various kinds. It can also be used to make a tile wider, or between indices to make the spacing between index lines wider.

~~~Scorpio
# Electro2
~~~Polyglot

### Grids
These are common in data science diagrams. `\grid` is followed by a sequence of letters such as `rgb,www`, which is specifying two rows, the first row with red, green and blue boxes and the second with three white boxes. 

A #UFO(future extension) will allow you to set your own custom letters. There's also a planned a custom version for chess.

~~~Scorpio
##Annotated
caption: Using \grid
:A: $$ \kbd { \slash grid \ rgbwrgbMNOP,bwrgbwrgOMNP,gbwrgbwrNOMP }
:B: $$\kbd{ \stack { { r \\grid r  - Red \ square\\\\\ } { g \\grid g - Green \ square \\\} { b \\grid b - Blue \ square\\\\ } { w \\grid w - White \ square \\\} { M \grid M - Red \ circle \\\} { N \grid N - Green \ circle \} { O \grid O - Blue \ circle \\}{P \grid P - White \ circle\}{ , \\\ - Start\ a\ new\ row} } }
:C: $$ \grid rgbwrgbwMNOP,gbwrgbwrOMNP,bwrgbwrgNOMP
:D: $$ \kbd{ \slash grid \ www,wwww,wgwgw,wwwwww}
:E: $$ \grid www,wwww,wgwgw,wwwwww
:A: at: 39,47
:B: at: 382,142
:C: at: 89,75
:D: at: 38,179
:E: at: 112,203
~~~Polyglot

### Repetition
`\mul` repeats the next thing up to 20 times.
~~~Scorpio
##Annotated
caption: Using \mul
bounding_boxes: 
:A: $$ \stack { \stack  \mul 7 { \grid g,g \\mul 9 {\grid gg,O \} \grid g,g} {\grid g \ \mul 9 {\grid gg \} \grid g}
:B: $$ \mul 6 {\forward  \ \forward}
:C: $$ \mul 6 {\round-flip \ \round}
:D: $$ \mul 6 {\chevron-flip  \ \chevron}
:E: $$ \mul 6 {\forward-flip  \ \forward-flip}
:F: $$ \mul 6 {\round \ \round-flip}
:G: $$ \mul 6 {\chevron  \ \chevron-flip}
:H: $$ \mul 6 {\straight \ \straight}
:I: $$ \kbd { \slash mul \ 6 {\ \left-brace \ \slash chevron-flip \ \slash \ \slash chevron \ \right-brace }
*:J: ( )
:A: at: 3,48
:B: at: 427,10
:C: at: 422,48
:D: at: 421,87
:E: at: 543,13
:F: at: 544,50
:G: at: 542,88
:H: at: 490,121
:I: at: 363,175
:J: at: 462,96
~~~Polyglot

### Transforms
These commands: `\flip`, `\fliph`, `\flipv`, `\flipminor`, `\rot90`, `\rot180`, `\rot270` and `\identity` will change the orientation of the next item - and for the flips there is a mirroring.
~~~Scorpio
##MindMap
caption: Using \flip
bounding_boxes: 
:A: $$\identity IDENTITY -\rot90 ROT90 - \rot180 ROT180 - \rot270 ROT270
:B: $$\fliph FLIPH - \flip FLIP - \flipv FLIPV - \flipminor FLIPMINOR
:A: at: 93,46
:B: at: 93,140
~~~Polyglot

### Rulers
`\ruler` is a widget that can be zoomed continuously. Well, it \Boat could be. I need to restore that functionality. Here is how it looks.

!!Scorpio
##Annotated
caption: Using \ruler
bounding_boxes: 
:A: $$\rot90 \ruler
:B: $$ \ruler
:A: at: 76,67
:B: at: 96,44
~~~Markdown


 #Button(index,Index) - Index