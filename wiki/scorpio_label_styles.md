# Scorpio Labels

The brackets that you put around text for a label determine the shape of the label.  Click on any example to edit.  

These first few examples have matching shapes for left and right ends. Labels will have round ends if you don't specify what shape the ends should be.
!!Raw
(round ends)
&lt;chevron ends&gt;
[straight ends]
/forward ends/
\backward ends\
!!Scorpio
##TheStandardStyle
boxed: 180
caption: End shapes
:A: (round ends)
:B: <chevron ends>
:C: [straight ends]
:D: /forward ends/
:E: \backward ends\
:A: at: 147,33
:B: at: 149,62
:C: at: 148,93
:D: at: 147,125
:E: at: 150,157
!!Markdown
## Mixed ends
How you mix and match the ends is up to you....
!!Raw
)rounded inwards(
/mixed ends)
>some other mixed ends]
!!Scorpio
##TheStandardStyle
boxed: 100
:A: )rounded inwards(
:B: /mixed ends)
:C: >some other mixed ends]
:A: at: 173,17
:B: at: 169,49
:C: at: 179,81
!!Markdown

##Quoting, Emoji, \n

> Quotes around the text of the label can help Scorpio know what is part of the label text and what is part of the label shape.  Use quotes around the text of the label to make it clear.

In the examples shown so far, you don't have to put the text of the label in quotes.  With labels that have the end indicators in them, you may need to.  It is always OK to use quotes.  Scorpio uses whatever text is inside the quotes.

For this example the quotes indicate that the spaces and the square brackets are inside the label, and the label has its usual round ends.  Without the quotes the extra space would be gone and the label would have square ends.
!!Raw
"   [quoted]   "
!!Scorpio
##TheStandardStyle
:A: "   [quoted]   "
boxed: plain
:A: at: 150,27
!!Markdown
You can use emoji in a label, and you can use #Code(\n) to indicate a multi-line label.
!!Raw
("🛡Immune \nSystem")
!!Scorpio
##TheStandardStyle
:A: ("🛡Immune \nSystem")
boxed: 80
:A: at: 150,40
!!Markdown
The #Code(\) has special meaning.  If you need a #Code(\) or a #Code(") in the label, then use a #Code(\\) and #Code(\") respectively.  In the next example there is a #Code(\) before each of the quotation marks in the label.
!!Raw
&gt;"a \"quoted\" word"&gt;
!!Scorpio
##TheStandardStyle
:A: >a \"quoted\" word>
boxed: plain
:A: at: 150,27
!!Markdown
The example below has a #Code(\\).  When Scorpio sees #Code(\\) it show it as #Code(\) and the letters after, such as #Code(n), is shown normally.  The second #Code(\n) in this example has only a single #Code(\), and so it is shown as a line break.
!!Raw
&gt;"A \\n causes a\nline break" &gt;
!!Scorpio
##TheStandardStyle
:A: >"A \\n causes a\nline break">
boxed: 80
:A: at: 150,40
!!Markdown
##Arrows
Scorpio also has arrow shaped ends.
!!Raw
&lt;=arrow ends=&gt;
[arrow right=&gt;
&gt=fancy tail feathers=&gt;
!!Scorpio
##TheStandardStyle
boxed: 140
:A: <=arrow ends=>
:B: [arrow right=>
:C: >=fancy tail feathers=>
:A: at: 132,24
:B: at: 133,63
:C: at: 137,100
!!Markdown

There are some additional shapes on the 'more label styles' page.
#Right([more label styles](more_label_styles))

##Long and Short form
All the short form end shapes also have a long form version.  These are equivalent:

* #Code(&#40;) - #Code(:round:)
* #Code(&lt;) - #Code(:chevron:)
* #Code([) - #Code(:straight:)
* #Code(/) - #Code(:forward:)
* #Code(\) - #Code(:backward:)
* #Code(=&gt;) - #Code(:arrow_head:)
* #Code(&gt;=) - #Code(:arrow_tail:)

For the flipped versions of simple shapes, add #Code(Flip) to the name, so #Code(:chevronFlip:) will give #Code(&gt;) rather than #Code(&lt;).

##Round, Square and Diamond Labels
You already have seen the syntax for doing small round, square and diamond shaped labels:
!!Raw
(a)
[b]
&lt;c&gt;
!!Scorpio
##TheStandardStyle
boxed: 120
##TheStandardStyle
caption: Example
:A: (a)
:B: [ b ]
:C: <c>
:A: at: 112,37
:B: at: 112,66
:C: at: 112,97
!!Markdown
You can get larger shapes by forcing the number of lines of text, either using \n to add extra blank lines or using #Code(:Height:)
!!Raw
:A: ("\nRound\n")
!!Scorpio
##TheStandardStyle
:A: ("\nRound\n")
boxed: 100
:A: at: 150,50
!!Raw
:Height4:(Round)
!!Scorpio
##TheStandardStyle
:A: :Height4:(Round)
boxed: 100
:A: at: 150,50
!!Raw
:Height4:[Square]
!!Scorpio
##TheStandardStyle
:A: :Height4:[Square]
boxed: 100
:A: at: 150,50
!!Raw
:Height9:&lt;Diamond&gt;
!!Scorpio
##TheStandardStyle
:A: :Height9:<Diamond>
boxed: 150
:A: at: 150,75
!!Markdown
&nbsp;
