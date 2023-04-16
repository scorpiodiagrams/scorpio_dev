##Connections
###Things Connected to Things

Scorpio is well suited for diagrams of 'things connected to things'. In these 'things connected to things' diagrams you can drag the things about and they stay connected.

A range of shapes for the things and for their connections gives a lot of flexibility in what Scorpio diagrams can show.  You can use the 'connections diagrams' for:

* Mind maps
* Flowcharts
* Annotations to diagrams
* Chemical structures

A text specification tells Scorpio what is connected to what, how to position things and how they are styled.

### Mind Maps
Many layouts have a hierarchical tree like structure.  You can specify a tree structure by listing the items.  Here's an example of a list that has different foods grouped together to make a hierarchy.
!!Raw
* Foods
** High Fat
*** Pizza
*** Burger
** High Carb
*** Potatoes
*** Rice
*** Bread
** High Sugar
*** Toffee
*** Honey
*** Chocolate
!!Markdown
Here's that list presented as a tree-like diagram.  This diagram is specified by the list above.  The list specifies the items and their connections. You then drag the items into position.  
!!Scorpio
##MindMap
caption: Essential food groups 😄
*:A: Foods
**:B: High Fat
***:C: Pizza
***:D: Burger
**:E: High Carb
***:F: Potatoes
***:G: Rice
***:H: Bread
**:I: High Sugar
***:J: Toffee
***:K: Honey
***:L: Chocolate
:A: at: 342,72
:B: at: 240,164
:C: at: 176,108
:D: at: 218,257
:E: at: 436,251
:F: at: 470,333
:G: at: 542,310
:H: at: 404,312
:I: at: 478,140
:J: at: 530,201
:K: at: 602,129
:L: at: 498,64
link: * *
bend: 30
!!Polyglot

> [!info]- Try it Out
## Positioning the Items
Drag the labels into new positions.  

Notice that the text updates to show the new position information.  The positions are the lines with 'at' and then coordinates in them.  If you delete those 'at' lines from the text, Scorpio will make a guess as to where to place the items.
```Raw
**Link to previous diagram!**
*:A: Foods
**:B: High Fat
***:C: Pizza
***:D: Burger
**:E: High Carb
***:F: Potatoes
***:G: Rice
***:H: Bread
**:I: High Sugar
***:J: Toffee
***:K: Honey
***:L: Chocolate
:A: at: 342,72
:B: at: 240,164
:C: at: 176,108
:D: at: 218,257
:E: at: 436,251
:F: at: 470,333
:G: at: 542,310
:H: at: 404,312
:I: at: 478,140
:J: at: 530,201
:K: at: 602,129
:L: at: 498,64
```)
> [!info]- Adding a Link
You can add in additional links, using the #Code(link:) command.

###Add more links
Add a link between #Code(D) (burger#) and #Code(H) (bread#) like so:
```Raw
**Link to previous diagram!**
link: D H
```
You should place this at the end of the spec.  You can place it earlier, so long as the labels #Code(D) and #Code(H) have already been defined.  Scorpio though will rearrange the spec as soon as you move any of the labels. )

### Flow Charts

### Annotated Diagrams

### Chemical Structures

> For chemistry, Scorpio has the beginnings of support for SMILES, a standard concise method for specifying chemical structure.  SMILES is a shorter way for specifying molecules.
#Right([SMILES](dev_smiles))

In the diagram below, each label and each link is specified in the Scorpio spec.  The Scorpio spec is more longwinded than the SMILES spec, but can handle a wider range of 'things connected to things' diagrams.
!!Scorpio
##Molecule
compound: CC(=O)NCCC1=CNC2=C1C=C(OC)C=C2
caption: Melatonin
:A: at: 121,117
:B: at: 168,116
:C: at: 181,163
:D: at: 190,70
:E: at: 238,60
:F: at: 283,73
:G: at: 289,121
:H: at: 253,153
:I: at: 275,201
:J: at: 324,186
:K: at: 324,140
:L: at: 360,118
:M: at: 400,144
:N: at: 435,117
:O: at: 474,146
:P: at: 399,183
:Q: at: 365,209
boxed: 250
!!Markdown
&nbsp;