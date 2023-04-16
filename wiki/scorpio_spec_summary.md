#Summary
### for diagram spec
A brief summary of the Scorpio diagram specification.

## Diagram Style

Each diagram has a style, which determines how it is displayed.  For example Scorpio has a #Code(##LineArt) type, which displays in black and white figures.  The most gaudy is #Code(##Rainbow), which has rainbow colours and 3d effect on the labels.  The style is the first line in a diagram spec.

#Example(
* #Code(##Standard) - Colourful and 3d.  Connecting lines are of fixed width. This is also the default.
* #Code(##MindMap) - Colourful and 3d.  Connecting lines vary in width (Sankey style).
* #Code(##Rainbow) - Like MindMap, but even more over the top colourful, with varying colours in the labels too.
* #Code(##SceneGraph) - Sombre black and blue two-tone colour, for that serious project.  Label widths are rounded up, so making more labels the same width as each other.
* #Code(##Geometry) - For trigonometry and drawing 'Euclid's elements'
* #Code(##FlowChart) - Labels are increased in width and height, with size 'rounded up' so that many of the boxes will have similar height/width.  Corners of rectangular boxes are chamfered.
* #Code(##Molecule) - Coloured single-letter circles with element abbreviations in them, and dark grey single and double links.
* #Code(##LineArt) - A black and white style for figure diagrams.
* #Code(##GenericDiagram) - A more colourful version of LineArt.
* #Code(##StarMap) - A style with white lines, useful for star maps.
* #Code(##Annotation) - A style for placing labels on an existing image.  The labels have translucent black backgrounds.
)End#

The names for the diagram styles suggets their uses, but you may find some styles work well outside their designed-for use.

The diagram styles from #Code(##Molecule) onwards use thin connecting lines.  The ones before use shapes that are filled with a colour to connect the labels.  At the moment the later ones are single colour and have fixed line width, but you can have double and triple links.  Meanwhile the ones listed before #Code(##Molecule) have variable colours and have widths that you can vary, but are always single links.

#Button(scorpio_diagram_styles, Diagram Styles) - Styles for Scorpio diagrams, with examples of how they look.

##Objects and names

Objects in Scorpio include

#Example(
* #Code(label) - which has a position
* #Code(link) - which links two labels
* #Code(angle) - which relates three labels
* #Code(quad) - which relates four labels
)End#

Each object has an optional #Code(label:) and an optional #Code(card:).  The #Code(label:) shows as text on the diagram.  The #Code(card:) shows to the left or right of the diagram, when you hover over the object.

In Scorpio labels are given names sequentially, #Code(A), #Code(B), #Code(C)....  then #Code(AA), #Code(AB), #Code(AC)...  and so on.  You don't have to manually give the labels names, Scorpio will do so.  If Scorpio works with a spec file it will add the names in for you.

##End Shapes

You can specify the shape of a label using end shapes

#Example(
* #Code(() and #Code(&#41;) - for round ends
* #Code([) and #Code(]) - for flat ends
* #Code(<) and #Code(>) - for chevron ends
* #Code(\) and #Code(/) - forwards and backwards slopes
)End#

There are some custom end shapes

#Example(
* #Code(:snake_head:) and #Code(:snake_tail:) - stylised snake shapes
* #Code(:arrow_head:) and #Code(:arrow_tail:) - arrow end shapes
* #Code(:cold_front:) and #Code(:warm_front:) - shapes used for meteorology
)End#

There are also some stacked ends

#Example(
* #Code(\+/+\) and #Code(/+\+/) - zigzag and zagzig ends
* #Code((+&#41;) and #Code(&#41;+() - sway and antisway ends
)End#

#Button(scorpio_label_styles, Labels) - End shapes for labels, with examples of how they look.

##Label Modifiers

#Example(
* #Code(:Height4:) - Makes the label '4 lines' high.
* #Code(:Width10:) - Sets the width of the label to 10.
* #Code(:Pad3:) - Expands the label by 3 relative to its minimum size.
)End#

##Line Types

#Example(
* #Code(--) - for a normal single line (this is the default for LineArt)
* #Code(==) - for a double line
* #Code(~~) - for a rippled line
)End#

End shapes work for the ends of lines in much the same way as they do for labels, but they look a bit different.  

* When an end shape is added to an unfilled line, that is, single, double or rippled, the end shape is unfilled too.
* When an end shape is added to a label (or a filled line) the end shape is filled, just like an end shape for a label.  

#Button(scorpio_link_styles,Links) - The styles for the lines, with visual examples.

##Label Text

Sometimes, when Scorpio might get confused about what the actual text of the label is, you will put the text inside quotation marks "", with the end shapes, label modifiers and line type indicators outside the quotes.

There are some special characters:
#Example(
* #Code(\n) - puts a new line in the label.
* #Code(\") - puts a quotation mark in the label, without ending the label.
* #Code(\\) - puts a \ in the label, without treating the next character as special
)End#

##Info Cards

Cards provide additional information on a label, using a large tooltip off to one side of the diagram.  

You can create a card using the #Code(card:) command. The text of the card can be on multiple lines that follow.  You use markdown to specify the text formatting.  For example:
#Example(
* #Code(&ast;&ast;this is in bold&ast;&ast;) - yields "**this is in bold**".
)End#

The markdown used by Scorpio is as follows:

#Example(
At the start of a line:
* #Code(#) big heading
* #Code(##) medium heading
* #Code(###) smaller heading
* #Code(>) put what follows in a quote box
* #Code(<) put what follows in a quote box (from the right)
* #Code(&ast;) bulleted list, single indent
* #Code(&ast;&ast;) bulleted list, second level (and so on) 

Anywhere in the text:
* #Code(&#91;title](https://www.example.com&#41;) a hyperlink
* #Code(&ast;&ast;something&ast;&ast;) put 'something' in bold
* #Code(&ast;something&ast;) put 'something' in italics
* #Code(&dollar;&dollar;latex&dollar;&dollar;) render the LaTeX (uses KaTeX library)
)End#

The text of the card ends with the next #Code(:) containing command.

#Button(scorpio_cards,Info Cards) - Examples of information cards in action.

##Other commands and attributes

Other commands work the same way as #Code(card:).

#Example(
* #Code(at: 400 80) - Sets the position of the current label.
* #Code(bend: 30) - Bends a link 'by 30%'.  Use -30 to bend the other way.
* #Code(cloze: label text) - Temporarily replaces the current label's label with cloze-styled text
* #Code(level: 3) - Changes the level of a label or a link, changing its colour.  To see this on a link needs a filled style like #Code(Rainbow) or #Code(MindMap).
* #Code(size: 3) - Changes the size of the label - only affects links from that label, and needs a style like #Code(Rainbow) or #Code(MindMap).
* #Code(label: label text) - Changes the text of a label.  Rarely used as you would usually set the text you want when defining the label
* #Code(card: some markdown text) - Sets the text of the info card for a label.
* #Code(multiplicity: 3) - Makes a link into a triple link.  Needs a line style such as #Code(LineArt).
)End#

Some of the restrictions as to what combinations work will be #Rock(fixed in the future.  For example, in the future I may allow #Code(card:) to be applied to links and the labels on the links, and not just to #Code(label)s.  )

##Selectors

To select the link between A and B, use 
#Example(
* #Code(link: A B )
)End#

Anywhere you use a label identifier you can use a wild card '&ast;'.  

#Example(
* #Code(link: A &ast;) - will select all links from A to something.
)End#

Bonds are directional.
#Example(
* #Code(link: A B) - is different to #Code(link: B A).  
)End#

To select multiple labels, write them out with #Code(:) between.  This command selects five chosen labels:
#Example(
* #Code(:A:H:Y:AA:AC: )
)End#
##Global commands
Some commands affect the whole diagram

#Example(
* #Code(magnify: 0.9) - dynamically changes the size of the diagram
* #Code(rotate: 0.1) - dynamically changes the rotation of the diagram
* #Code(:info:) - set the current label to the 'pseudo label' which is the info button in top left corner.  This is only useful for setting the card for the info button.
* #Code(caption: A diagram) - set the caption of the diagram.  This is used below the diagram and also as the title for the edit box.
* #Code(background: blue) - sets a background colour. Many css formats for colour, such as #9a1 for a green, will work.  If you host Scorpio diagrams yourself, you can also use background to set a background image from your site such as Brush.png or Braid.png.
* #Code(boxed: 150) - #Rock(used 'in house' to make the box for the diagram smaller.)
* #Code(object: {...}) - #Rock(used 'in house' to add a 'scene graph object' to the diagram.  This is typically for development work in progress.)
)End#

 #Button(diagram_forge,Diagram Forge) - For making your own diagrams in Scorpio format