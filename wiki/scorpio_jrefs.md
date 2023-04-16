# JRefs
## To Reference parts of a JaTeX Formula...
The JaTeX formula is written as normal for JaTeX. The spec below additional has two #Code(jrefs). These state the part of the formula to refer to, and name it with a letter, #Code(D) and #Code(E) in this case. The letter can then be used just like the name of a label, so it can be used ot specify the end point of a #Code(link:).
!!Raw
$$\nabla \times \mathbf{F} = \frac{i}{c}\left( \frac{\partial \mathbf{F}}{\partial t} + H_2 O + 4\pi\mathbf{J} \right) \\\ \in \ \mathbb{Z\supsub 0 1}
jref:D: {F}
jref:E: \nabla \times
!!Scorpio
##Annotated
caption: Equation with JRefs
boxed: 120
:A: $$\nabla \times \mathbf{F} = \frac{i}{c}\left( \frac{\partial \mathbf{F}}{\partial t} + H_2 O + 4\pi\mathbf{J} \right) \\\ \in \ \mathbb{Z\supsub 0 1}
:B: Electromagnetic Field
:C: Curl
:A: at: 48,62
jref:D: {F}
jref:E: \nabla \times
:B: at: 234,34
:C: at: 81,45
link: B D ---->
link: C E ---->>>
:B:D:
card:
## Field F
This is complex valued and has the electric and magnetic components.
:C:E:
card:
## Curl
This measures the rotational part of the field
!!Markdown
In this example #Code(D) and #Code(E) are also given #Code(card:) commands that reference the #Code(jref:) hotspots in the equation.

The #Code(jref:)s find exact string matches in the JaTeX specification, and assign the letter to whatever part of the formula that part produces.

I've chosen to use the same card for the label and the part of the equation pointed to, but that is just a choice. #Code(D) and #Code(E) could be given their own cards with different text. The label pointing to them is optional too. They can have a card without being pointed to.

## JaTeX Playground
Here are some example JaTeX formulae to try out. This larger canvas has the #Code(Details) button, which can be used for debugging to see the hotspots and their colour coding.
!!Scorpio
# JatexPlayground
!!Markdown

## Penrose Notation
Here are some equations in Penrose Notation.
!!Scorpio
# PenroseNotation
!!Markdown
&nbsp;
