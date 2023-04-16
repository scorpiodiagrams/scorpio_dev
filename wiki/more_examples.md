## More Examples

This page has more examples you can look at and modify.  It's an extended version of the [Diagram Forge](diagram_forge).  Once again the diagrams shown on this page are editable.  Click on any label and drag it around to move it.  The edit box will appear.  You can then edit the text.

All the diagrams on this page are similar in kind.  They all show 'things connected to other things'.  

## Mind Maps

A mind map.  For a less gaudy look, try changing it to use #Code(##Geoemtry).  For a more eye popping look, use #Code(##Rainbow)

!!Scorpio
# Characters
!!Markdown

## Annotating an Image

Here's an #Code(##Annotated) image.  You can get just the annotations on their own by removing the background image.

!!Scorpio
# CellWallRevision
!!Markdown

## Geometry
!!Scorpio
##Geometry
caption: Subdividing a triangle
*:A: (A)
*:B: (B)
*:C: (C)
*:D: (D)
:A: at: 83,300
:B: at: 200,100
:C: at: 570,300
:D: at: 200,300
link: A B
link: B C
link: C A
link: B D
angle: C A B
angle: D B C
angle: C D B
:info:
card:
<h3>Trig</h3>We can use LaTeX such as $$\cos^2\theta$$ in the info card.
!!Markdown
The styling above is for geometry, such as in trigonometry.

## Molecules
!!Scorpio
# Melatonin
!!Markdown
Here the styling is as a molecule.  In the future Scorpio will allow for molecules on a large biochemistry diagram.  Scorpio already uses part of the SMILES standard to specify these molecular structures.
#Right([SMILES](smiles))

## Flow Charts
!!Scorpio
# FlowChart2
!!Markdown
This styling is suitable for flow charts.

## Consultancy Diagrams

This diagram is using the Scorpio shapes, without showing the connection between them.  This diagram is using the #Code(/) and #Code(\) end shapes for all the labels.

!!Scorpio
# Maslow
!!Markdown
Additional information about each label in the diagram is given in the info cards.

## Star Maps

This diagram uses a colour for the background rather than an image.  It's using #Code(##StarMap) style, which has white lines.
!!Scorpio
# Orion
!!Markdown

For learning which star is which, open the details panel and then on the 'hotspots' list, hover over the different boxed colours to pick out the corresponding star.

## Generic Diagrams
!!Scorpio
##GenericDiagram
caption: Tours around two shapes
:A: ("A")
:B: [" B "]
:C: <"C">
:D: /" D "/
:E: E
:F: F
:G: G
:A: at: 80,300
card:
<h2>("A")</h2> placeholder...
:B: at: 80,100
card:
<h2>[" B "]</h2> placeholder...
:C: at: 400,100
card:
<h2><"C"></h2> placeholder...
:D: at: 400,300
card:
<h2>/" D "/</h2> placeholder...
:E: at: 500,150
:F: at: 640,150
:G: at: 570,250
link: * *
bend: 0
link: A B --from A to B-->
link: B C ~~<from B to C>~~>
link: C D ==from C to D-->
link: D A [~~<from D to A>~~>>>
link: E F ~~>
bend: 50
link: F G ~~>
bend: 50
link: G E ~~>
bend: 50
!!Markdown

This diagram supports styled lines with additional text on them. 
