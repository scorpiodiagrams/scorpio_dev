!!Polyglot
## Design Guide

### Markdown
The markdown should be:
* Compatible with Obsidian#Footnote(1).
* Usable with GitHub#Footnote(2). 

Need a space after a #Hash in titles as both Obsidian and GitHub require that. Obsidian is kind of strange about nesting paragraph styles, and something needs sorting there.

I aim to do smarts on hyperlinks, so that we can show info cards for a link on hover, and trap chapter and section references and recognise that they are in the same document.

Similarly exercises and figures can be picked up from the naming of the header.

```Raw
### %Footnote xxxx
### %Exercise xxxx
### %Figure xxxx
### %Footnote xxx
### %Word xxxx
### %Fold xxxx
### %Card xxxx
### %End
```

Some lists can be created by state changes. For example an idiolect page can be made by listing subheads.

I also do some custom smarts with these:
```Raw
\UFO
\Boat
\Rock
```

### JaTeX

### Scorpio Specs
The short form should be using the highly mnemonic syntax such as:

```raw
 > Text >   for text on a chevronned label
 ~~[Text]~~ for text in a square box on a wiggly link
```

It should be possible to paste in a bulleted list and nothing else and get a tree diagram. Everything should be taken care of, default sizes, colours, styles.

### Auto Numbering

Everything 'of sufficient size' should get a number (in the form A,B... AA, AB...) for itself, and these should be renumbered as required.

In particular a label on a link should get a number too, so that it is 'a proper label'

### Positioning

The default positioning should be at least 'sane', and conform with any connections that have been specified by the hierarchy. I'm using a simple spring based energy minimiser. The expectation is that you will then drag the items into position.

Dragging should respect the hierarchy, or in other words be 'Scratch like'. When you drag an item, its descendants and younger siblings should be dragged by the same amount.

It should be possible to drag a label that is on a link and have the position update. The position will be recorded as a percentage rather than as an absolute position. Dragging the label should bend the link, or the position should snap back if bending is disallowed.

### Subdiagrams

It should be possible to specify an existing complex diagram as a sub-diagram

### Code

Support for code as well as data is an essential, even if data is the dominant mode.

### Data Islands

Scorpio should be capable of consuming data islands.

### Info Cards

----
### Footnotes

### %Footnote(1)
In particular Scorpio should/could handle Obsidian drop downs. Scorpio directives may not be picked up by Obsidian, but their display can still be reasonable.

### %Footnote(2)
GitHub should generally display the markdown in an intelligible way. GitHub is more picky about LaTeX and line breaks than it could be, so extra blank lines are needed around some constructs to avoid the all-on-one-line effect.
#FootnoteEnd