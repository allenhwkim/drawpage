drawpage
========

Draw outline of your web page and disappear.


Inspired by [svg drawing animation](http://tympanus.net/Development/SVGDrawingAnimation/), I thought we can draw any outline of any webpage by following the paths of box models, and this is the result.

[demo](https://rawgit.com/allenhwkim/drawpage/master/demo1.html)

How to use
----------

  * To draw page every time when page loads, append the following code at the end of your page

        <script src="https://rawgit.com/allenhwkim/drawpage/master/draw-page.js"></script>
        <script>drawPage()</script>

  * Or, only to test how it looks like 

    1. Go to any web page, and open a console
    2. copy paste the following code if ["Content-Security-Policy"](https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy) is allowed

             (function() {
                var dp = document.createElement('script'); dp.type = 'text/javascript'; dp.async = true;
                dp.src = 'https://rawgit.com/allenhwkim/drawpage/master/draw-page.js';
                document.documentElement.appendChild(dp);
              })();

    3. run `drawPage()` command

Options
-------
    
  drawPage function accepts one parameter

  * css selector  
    in default, "div". For example;  

    `drawPage("table")` will draw all tables in the document.  
    `drawPage(".drawme")` will draw all elements that has `drawme` class.

