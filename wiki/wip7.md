# Work in Progress VII

Experiments with a new Markdown processor. This processor, Polyglot, tokenises the text and then processes token by token, the same design as for JaTeX. This is in contrast my previous scheme, which used a lot of hacked together regexs. The previous scheme could not handle brackets well.

Polyglot doesn't use the zim-style markdown I used to use, but uses Obsidian style instead. Obsidian is mainstream markdown (with extensions) and is compatible with more tools than zim is. In particular, obsidian-style is close to GitHub's markdown style. My intent is that raw markdown docs can be stored at GitHub and can be read there, despite the extensions I make. Often polyglot extensions are named like #SomeFuntion(), which markdown just shows as-is.

GeSHi islands are explored/tested on this page, along with other test cases that matter.
!!Polyglot
----
## Polyglot
Between the two horizontal rules we are in polyglot. This text should be very readable in Obsidian. The markup should be compatible.

#CommandList

#JatexList

 /δ/ function, [454](chapter006!p454) (ex. [6.12](chapter006!exercise_6.12) )
 /δ_{η}/ (variation operator), [26](chapter001!p26)

> [!info]+ Picking up a block??
Pick up the block!
Line 1
Line 2
```Koolaid
Line 3
Line 4
```)
#PopBox( PopUp1

# Popup Box 1
* Line 1
* Line 2
> a cool piece of text
)
#PopBox( PopUp2 

# Popup Box 2
## More Titles
)
#PopBox( PopUp3

# Popup Box 3
## Yet more titles
)
```Scheme
(define ((H0 alpha) state) (let ((p (momentum state))) (/ (square p) (* 2 alpha)))) (define ((H1 beta) state) (let ((theta (coordinate state))) (* -1 beta (cos theta)))) 
```
> [!info]+ Code Readiness Indicators
#UFO(**UFO**) - plans for the *far* future
#Rock(**Rocket**) - plans for the near future
#Boat(**Boat**) - old shipwrecked plans that need refloating
)
> [!info]+ Polyglot Headings
# h1 text
## h2 text
### h3 text
#### h4 text
)

We are `handling` markdown \very differently to the pre polyglot markdown processor that we had.
  - Indented
- Less indented

This text has **bold** text in the middle of it.
```Verbatim
Some verbatim text
```
```
Raw box with no type field
```
## A heading with some text in it!
Bold is achieved with *double stars* on either side, as usual.
We can use `#Code(xyz)` to get bold #Code( xyz ) too.
![[./images/BlocksMissing.png|300]]
#Button(wip,Development)

```SQL
SELECT * from tables WHERE foo = bar;
```
Some text between the two GeSHi islands.
```javascript
var foo="1234";
function jack( a b c ){
  return "abcdef";
}
```
----
!!Markdown

