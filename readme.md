Etsy-thanks ASCII Art Displayer
================================

This is a tiny JavaScript (+ HTML & CSS) program that slowly displays an ASCII art image that I made, character-by-character. I made it as a thank-you to the folks at Etsy that sponsored me as a student at Hacker School.

###See it in action here:
www.emilysommer.com/thanks.html

Code Choices
------------

I wanted the code itself to look cool and show off the ASCII art, so I loaded the art in as a variable in text:
<pre>
"      111111111111111111111111\n",
"      11                    11              #######         #######\n",
"      11  1111111111111111  11            ###########     ###########\n",
"      11  0011001100111111  11           #############  ##############\n",
"      11  1111111111111111  11           #############################\n",
"      11  1100001100001111  11            ###########################\n",
"      11  1111111111111111  11             #########################\n",
"      11  1111111111111111  11              #######################\n",
"      11                    11                ###################\n",
"      111111111111111111111111                 #################\n",
"              11111111                           #############\n",
"        11111111111111111111                       #########\n",
"      111111  11  11  11  1111                       #####\n",
"      1111  11  11  11  111111                         #\n",
"      111111111111111111111111\n",
"\n",
"\n",
"===================/|\n",
"``\\===============\\\\|\n",
"   ===|            ||      /|\n",
"   ===|            ''     /=|\n",
"   ===|                  /==|\n",
"   ===|        ||     __/===|=====    /=========\\   =========     =========\n",
"   ===|_______//|     ============   /===      \\=|   \\====/        \\====/\n",
"   ===========\\\\|        ===|        |==        \\|    \\===\\         \\==/\n",
"   ===|        ||        ===|        \\====             \\===\\         =/\n",
"   ===|                  ===|          \\====            \\===\\       =/\n",
"   ===|                  ===|             =====          \\===\\     =/\n",
"   ===|            ..    ===|                ====\\        \\===\\   =/\n",
"   ===|            ||    |===\\   ,,  |\\        ===|        \\===\\ =/\n",
",,/===============//|     \\======/   |=\\       ===/         \\====/\n",
"===================\\|       ===/      \\==========/           \\==/\n",
"                                                              //\n",
"                                                   |\\        //\n",
"                                                   |\\\\______//\n",
"                                                    \\=======/\n"
</pre>

I then joined the lines, split by character, reversed it so I could pop off tokens on each loop of the display code.

Once I had my array of characters, I added spans with css classes to control the colors and swapped out '\n' (newlines) and spaces for their appropriate html counterparts ('<br>' and '&nbsp;' in this case).

The display function could be a lot faster -- it slows down towards the end because I'm appending elements to the text div each time, and as that grows, it gets slower to read it in and add html to it. It would be likely be faster to make a new div for each line and use appendChild() to add them to the outer text div.

Future Goals:
--------------
- [ ] Optimize for speed, break character additions into line-by-line divs to keep speed equal throughout runtime (it currently slows down towards the end).
- [ ] Generalize this! Have it accept a text variable as input and some rules for the coloring of it and output the dislay code.

Proud of:
----------
- My design choice to use certain characters only for each logo -- made it very simple to style with css afterwards.
- The success of the art itself (this was my first go at ASCII art)
- That I kept the beauty of the design in the code -- a friend suggested to me to do the edits to the text in the code instead of doing a find-and-replace before loading in the ASCII text (for things like newlines and white space that needed to be converted to html).

License:
---------
? Feel free to use to your liking.
