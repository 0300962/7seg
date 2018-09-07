# 7seg
7seg is a simple JavaScript and SVG-based applet to render a time in the style of a seven-segment display.  Feel free to
 adapt and modify as you see fit;  I did experiment with changing the display size but to be honest it got pretty tricky
  to keep everything aligned.  There are some small clipping issues remaining on the neon blur; this may be fixed in the 
  future if the SVG standard is updated.

There is an idea, but no plans, to implement full 14- or 16-segment display. This is no small task, but would allow display
 of text characters; so I may get around to it eventually.

Try it out here: https://0300962.github.io/7seg/7seg.html

## To use
The update() function does the work.  It accepts a string (the picker provides a time in HH:MM) and populates
 an SVG canvas with id="display".  time() gets the current system time, pads out the hours and minutes as necessary 
 (*Date() omits the leading zeros?!*) and passes the resulting string to update().  Update() looks for two variables (*fill*
  and *stroke*) to set the colours used in the display; the background comes from the containing div.

The applet will accept any number of digits (although it was written for four, plus the : in the middle).  The colon is
 hard-coded at the moment; you can use the display for decimal numbers if you want, but only two digits on the left-hand
  side.  To modify, just change the switch(index) values for both the horiz() and vert() functions.


View the code for more information.
