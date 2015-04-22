# dazzleSketch - OmniDazzle meets JavaScript
A JavaScript library that allows one to sketch over a web page or `reveal.js` presentation.  Quite useful when using 
`reveal.js` to give a live lecture or when you are using `reveal.js` to record a lecture using a tool like 
<a href="https://www.techsmith.com/camtasia.html" target="_blank">Camtasia</a>.

This is a bit of code that builds on the excellent `sketch.js` library that implements a simple sketching tool
using jQuery and the HTML5 canvas:

http://intridea.github.io/sketch.js/

I mimic the UI and keystrokes of the OmniDazzle drawing tool that worked so well but was not compatible with MacOS versions
beyond 10.8 :(. You add dazzleSketch to a web page using the following pattern:

    <html lang="en">
    <body>
        <h1>This is a Header</h1>
        <p>This is a paragraph that we will scribble on.</p>
        <script src="jquery-1.11.2.min.js"></script>
        <script src="sketch.js"></script>
        <script src="dazzleSketch.js"></script>
    </body>
    </html>

This also works well when added to the reveal.js HTML.  I would like to see it turned into a plugin for 
`reveal.js` - but I am sure it needs a bit of code review.

When dazzleSketch is loaded, you see no UI on the screen - it is just ready to scribble and 
activated using the following keystrokes.

* ctrl-` (next to the 1) erase and turn off drawing
* ctrl-1 Yellow Pen
* ctrl-2 Green Pen
* ctrl-3 Cyan Pen
* ctrl-4 Red Pen
* ctrl-5 White Pen
* ctrl-6 Blue Pen
* ctrl-7 Magenta Pen
* ctrl-8 Black Pen
* ctrl-- Make pen narrower
* ctrl-= Make pen wider

While you are scribbling most mouse movements will be taken over by dazzleSketch.  If you hover over a link, the 
a:hover action will not happen and you might not be able to click on a link in the HTML document until you 
clear the sketch overlay with ctrl-`.  This is because dazzleSketch makes an HTML5 canvas that covers 
the entire window area and uses z-index to be "on top" of the other HTML content on the page.   When you clear 
the screen, the dazzleSketch canvas is placed behind the rest of the content using z-index 
so all the normal mouse movements apply to the web content.

For me, I have a <a target="_blank" href="http://www.amazon.com/gp/product/B00115OFJK/ref=as_li_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=B00115OFJK&linkCode=as2&tag=drchu02-20&linkId=VKON6Z2MQ3TLWN6S">Wacom Cintiq 12WX 12-Inch Pen Display</a><img src="http://ir-na.amazon-adsystem.com/e/ir?t=drchu02-20&l=as2&o=1&a=B00115OFJK" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" />
that I remap the keys to make the drawing very smooth for nice drawings while recording lectures for 
my online classes.


 
