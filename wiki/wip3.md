# Work in Progress III

!!Markdown
##Sankey Diagrams

An overlay over a thermal efficiency diagram.  Current #Code(##Sankey) demo shows nothing more than that you can size the nodes in the graph individually and that the connecting tapered lines will then follow suit.  The text is deliberately very faint.  In the complete version there will be some kinds of directives for positioning text relative to the ends of the Sankey branches.  The Sankey branch ends and the leaf labels will not need to coincide.

This kind of Sankey diagram is intended as an overlay over another diagrams, for example illustration of the water cycle, or over a map showing an army's progress, or over a timeline or as an illustrated phylogentic tree, or for a map of delta v to various solar system destinations.  The hand positioning becomes important in those uses.  It's a different use from the more abstract Sankey diagrams that can be found in other diagram software.

#Rock(Still to do, I intend to make it a lot easier to make this kind of diagram by 'drag and drop'.)

!!Scorpio
# Sankey
!!Markdown

## Biochemistry

#Rock(This is work towards a biochemical pathways browser.  The main point of this piece of development is to get subdiagrams working so that you can build complex diagrams out of smaller ones.  )

First some molecules to use later...

!!Scorpio
# Citrate
!!Markdown

!!Scorpio
# Succinate
!!Markdown


###Citric Acid Cycle
Now we have the molecules, the start of the biochemistry pathway diagram proper.  The molecules are included in the diagram.  Whatever you add into the Citrate and Succinate diagrams will appear here.  If you modify, magnify or rotate the molecules on their source diagrams, they will modify, magnify and rotate here.  

You may need to click on the diagram to make it refresh.  That's because this is work in progress... 
!!Scorpio
##Mindmap
caption: Citric Acid Cycle
:A: >Citrate\+/+\
:B: \+/+\cis-Aconitase\+/+\
:C: \+/+\D-Isocitrate)+(
:D: )+(Oxalosuccinate)+(
:E: )+(α-ketoglutarate>
:F: >Succinyl-CoA>
:G: >Succinate>
:H: >Fumarate>
:I: >Malate>
:J: >Oxaloacetate>
:K: Succinate
:L: Citrate
:A: at: 331,36
:B: at: 480,81
:C: at: 529,146
:D: at: 531,225
:E: at: 481,299
:F: at: 296,367
:G: at: 123,302
:H: at: 75,223
:I: at: 83,142
:J: at: 174,81
:K: at: 19,250
subdiagram: Succinate
:L: at: 243,-24
subdiagram: Citrate
link: A B
link: B C
link: C D
link: D E
link: E F
link: F G
link: G H
link: H I
link: I J
link: J A
link: * *
bend: 20
:A:
card:
##Citrate
placeholder with some *markdown* in it.
:B:
card:
##cis-Aconitase
placeholder...
:C:
card:
##D-Isocitrate
placeholder...
:D:
card:
##Oxalosuccinate
placeholder...
:E:
card:
##α-ketoglutarate
placeholder...
:F:
card:
##Succinyl-CoA
placeholder...
:G:
card:
##Succinate
placeholder...
:H:
card:
##Fumarate
placeholder...
:I:
card:
##Malate
placeholder...
:J:
card:
##Oxaloacetate
placeholder...
!!Markdown

