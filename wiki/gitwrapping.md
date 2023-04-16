!!Polyglot
## Gitwrapping

You can host diagram specs at no cost using a method called 'gitwrapping'.  You place your specs at GitHub.  You then use [this link](gitwrapped.html) to view them, wrapped with the Scorpio JavaScript.  

> In some ways this is similar to having GitHub run Jekyll for you to deploy a website.  Gitwrapping does more than process the diagrams. It also processes markdown pages that you push to GitHub.  You can build multiple connected pages with text formatted from markdown and multiple diagrams this way.

< One difference to Jekyll is in when the processing is done.  The formatting and interaction with info cards relies on JavaScript, and is done client side rather than server side.

Regard the gitwrapping feature as a low effort way for you to get a Scorpio based website.  You save your specs and markdown files at GitHub and the gitwrapping will display them. Updates to the 'website' are immediate on pushing to GitHub. 

More sustained use should use the [snippet](snippet) method and use external JavaScript, e.g. from a CDN, or you should host the Scorpio JavaScript files as well as your content.