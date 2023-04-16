#ScorpioHead(27 February 2023, Download Diagrams)
!!Polyglot
##Downloads

For downloading diagrams you've created, open the #Code(Details) panel ([it's below the diagram](scorpio_details_panel)) and then click on #Code(Download).  

There are several download options:

> **Html Snippet:**<br><br>This saves your spec embedded in html.  When viewed in a browser, this snippet will invoke the Scorpio library and make one diagram.  The library code is fetched from the cloud.  
#Right([HTML Snippet](snippet))

> **Diagram Spec:**<br><br>The #Code(Diagram Spec) option downloads your spec as a text file. The text spec can then be used to:<ul><li>work on the diagram again later (there's an upload button in another panel)</li><li>to host diagrams with the info cards on your own website and server</li><li>to host diagrams using GitHub storage (gitwrapping)</li></ul>
#Right([Gitwrapping](gitwrapping))

> **Image:**<br><br>To download a still image of the diagram you've created use #Code(Image).  The result will be a .png file.<br><br>Use the #Code(Image) download if you don't need the info cards that pop up when you hover, and just want a still image.

If you are using #Code(Image) to get annotations, you can if you like remove the background before you download.  The downloaded image will then have transparent regions, and can be used as an overlay.
----
## For Developers

The source files are available at GitHub.

> **GitHub:**<br><br>The JavaScript software is available from [my GitHub repo](https://github.com/scorpiodiagrams/Scorpio).  The code is MIT licensed.  

The repo at GitHub can be used as-is to serve Scorpio pages and diagrams.

* It includes sample text and images in the #Code(./contents/) subdirectory.
* It has an #Code(index.html), which will do the serving of pages with diagrams.  It fetches both markdown files and files with diagram specs and puts them together to make complete pages.
* It has a #Code(snippet.html), which is an example of serving one single diagram
* It has a #Code(gitwrapped.html), which shows how gitwrapping is done.  #Code(gitwrapped.html) is #Code(index.html) with different config parameters.

Additionally the repo has #Code(LICENSE), #Code(README) and #Code(./docs/)


