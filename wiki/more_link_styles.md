##More Link Styles

The default #Code(##MindMap) [diagram style](scorpio_diagram_styles) has colourful lines that vary in width.  A link between labels A and B could look like this:
!!Scorpio
##MindMap
*:A: A
**:B: B
boxed: plain
:A: at: 100,27
:B: at: 300,27
!!Markdown


###Change the appearance
These links can be styled.  Here is how to style the link as a curved snake with text on it:
!!Raw
link: A B :snake_tail:-->"I am a snake!">--:snake_head:
bend: 15
!!Scorpio
##Sankey
boxed: 200
caption: Example
*:A: A
**:B: B
:A: at: 82,157
:B: at: 422,83
link: A B :snake_tail:-->"I am a snake!">--:snake_head:
bend: 15
!!Markdown
All the usual end shapes work for the ends of the link.  

The problem with #Code(##MindMap) is that ends like #Code(:chevron:) and #Code(:straight:), or their short equivalents #Code(>) and #Code([), will usually be obscured by a label.

In this example I'm using the still experimental #Code(##Sankey) style which has labels that almost vanish, so that you can see the end shapes.

###Hiding labels
An alternative to #Code(##Sankey)'s near invisible labels is to use the #Code(hide:) command to hide labels.  Here's an arrow, done with #Code(##MindMap) style and hiding both of the labels.

!!Raw
link: A B >=-->"An arrow">--=>
bend: 15
:A:B:
hide:
!!Scorpio
##MindMap
boxed: 200
caption: Example
**:A: A
***:B: B
:A: at: 82,157
:B: at: 422,83
link: A B >=-->"An arrow">--=>
bend: 15
:A:B:
hide:
!!Markdown

###Sizing labels

Size and colour can be changed using the #Code(size:) command and the #Code(level:) command applied to the labels.

!!Raw
:A: A
:B: B
:A: at: 82,157
size: 5
hide:
level: 5
:B: at: 422,83
size: 20
hide:
level: 3
link: A B >=-->"An arrow">--=>
bend: 15
!!Scorpio
##MindMap
boxed: 200
caption: Example
:A: A
:B: B
:A: at: 82,157
size: 5
hide:
level: 5
:B: at: 422,83
size: 20
hide:
level: 3
link: A B >=-->"An arrow">--=>
bend: 15
!!Markdown

###Doubled and Squiggly lines

The squiggly line style and the doubled (trebled and higher multiplicity) lines only work with the narrow lines currently.  Also the wide Sankey lines can only accept one end shape at each end, whereas the narrow lines can have multiple arrow heads and arrow tails.

* #Button(scorpio_link_styles,Squiggly Lines) - Styling for the narrow lines
* #Button(scorpio_spec_summary,Summary) - Summary of commands