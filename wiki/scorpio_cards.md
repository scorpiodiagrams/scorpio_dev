### Info Cards

Scorpio diagrams can add labels to diagrams and images. These labels can provide more detail with 'info cards' - additional text that appears when your mouse pointer is on the label. Hover over the green labels to see the info cards.

!!Scorpio
##Mindmap
boxed:300
caption: Info cards shown on hover
:A: ( Hover over this label )
:B: ( ...and also this one )
:E: $$\kbd { Invisible \ \ Water }
:A: at: 124,36
:B: at: 470,47
:E: at: 185,230
background: VisibleWaterSmall.png
:A:
card:
##Info Cards
> Most of the iceberg is below the waterline
Scorpio can show info cards, like this one.  The cards stay out of the way, well away from the place where you hover.
:B:
card:
##Another Info Card
> But did you know, a lot of moisture in the air is *below* clouds? Air cools and expands as it rises. We see the flat bottoms of clouds because it's where the water must condense out.
This card gets shown on the other side from the first one.
:info:
card:
##Scorpio Info Cards
Each diagram has an info button in the top left.  This typically has general information about the diagram, including some copyright information.
 *Credits: &copy; James Crook 2023.*
!!Polyglot
Info cards can have hyperlinks in them. To get to the hyperlinks, move the mouse pointer reasonably quickly, to move it into the card without the card disappearing or moving away. 

The Immunology and Maxwell's Equations labels shown below have hyperlinks in their info cards.
!!Scorpio
##Mindmap
boxed:110
caption: Info cards shown on hover
:A: >Maxwell's Equations >
:B: < Immunology<
:C: $$\kbd #fd3 {The\ Body\ vs\ the\ Invaders ...}
:D: $$\kbd #fd3 {Magnets,\ Electricity\ and\ Light!}
:A: at: 283,90
:B: at: 455,41
:C: at: 188,5
:D: at: 37,53
background: LightningArt.png
:A:
card:
##🧲[Maxwell's Equations](maxwells_equations)⚡
Maxwell's equations are differential equations that describe electromagnetism. This [link](maxwells_equations) takes you to Wikipedia for more information.
:B:
card:
##🛡[Immunology](immunology)
Immunology is about how the body defends against pathogens.  This [link](immunology) takes you to Wikipedia for more information.
:info:
card:
##Scorpio Info Cards
Each diagram has an info button in the top left.  This typically has general information about the diagram, including some copyright information.
 *Credits: &copy; James Crook 2023.*
!!Markdown
If you move too slowly, the card will disappear. The intention is that info cards stay out of the way, that they provide additional information only for when you want to follow it.

!!Polyglot
> [!info]- Info Cards Elsewhere
Scorpio info cards are a similar feature to the preview 'tips' in Wikipedia, Obsidian and Arbital. They are also related to the idea of a 'master-detail' display, where one panel gives detail on an overview. 

Some ways Scorpio info cards differ:
* They work on diagrams and images, not just on text. 
* Rather than be right next to the mouse pointer, they are kept some distance away, so as not to cover where you are mousing over.
* Scorpio avoids a clutter of info cards when info cards have info cards, by updating the card rather than showing more than one at once.
* Scorpio's info cards use 'optical stability' to reduce the amount of flicker and 'jumping about' when you mouse-over different things. It's in how they move and the timing of how they change.
These are small changes that make the info cards more usable.)

> [!info]- The Info Button
The diagrams have an info button that appears in the top left hand corner when you're hovered over the diagram. Hover over this info button for an additional info card with copyright information.)

> [!info]- Scorpio uses Markdown

### Syntax 
Scorpio Daiagrams uses different syntax for different parts of the diagrams. Most text is specified with Markdown. Equations use JaTeX, a LaTeX like syntax. 

### Syntax for cards
The spec shown below has syntax for specifying two labels and a link between them. The info cards are specified at the end. The text of the cards is in Markdown format.
```Raw
##LineArt
:A: London
:B: Edinburgh
background:FakeMap.png
link: A B --only 332 miles-->
:A:
card:
## London
Londinium was a commercial centre in Roman Britain, which later became London.
:B:
card:
## Edinburgh
Edinburgh is the capital of Scotland.
```)
!!Scorpio
##LineArt
caption: Flights!
boxed: 130
:A: London
:B: Edinburgh
:A: at: 76,105
:B: at: 518,29
background: FakeMap.png
link: A B --only 332 miles-->
:A:
card:
## London
Londinium was a commercial centre in Roman Britain, which later became London.
#Wiki(London)
:B:
card:
## Edinburgh
Edinburgh is the capital of Scotland.
#Wiki(Edinburgh)
!!Polyglot
#Caption Fantasy Map #CaptionEnd
The map above has labels on it that use Markdown for their info cards.

Scorpio Markdown has a few extensions built in. For example `#HashWiki(` makes a hyperlink to Wikipedia.
