# Work in Progress II

!!Markdown
###Bonus: Horizontal Stacking
####for use with [line styles](scorpio_link_styles)<br><br>
#UFO(I am working on a system for 'arithmetic' with end shapes.  I'm still working on the ideas of how it will work.)

The end shapes for the [line styles](scorpio_link_styles) stack horizontally.  This is mainly useful for feathers on the arrows, or 'doubling' an end to match a doubled line.  
####decorative effects
You can create some decorative effects using the stacking.  The decorative effects are more for recreational than practical use.  I plan in time to support a wider range of useful shapes of all kinds, a larger shape library.  When these are available I will also overhaul the horizontal stacking.
####feathers
!!Raw
>>>--Arrow with 3x feathers and blunt end--]]
!!Scorpio
##GenericDiagram
:A: >>>--Arrow with 3x feathers and blunt end--]]
boxed: plain
:A: at: 200,27
!!Markdown
####dots
The next example shows an additional end shape #Code(.), which can also be obtained using #Code(:dot:).  I provided it mostly for use with horizontal stacking.
!!Raw
<.....>--Dots!--].].].].]
!!Scorpio
##GenericDiagram
:A: <.....>--Dots!--].].].].]
boxed: plain
:A: at: 200,27
!!Markdown
####overprinting
The next example is a bit ridiculous and of no practical use.  I'm using vertical and horizontal stacking and overprinting of rather a lot of end shapes, and two of the special end shapes for snakes.
!!Raw
:A: A
:B: B
:A: at: 100,27
:B: at: 300,27
boxed: plain
link: A B ()+()+()+()+()+()[[[[[[~~:snake_tail:" Larking About ":snake_head:~~]]]]]]((+)(+)(+)(+))
multiplicity: 3
!!Scorpio
##GenericDiagram
:A: A
:B: B
:A: at: 100,27
:B: at: 300,27
boxed: plain
link: A B ()+()+()+()+()+()[[[[[[~~:snake_tail:" Larking About ":snake_head:~~]]]]]]((+)(+)(+)(+))
multiplicity: 3
!!Markdown

##Styling Directives

The following styling #NUTC(directives) aren't available yet.  They can for now only be set by choosing the [diagram type](scorpio_diagram_types)
#[
<pre class='raw'>

:Flat: - Lose the 3D edge.
:NoBorder: - Lose the border entirely.
:NoFill: - Lose the background fill colour entirely.
:FontSize14: - Set the font size to 14 (or some other number)
</pre>
#]

##Any-Shaped Ends

Scorpio uses #NUTC(SVG paths) for the shape of the ends.

SVG paths for ends will look something like "L 20 20 L 80 20".  They are additional steps on a path that starts at 0,0 and ends at 100,0.  
#[
Currently you can only add new paths for end shapes by hacking the source code.  That will change "when I get a round tuit".
#]

