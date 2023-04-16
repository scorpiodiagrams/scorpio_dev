#ScorpioHead(27 February 2022, Scorpio Blocks)
##Blocks
 * #Rock(This is still aspirational.)*

I plan to support a Scratch-like block-based programming interface.  Kids can make interactive games using Scratch.  I don't see why adults shouldn't be able to add interactivity to a diagram by placing click-together blocks. 

The click-together programming style pioneered by Scratch seems well suited to programming animation.  Scratch uses click together blocks for programming.  Scorpio uses click together blocks for the diagrams too.  In Scorpio, structural elements can be clicked together to make larger structures just as larger programs can be built up from smaller ones.  My thinking here is that people can learn how to combine things on the diagrams, without animation or code, and then find that combining peices of code, by clicking them together, works much the same way.

Blocks are not a panacea.  Blocks are good for smaller projects.  With larger projects, tools based on text are needed.  Our tools for working with large and complex programs are much better when the programs are text rather than blocks.  

There seems to be a glass-ceiling with Scratch.  Moving on from Scratch to a textual language like Python seems a much harder transition for the children than you might expect.  

In part this is because the error messages in Python are often inscrutable.  Scratch sidesteps this by very largely avoiding errors at all.  However languages with more features do seem to need to be able to report errors.

##Errors of Omission

I plan to fix this problem by reframing many errors as 'something is missing'.  Many errors are in fact detected by the parser as 'omissions'.  The parser expects to find one thing, and it finds something else instead.

!+[Missing](./images/BlocksMissing.png =300px)

These errors can become prompts for what to do to move on from them.  Potentially too the error reporting and keyword completion are part of the same system.

###Other Wrinkles
There are a number of other wrinkles in this updated style.  The input box is the full height of the block, making the tile more compact.  The stem of the 'if' block has a soft break in it, which allows for inclusion of 'else if' clauses, and in a similar style, case statements with multiple options.

The blocks can be faded out, giving a text based interface in the same space.  Round tripping between text and blocks is fully supported.  For example syntactically incorrect programs laid out with unusual line breaks and indentation can still be presented as unusually shaped and laid out blocks.

Another wrinkle is that blocks can be separated and have a cable connecting them.  You can use this to shift from click-together blocks to shader graphs, and mix the two styles in the same program.

##Blocks in the Diagram

I plan to use blocks in the diagram, e.g. rectangular blocks holding an image or blocks for mathematical symbols with places to attach equations to.  These can be 'clicked together' to lay out the diagram.

The block backgrounds can then be faded out.

##Work in Progress

This diagram below shows how shapes, as used in block based programming, can be built up.  As well as end shapes, we now have edge shapes. This is using style #Code(##CodeTiles).
!!Scorpio
# CodeTiles
!!Markdown

The segmented stems allow for mix and match of #Code(if) and #Code(elseif) and similarly for #Code(switch-case).  They also visually cue the directionality of flow of control.

The I-J-K diagram on the right is for state machines.  No, I don't yet know exactly how I will use that.

The code tiles will lead on to using the same system for large diagrams of biochemistry to show large diagrams of how code works.  Also the code tiles lead on to integrating large diagrams and large text.  When you fade out the tile backgrounds you get a normal textual program with Geshi syntax highlighting, perhaps.

Scorpio does not yet support tile-aware dragging and snapping, so positioning these new shapes so that they exactly line up is painful.  

#Rock(There's a ton of work to do here.  The changes should be beneficial well beyond code tiles.)

I plan for natural dragging of block shapes for a future version of Scorpio.  The snapping and dragging scheme will also improve item positioning in other kinds of diagrams.

#UFO(A full programming system using blocks will, as they say, 'be ready "presently"'.)

## Scene Graph
The same kind of tiles work for a scene graph. This is using style #Code(##SceneGraph).
!!Scorpio
# SceneGraph
!!Markdown

The scene graph style has different colours, and it rounds horizontal sizes up in much the same way that the FlowChart style does - so that boxes tend to have the same sizes.

Here the 'stem-flow' is dataflow rather than flow of control.  I will use different styles of connection for different 'volumes' of data, so that it is clear when high volume raster data is flowing.

The I-J-K-L thing is for shapes that sample from image data and feed it into the data flow.  You can drag it over the image you are working on to capture data from a region.



