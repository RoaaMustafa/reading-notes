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
  var today= new Date{);
var hourNow = today.getHours{) ;
var greeting;
if (hourNow > 18) {
greeting= 'Good evening';
else if (hourNow > 12) {
greeting= 'Good afternoon';
else if (hourNow > O) {
greeting 'Good morning';
else {
greeting 'Welcome';
document.write(greeting) ;
```
```
var price;
var quantity;
var total;
price = 5;
quantity = 14;
total = price * quantity;
c02/j s/numeri c-vari ab 1 e .j s
var el = document.getElementByid( ' cost ' ) ;
el .textContent = '$' +total;
```
