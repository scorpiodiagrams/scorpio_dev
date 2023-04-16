## JaTeX Formulae

JaTeX is a playful variation on ideas from the maths typesetting language, LaTeX. JaTeX supports a LaTeX like syntax with some interactive extensions and features that are not standard in LaTeX. 

To use JaTeX format for a label, start the label with #Code($$).
Here is a made up formula that mixes some chemistry in with the maths.
!!Raw
$$\nabla \times \mathbf{F} = \frac{i}{c}\left( \frac{\partial \mathbf{F}}{\partial t} + H\sub 2 O + 4\pi\mathbf{J} \right) \in \mathbb{Z\supsub 0 1}
!!Scorpio
##TheStandardStyle
$$\nabla \times \mathbf{F} = \frac{i}{c}\left( \frac{\partial \mathbf{F}}{\partial t} + H\sub 2 O + 4\pi\mathbf{J} \right) \\ \in \ \mathbb{Z\supsub 0 1}
boxed: 80
:A: at: 60,15
!!Markdown
## Principal Differences to LaTeX

JaTeX is nothing like as complete and comprehesive as LaTeX. Think of it more as a place where I'm experimenting with variations on LaTeX. 

JaTeX does not maintain LaTeX's layout rules. You will get different layout from JaTeX and LaTeX. JaTeX can't be used for print documents. 

Some of the differences between JaTeX and LaTeX that matter the most: 
#Example(
* #Code(^) and #Code(_) aren't quite working yet: 
** If you need both on the same symbol, you should use JaTeX's #Code(\supsub) instead. 
** JaTeX's subscripts and superscripts with #Code(\sum) places limits alongside the sum, rather than above and below.
* Currently the rather messy #Code(\) is used to add a small space. Unfortunately it is needed too much - as a workaround for when the spacing JaTeX makes is too tight.
* Many symbols are not yet supported
* No support for matrices
* No support for #Code(&) for alignment
)End#
!!Polyglot

> [!info]- \UFO Plans for LaTeX with JaTeX

* Some time I will improve on JaTeX for print, but it is not an urgent focus of development work, since LaTeX and its tools already covers print well. JaTeX is meant for web use.
* JaTeX has many small extensions relative to LaTeX, and many omissions. The extensions could be ported form JaTeX to LaTeX. The extensions such as `\twisty` and `\tensor-sensor` would then be handled as tikz LaTeX macros.
!!Markdown

## More Symbols

You can use emoji in the JaTeX and there are also some bonus symbols. These will vary from platform to platform.
#Example(
* #Code(\poison \radioactive \biohazard \dna \chemequal) - additional symbols
* #Code(\rook \knight \bishop \queen \king \pawn) - additional symbols
* #Code(\rookw \knightw \bishopw \queenw \kingw \pawnw) - additional symbols
)End#
!!Raw
$$\radioactive + \dna \chemequal \mathbig \biohazard
!!Scorpio
##TheStandardStyle
$$\radioactive + \dna \chemequal \mathbig \biohazard
boxed: 60
:A: at: 60,15
!!Markdown
These additional symbols are 'drawn' rather than coming from a font, so they will be the same on all platforms.
#Example(
* #Code(\transistor), #Code(\resistor) and #Code(\capacitor) - for electrical symbols.
)End#
!!Raw
$$\resistor + \capacitor + \transistor
!!Scorpio
##TheStandardStyle
$$\resistor + \capacitor + \transistor
boxed: 65
:A: at: 60,15
!!Markdown


## End Shapes
The label end-shapes from Scorpio work within JaTeX, with almost no changes. The end shapes are given first, and there is an optional colour argument.
!!Raw
$$\tile ( ( round \\ \tile #252 < < chevron \\\\\\ \tile snake-tail arrow-head {snake \ arrow}
!!Scorpio
##TheStandardStyle
$$\tile ( ( round \\\\\\ \tile #252 < < chevron \\\\\\\\\ \tile snake_tail arrow_head {snake \ arrow}
boxed: 50
:A: at: 60,15
!!Markdown
#Example(
* #Code(\round) and #Code(\round-flip) - for round ends.
* #Code(\chevron) and #Code(\chevron-flip) - for chevron ends.
* #Code(\straight) and #Code(\straight-flip) - for straight ends.
* #Code(\forward) and #Code(\forward-flip) - for forward ends.
* #Code(\backward) and #Code(\backward-flip) - for backward ends.
* #Code(\arrow-head) and #Code(\arrow-head-flip) - for arrow-head ends.
* #Code(\arrow-tail) and #Code(\arrow-tail-flip) - for arrow-tail ends.
* #Code(\snake-head) and #Code(\snake-head-flip) - for snake-head ends.
* #Code(\snake-tail) and #Code(\snake-tail-flip) - for snake-tail ends.
* #Code(\cold-front) and #Code(\cold-front-flip) - for cold-front ends.
* #Code(\warm-front) and #Code(\warm-front-flip) - for warm-front ends.
* #Code(\zigzag) and #Code(\zigzag-flip) - for zigzag ends.
* #Code(\zagzig) and #Code(\zagzig-flip) - for zagzig ends.
* #Code(\sway) and #Code(\sway-flip) - for sway ends.
* #Code(\antisway) and #Code(\antisway-flip) - for antisway ends.
* #Code(\round #ccc) - use a 3 digit hex number to set the color
)End#

## Permutations
The #Code(\twisty) notation can be used to show permutations graphically.
!!Raw
$$\twisty ijk \twisty jki \twisty kij \twisty kji \twisty jik \twisty ikj
!!Scorpio
##TheStandardStyle
boxed: 50
$$\twisty ijk \twisty jki \twisty kij \twisty kji \twisty jik \twisty ikj
:A: at: 60,15
!!Markdown
The #Code(twisty) has a more extended syntax which allows for specifying the top and bottom row, e.g. #Code(\twisty ijlk-kilj). In this format you can place a #Code(.) (or a letter not used on the other row) to leave a gap. Use #Code(\twisty -kilj) for a contravariant tensor. This will give you the opposite permutation to #Code(\twisty kilj).
!!Raw
$$\twisty i.jk-ij.k \twisty lkij-kijl \ \ \twisty ikj-jpi
!!Scorpio
##TheStandardStyle
boxed: 50
$$\twisty i.jk-ij.k \ \ \twisty lkij-kijl \ \ \twisty ikj-jpi
:A: at: 60,15
!!Markdown
You can also add symmetrising and anti-symmetrising bars using the #Code([]) and #Code((#CloseBrace) notation. A #Code(\twisty -i[jk]l) will put the bar across the #Code(j) and #Code(k) and at the bottom.
!!Raw
$$\twisty k[ji] \ \ \twisty -j[ik]
!!Scorpio
##TheStandardStyle
boxed: 50
$$\twisty k[ji] \ \ \twisty -j[ik]
:A: at: 60,15
!!Markdown
#Rock(The plan is to use the twisty notation in Penrose tensor diagrams.)
## More codes
!!Markdown
#Example(
* #Code(\flip) and #Code(\rot90) - for transforming the next part of the diagram.
* #Code(\ruler) - for a ruler
* #Code(\graph) - for a mini-graph of a function.
* #Code(\minWidth) and #Code(\minHeight) - various parameters that can be set.
* #Code(\macro) - a short form for a longer sequence
* #Code(\tiny) - for a very small font.
* #Code(\stack), #Code(\hstack), #Code(\frac) - various stackings. JaTeX starts off in #Code(\hstack) mode, which is making a horizontal stack.
)End#

