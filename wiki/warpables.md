# Work in Progress IV

These are some more features I am working on.

## Bugles

#Boat(Old code destined for chronograms/spindle-diagrams, now with 'wood' colours.)

!!Scorpio
# Bugles
!!Markdown
## Brush
#UFO(Warpable tiles). This first example is for the path of a blue paintbrush. The idea is to warp a standard repeating bitmap into the right shape for drawing with.

But braid, or brushstrokes?  Both are the same thing.  They are image warpings using a NURB algorithm.

Dragging the corner points is a bit laggy.

!!Scorpio
# Brush
!!Markdown

## Braid
Warping to a NURB patch, now with a braid pattern instead. This is the same code, just with a different image:

!!Scorpio
# Braid
!!Markdown

### How they Work

The building block for the distortable paths is a NURB patch.  It's cubic in the curvy dimension, linear in the other.  

The texture being fed to the NURB patch is horizontally tilable, and so joins up end to end.  The texture has transparency at the top and bottom edges and so 'can have its own shape' to its edge.

Linear changes to the scale factors in the s,t texture coordinates gives us:
* The option of the stacked repeats (vertical) and with that compression/expansion in that dimension.
* The option of end to end repeats (horizontal) and with stretching/compressing in that direction.  

We stretch texture with the brushstroke to get the flow. 

### #Rock(Warpable Patches in JaTeX?)

Possible future JaTeX option as #Code(\warp)?

The patches work, but I'd like to work some more on how to use them before I make them part of JaTeX. For example I want to be able to place any part of the diagram into a warpable patch.

### #UFO(GL Shaders for speed?)
The main problem with these NURB patches are that they are slow.  Moving the points is laggy. The cause of slow repainting is that the conversion to and from image data in the canvas is slow.  It probably will make sense to reimplement the NURBs as shaders.

* Safari browser on an M1 was way more responsive than Chrome browser on an Intel. Probably the graphics memory on an M1 is better integrated. 
* I have enabled `willReadFrequently` on all canvases. This may help the readback of data a little.

The patches have a lot of mileage in them.  For example for warped text, or for warping any image created by Scorpio.  Other s,t coordinate calculations can give 'bias cut' tiling and semi-repetitive patterns 'along a curve'.  

I plan to hold off on the shader version and see how far I can push the JavaScript canvas version.  For example, doing the texture morphing only as a final end stage, but not whilst dragging points.

