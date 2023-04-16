##HTML Snippet

The HTML snippet is similar in style to [Google charts](https://developers.google.com/chart/interactive/docs/quick_start).  The snippet shows how to call Scorpio to make a chart. 

You can copy the snippet to a .html file on your computer and then open in a browser to see the chart.

Most of this snippet is taken up with the diagram spec itself.  

!!Raw
&lt;!DOCTYPE html&gt;
&lt;html lang="en"&gt;
  &lt;head&gt;
    &lt;meta charset="utf-8"&gt;
    &lt;script data-cfasync="false" src="http://www.scorpiodiagrams.com/js2/jsloader.js"&gt;&lt;/script&gt;
    &lt;script type="text/javascript"&gt;

      // Load the modules you'll be using...
      scorpio.load('diagrams annotations katex');

      // Set a callback to run when scorpio is ready
      scorpio.setOnLoadCallback(makeDiagram);

      // Callback that makes the diagram
      function makeDiagram() {
        var diagram = new scorpio.diagram();
        diagram.setDiv( document.getElementById( 'diagram_div' ));
        diagram.setSpec(
`
&#35;&#35;StarMap
caption: The constellation of Orion
*:A: ("🌟")
*:B: ("🌟")
*:C: ("🌟")
*:D: ("🌟")
*:E: ("🌟")
*:F: ("🌟")
*:G: ("🌟")
*:H: ("🌟")
*:I: ("🌟")
*:J: ("🌟")
*:K: ("🌟")
*:L: ("🌟")
:A: at: 217,112
:B: at: 325,126
:C: at: 244,250
:D: at: 271,234
:E: at: 298,220
:F: at: 474,115
:G: at: 219,360
:H: at: 335,256
:I: at: 374,351
:J: at: 296,75
:K: at: 455,196
:L: at: 424,42
background: &#35;113
link: * *
bend: 0
link: A B
link: A C
link: C D
link: D E
link: E B
link: C G
link: E H
link: H I
link: B J
link: A J
link: B F
link: F K
link: F L
:A:
card:
&#35;&#35; Betelgeuse
&#35;&#35;&#35; Alpha Orionis
Betelgeuse is the second brightest of the stars in Orion, with a visual magnitude of 0.7. It's 13,000 times more luminous than our sun, and is 520 light years away.
:B:
card:
&#35;&#35; Bellatrix
:C:
card:
&#35;&#35; Alnitak
:D:
card:
&#35;&#35; Alnilam
:E:
card:
&#35;&#35; Mintaka
:J:
card:
&#35;&#35; Meissa
:G:
card:
&#35;&#35; Saiph
:I:
card:
&#35;&#35; Rigel
&#35;&#35;&#35; Beta Orionis
Rigel is the star with the highest absolute magnitude in the Southern hemisphere, with a magnitude of -7.1.  It's around 25,000 times more luminous than our sun.  It is about 900 light years away, and its visual magnitude (as seen from Earth) is 0.15.
`
          );
      }
    &lt;/script&gt;
  &lt;/head&gt;

  &lt;body&gt;
    &lt;!--Div that will hold the diagram--&gt;
    &lt;div id="diagram_div"&gt;&lt;/div&gt;
    &lt;br clear=all&gt;
  &lt;/body&gt;
&lt;/html&gt;
!!Markdown

&nbsp;