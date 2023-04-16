# Components
The three main components of diagrams are labels, links and information cards.  The following line specifies a label called #Code(A) with the text "#Code(My first label)".

!!Raw
:A: My first label
!!Markdown

Sometimes you will need to put the text for a label in quotes. For example, if the label has #Code($$) at the start, Scorpio will treat the label as a mathematical equation. Most of the time you won't need to put quotes round the label.

To join label #Code(B) and #Code(C) use:
!!Raw
link: B C 
!!Markdown

Upper case letters such as #Code(A), #Code(B), #Code(C), represents the labels.

Additional information for a label, link or angle follows afterwards.  For example this joins #Code(G) and #Code(K) with a double link:
!!Raw
link: G K ==
!!Markdown

These three lines change the text of label #Code(B) to say #Code(Hello!) and then set its #Code(level) to #Code(3).

The #Code(level) can change the size of the label and its colour.
!!Raw
:B:
label: Hello!
level: 3
!!Markdown

> #Button(scorpio_connections,Connections) - More about labels and connecting them<br>#Button(scorpio_label_styles,Labels) - More about styling labels<br>#Button(scorpio_link_styles,Links) - More about styling links

## Tree of links format

It's very common to make 'trees' of things connected to things.  There's a shorter format for that. The two specifications that follow are equivalent:
!!Raw
* Foods
** High Fat
!!Raw
:A: Foods
level: 1
:B: High Fat
level: 2
link: A B
!!Markdown

The two examples do the same thing.  

#Code(A) and #Code(B) aren't mentioned in the first spec.  The first time you mention a label you don't have to give it a letter.  

* A letter is chosen automatically.
* The level is set by the number of stars
* The link from the one star to the two star item is created automatically.

Use this short format to paste in a list indented with #Code(&ast;)s and get a tree structure.  Scorpio will add the letters like #Code(:A:).

When you look at the spec you will see it has been changed to something like this:
!!Raw
*:A: Foods
**:B: High Fat
!!Markdown

Scorpio has added in the letters for you.  Scorpio will continue to do its best to update the letters sensibly when you edit the spec.  When you add a row or remove a row, or change the order of some lines,  you don't have to go through 'renumbering' the lines to be sequential.  Scorpio will do that for you.

## List format
Using the stars to indent the list and make some connections automatically is optional.  You can just list the labels and then make the connections explicitly.

Here's an example:
!!Raw
London
Edinburgh
link: A B --direct flights, daily-->
!!Markdown

This is for a diagram with an arrow between 'London' and 'Edinburgh'.  When the file comes back from Scorpio it will look like this:
!!Raw
:A: London
:B: Edinburgh
link: A B --direct flights, daily-->
!!Markdown

 #Button(scorpio_diagrams,Diagrams) - Description of the features of Scorpio diagrams