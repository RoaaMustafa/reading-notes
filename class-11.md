# Read: 11 - Assorted Topics
## Readings : Audio, Video, Images
### HTML
#### Images
1. I learned how to conrol the size of image using `width:`,`hight:`
2. how to align image using `float:right or left` and `margin-right or margin left`
3. how to center image useing  `display:block `and `margin:0px auto`
4. How to set a backgroung image using this code line: `background-image: url("images/pattern.gif");`
5. `background-repeat`:`repeat`,`repeat-x` for repeate horizintally ,`repeat-y `repeated virtically,`no-repeat` ,`background-attachment`:**fixed**: The background image stays in the same position on the page.,**scroll**:The background image moves up and down as the user scrolls up and down the page.
6. change background position using:`background-position` : left top,left center,left bottom,center top,center center,center bottom,right top,right center,right bottom or The top left corner is equal to :0% 0%. values of 50% 50%: centers the image horizontally and vertically.
7. it is possible to create a link or button that changes to a second style when a user moves their mouse over it (known as a rollover) and a third style when they click on it.
    + The **background-position** property is used to move the image in order to show the button in the right state.
    + the **:hover** pseudo-class has a rule that moves the **background-position** of the image to show a different state for that button.
    + when the user clicks on the link, the **:active** pseudo class has a rule to show the third state for that button.
8. can set backgorund-image in different ways: 
```
#gradient {
/* fallback color */
background-color: #66cccc;
/* fallback image */
background-image: url(images/fallback-image.png);
/* Firefox 3.6+ */
background-image: -moz-linear-gradient(#336666,
#66cccc);
/* Safari 4+, Chrome 1+ */
background-image: -webkit-gradient(linear, 0% 0%,
0% 100%, from(#66cccc), to(#336666));
/* Safari 5.1+, Chrome 10+ */
background-image: -webkit-linear-gradient(#336666,
#66cccc);
/* Opera 11.10+ */
background-image: -o-linear-gradient(#336666,
#66cccc);
height: 150px;
width: 300px;}
```
9. contrast of background image:If you want to overlay text on a background image, the image must be low contrast in order for the text to be legible.
   + A high contrast background image makes the text difficult to read.
   + A low contrast background image makes the text easier to read.
   + A screen added to a high contrast image makes the text easier to read.
### Practical Information
+ Search engine optimization
+ Using analytics to understand visitors
+ Putting your site on the web
1. Search Engine Optimization (SEO): **What?** to help your site appear nearer the top of search engine results when people look for the topics that your website covers.
2. On-page techniques are the methods you can use on your web pages to improve their rating in search engines.
3. Off-Page Techniques Getting other sites to link to you is just as important as on-page techniques. Search engines help determine how to rank your site by looking at the number of other sites that link to yours.

 
