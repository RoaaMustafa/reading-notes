# Read03 HTML Lists, Control Flow with JS, and the CSS Box Mode
## HTML

 #### types of lists:

   `<ol> `  Ordered lists
  
   `<ul>` Unordered lists 
   
   ##### Definition lists: 
    
    `<dl>`   definition list 
     
     
    `<dt>` definition term
     
     
    `<dd>` definition content
     
  #####  nested list : 
   
   ```
   <ul>
<li>Mousses</li>
<li>Pastries
<ul>
<li>Croissant</li>
<li>Mille-feuille</li>
<li>Palmier</li>
<li>Profiterole</li>
</ul>
</li>
<li>Tarts</li>
</ul>
```

## CSS

>You can specify the width, height and even limit them with a minimum and a maximum value.

>Every box has a mirgin , a border & a padding ; that you also can control them by numbers or percentage.
```
mirgin:30px;
border:5px;
padding:25px;
```
>You can also control the text alignment `text-align:center;`, the visability of an element `visability:hidden;`, the border properties, displaying the list inline `display:inline-block;`, controlling the boxes shadows, and border corners by controling the radius.

## Java script

>Using quotes inside a string using ` document.getElementByld` and `elTitle.innerHTML` 

```
var title;
title= "Molly's Special Offers" ;
var elTitle = document.getElementByld('title') ;
elTitle.innerHTML =title;
```
>using a variable to store a boolean :   
 
  ```  
 var elShip = document .getElementByid('shipping');
 elShip.className = shipping ;
```


>comparing two expressions: 

```
//Check if scores are higher than current high scores
var comparison= (score!+ score2) > (highScorel + highScore2);
//Write the message into the page
var el = document.getElementByid( 'answer');
el .textContent ='New high score:'+ comparison;
```
  >or by using logical And &&:
```
//Check whether user passed both rounds , store result in variable
var passBoth = (scorel >= passl) && (score2 >= pass2);
//Create message
var msg = 'Both rounds passed: ' + passBoth;
//Write the message into the page
var el = document.getElementByid( ' answer') ;
el.textContent = msg;
```
  >using logical OR `||` or Not  `!`
  ```
//Check wh ether user passed one of the two rounds. store result in vari able
var minPass = ((scorel >= passl) I I (score2 >= pass2));
//Create message
var msg = 'Resit required: ' + !(minPass);
//Write the message into the page
var el = document.getElementByld('answer');
el .textContent = msg;
```
  >using if statement:
  ```
function congratulate() { 
msg += ' Congratulations! ' ;
} 
if (score>= 50) { II If score is 50 or more
congratulate();
msg += 'Proceed to the next round . ' ;
var el = document.getElementByld('answer' ) ;
el.innerHTML = msg;
```
>using if else statement:
 ```
 if (score >= pass) {
msg = 'Congratulations, you passed!';
} else {
msg = 'Have another go!';
}
var el = document .getElementByld('answer');
el .textContent = msg;
```
