# 7seg
7seg is a simple JavaScript and SVG-based applet to render a time in the style of a seven-segment display.  Feel free to adapt and modify as you see fit;  I did experiment with changing the display size but to be honest it got pretty tricky to keep everything aligned.  There are some placeholder SVG filters remaining in the code too; these are to be fixed at a later date.

There is an idea, but no plans, to implement full 14- or 16-segment display; this is no small task, but would allow display of text characters.  The code can easily be modified to add more or less digits to the display; 

##To use
The update() function does the bulk of the work.  It accepts a string (the picker provides a time in HH:MM) and populates an SVG canvas with id="display".  time() gets the current system time, pads out the hours and minutes as necessary (Date() omits the leading zeros?!), and passes the resulting string to update().

The applet will accept any number of digits (although it was written for four, plus the : in the middle).  The colon is hard-coded at the moment; you can use the display for decimal numbers if you want, but only two digits on the left-hand side.  To modify, just change the switch(index) values for both the horiz() and vert() functions.


View the code for more information.
