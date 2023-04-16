#More Label Styles

##Bonus: Vertical Stacking

Some end types can be added together to stack vertically.  

These examples are special built in patterns rather like the :snake_head: pattern. #UFO(I plan in time to make the end-type stacking general.)

In the examples below, stacking has been used to make "zig zag" ends and "sway" ends that curve back and forth. 
!!Raw
\+/+\zigzag ends\+/+\
!!Scorpio
##TheStandardStyle
:A: \+/+\zigzag ends\+/+\
boxed: plain
:A: at: 150,27
!!Raw
/+\+/zagzig ends/+\+/
!!Scorpio
##TheStandardStyle
:A: /+\+/zagzig ends/+\+/
boxed: plain
:A: at: 150,27
!!Raw
)+(sway ends)+(
!!Scorpio
##TheStandardStyle
:A: )+(sway ends)+(
boxed: plain
:A: at: 150,27
!!Raw
(+)antisway ends(+)
!!Scorpio
##TheStandardStyle
:A: (+)antisway ends(+)
boxed: plain
:A: at: 150,27
!!Markdown

##Bonus: Additional Large Shapes
You can get some other useful shapes using variations on the #Code(:Height4:) technique.  You can create triangular, hexagonal and 'logic-gate' shapes.  

However, Scorpio is not yet smart enough about calculating how the text should fit in so unlike the previous large shaped tiles, these examples have bodges to make them work. 

As well as using \n to make extra lines, in some of these examples I use #Code(:Width:) to tell Scorpio to make adjustments to the amount of space for the text.  These are both temporary kludges to enable these shapes to work at all. #Rock(Later versions of Scorpio will not need #Code(:Width:) to get these shapes).
!!Raw
:Width4.1:\"Triangular\n\n\n\n"/
!!Scorpio
##TheStandardStyle
:A: :Width4.1:\"Triangular\n\n\n\n"/
boxed: 160
:A: at: 150,80
!!Raw
:Width4.1:/"\n\n\n\nTriangular"\
!!Scorpio
##TheStandardStyle
:A: :Width4.1:/"\n\n\n\nTriangular"\
boxed: 160
:A: at: 150,80
!!Raw
:Height5:&lt;Hexagonal&gt;
!!Scorpio
##TheStandardStyle
:A: :Height5:<Hexagonal>
boxed: 130
:A: at: 150,65
!!Raw
:Height3:["Nor")
!!Scorpio
##TheStandardStyle
:A: :Height3:["Nor")
boxed: 150
:A: at: 150,77
!!Markdown

##Fancy ends
These are some other custom end shapes:
!!Raw
:snake_tail:"snake ends":snake_head:
!!Scorpio
##TheStandardStyle
:A: :snake_tail:"snake ends":snake_head:
boxed: 100
:A: at: 200,50
!!Raw
:cold_front:"meterology":warm_front:
!!Scorpio
##TheStandardStyle
:A: :cold_front:"meterology":warm_front:
boxed: plain
:A: at: 150,27
!!Markdown
&nbsp;