## Work in Progress Annotations


## Annotated
The next demo shows that you can take an existing image and mark it up with annotations. For maths such as this example this has very largely been obsoleted by the JaTeX system, as you can now create LaTeX on the canvas, and then have #Code(jref)s that link to them.

For other kinds of images 'from elsewhere' such as the anatomy illustrations later on this page, the annotated images can be good to have.

You can download images you have annotated in Scorpio to use elsewhere.  Use the 'download' button in the ['details' panel](scorpio_details_panel).  If you just want the annotations as a layer on their own, remove the background image first.

This example has the #Code(option: nodrag) set, so you cannot move the labels around by dragging.

!!Scorpio
# AnnotatedLatex
!!Markdown

Here's another maths example:

## Vis-Viva
!!Scorpio
# AnnotatedLatex2
!!Markdown

## Femur
This example has #Code(option: nodrag) set and has #Code(boxed: 250) which disables the details panel and fixes the box height to 250px.  The info cards and annotation positioning is 'locked in'.

!!Scorpio
##Annotated
caption: Femur
boxed: 250
options: nodrag
:A: Head
*:B: ""
:C: Greater\nTrochanter
*:D: " "
:E: Lesser\nTrochanter
*:F: " "
:G: Condyles
*:H: " "
*:I: " "
:A: at: 48,42
:B: at: 95,62
:C: at: 48,148
:D: at: 120,139
:E: at: 199,17
:F: at: 166,104
:G: at: 526,106
:H: at: 473,137
:I: at: 469,88
background: Gray252.png
:A:B:
card:
##Head
Large ball of the ball and socket joint of the hip
:C:D:
card:
##Greater Trochanter
Muscles that abduct the hip attach here.
:E:F:
card:
##Lesser Trochanter
Muscles that adduct the hip attach here.
:G:H:I:
card:
##Condyles
Smooth surfaces that make the top part of the hings at the knee.  
:info:
card:
##Femur
The illustration of the femur is from the 1918 edition of Gray's anatomy, and is in the public domain. 
!!Markdown

&nbsp;