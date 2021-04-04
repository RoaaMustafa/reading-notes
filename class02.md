# Read: 02 - HTML Text, CSS Introduction, and Basic JavaScript Instructions

### HTML 
+ markup :These tags provide extra meaning and allow browsers to show users the appropriate structure for the page.
  - Structural markup: the elements that you can use to describe both headings and paragraphs
  - Semantic markup: which provides extra information; such as where emphasis is placed in a sentence, that something you have written is a quotation (and who said it), the
meaning of acronyms, and so on.
+ Headings : `<h1>,<h2>,<h3>,<h4>,<h5>,<h6>`
+ Paragraphs : `<p></p>`
+ Bold : `<b></b>`
+  Italic : `<i></i>`
+  Superscript : `<sup></sup>` : E=MC<sup>2</sup>
+ Subscript: `<sub></sub>` : CO<sub>2</sub>
 `<br />` : showeach new paragraph or heading on a new line.
`<hr />` : add a horizontal rule between sections using the `<hr />` tag.
 `<strong>` indicates that its content has strong importance.
 `<em>` element indicatesemphasis that subtly changesthe meaning of a sentence.
 `<blockquote>` element isused for longer quotes that takeup an entire paragraph.
  ` <q>` element is used forshorter quotes that sit withina paragraph.
 `<abbr>`element can be used If you use an abbreviation oran acronym .
 `<cite>` element can be usedto indicate where the citation isfrom.
 `<dfn>` The <dfn> element is used to indicate the defining instance of a new term.
  `<address>` element has quite a specific use: to contain contact details for the author of the page.
  `<ins>` element can be used to show content that has been inserted into a document, while
 `<del>` element can show text that has been deleted from it.   
 `<s>` element indicates something that is no longer accurate or relevant (but that should not be deleted).
  
  ### CSS 
  `<link>` element can be used in an HTML document to tell the browser where to find the CSS file used to style the page.
  `href` This specifies the path to the CSS file
  Universal Selector * {}
  Type Selector h1, h2, h3 {}
  Cl ass Selector .note {}
  ID Selector #introduction {}
  Chil d Selector li>a {}
  Descendant Selector p a {}
  Adjacent Sibling Selector h1+p {}
  General Sibling Selector h1~p {}
  ### JS
  
  `<script></script> `
  ```
 //Create variables for the welcome message
var greeting = 'Howdy ';
var name = 'Molly';
var message= ', please check your order: ' ;
c02/ js/example.js
// Concatenate the three variables above to create t he welcome message
var welcome = greeting + name + message;
// Create variables to hold details about the sign
var sign = 'Montague House' ;
var tiles= sign.length;
var subTotal = tiles * 5;
var shipping = 7;
var grandTotal = subTotal + shipping;
// Get the element that has an id of greeti ng
var el = document .getElementByid('greeting') ;
// Replace the content of that element with the personal ized welcome message
el .text Content = welcome;
// Get the el ement that has an id of userSign then update its contents
var el Sign = document .getElementByld('userSign ' ))
elSign .textContent = sign ;
// Get the element that has an id of ti l es then update its contents
var elTiles = document .getElementByid('tiles');
elTiles .textContent = tiles ;
// Get the element that has an id of subTotal then update its contents
var elSubTotal = document.getElementByid('subTotal ' );
el SubTotal .textContent = '$' + subTotal;
// Get the element that has an id of shipping then update its contents
var elSubTotal = document .getElementByid('shipping') ;
el SubTotal .textContent = '$' +shipping;
// Get the element that has an id of grandTotal then update its contents
var elGrandTotal = document.getElementByid( 'grandTotal ') ;
elGrandTotal .textContent = '$ ' + grandTotal;
```
