!!Polyglot
# Musings


### Consistency is Good?
Consistency is great for reference material. On its own it is not wonderful for memorable content. The diagrams could be boring, too similar to each other. I wanted diagrams that are easy to make *and* that I can easily customise with hand crafted details. These added details act as visual landmarks. The diagrams become more useful for learning from, not just as reference material. Without customisation, there would be too big a quality gap between automatic and hand-crafted diagrams.  

Maintaining a balance between automated structure and hand crafted detail is hard. It's a particular problem when the underlying information behind a diagram is updated. I'm trying to solve that problem so that information rich *educational* diagrams become easier to make.
----
### Diagrams and MidJourney
Originally I planned to use spot-art in the diagrams to make the images more memorable. I also planned to create styled brushes to draw the curved lines, so that those too could be styled. A diagram of photosynthesis could have a leaf or a molecule of Chlorophyll at the centre. 'Motorways' in a biochemical diagram could be styled differently from the by-roads.

I had the idea that textural detail could be filled in programmatically by 'greebling'. Rather than using only in-fill-colours, I'd in-fill using textures adapted to the shapes around them. This could be used to indicate information that's normally shown by colour coding. For example different textures could indicate different compartments in the cell. 

MidJourney makes the creation of spot art from text description quick and easy. The [warpable textures](wip4) could make styled brushes easy, styled with patterns generated in MidJourney and imported in. 

The greebling though needs something that's not there yet.
----
### Standards are Good?
* With JaTeX I'm breaking from the LaTeX standard. 
* With Scorpio diagrams markdown I'm close to, but still breaking with standard Markdown.

The reason to break with the standards is try out new things. I want to try new ideas. I don't want to additionally recreate the full LaTeX stack, or the full Obsidian experience. It's too much work as a solo developer to carefully match every quirk and detail in new software. Instead I implement the pieces I see as essential.

With open source code, I could fork and reuse. But I don't want to fork and adapt the existing libraries either. KaTeX is built around the HTML DOM. I have chosen instead to be built around the HTML Canvas. Typst is in rust. I don't want ot be in rust. I want to be in JavaScript where I can develop faster.

> [!info]- Lifecycle of Re-Implementations

### A new Version of X
A new implementations of established software often start its lifecycle with claims to how it is smaller, simpler and faster than the software that inspired it. That's the merit that can be pointed to when the software is immature and incomplete. The real reason for touting these virtues is that in the early days you don't have a feature rich program to show.

Gradually the lean mean software gathers cruft and bloat. It loses the simple logical design, because it's easier to bolt on someone else's library or feature than to write something better from scrarch. After a while the software is a mess and it's time to write a new version.)
----
