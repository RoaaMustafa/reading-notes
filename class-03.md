# Read03 HTML Lists, Control Flow with JS, and the CSS Box Mode
## Java script
+ Using quotes inside a string using ` document.getElementByld` and `elTitle.innerHTML` 
```
var title;
title= "Molly's Special Offers" ;
var elTitle = document.getElementByld('title') ;
elTitle.innerHTML =title;
```
 + using a variable to store a boolean :   
 
  ```  
 var elShip = document .getElementByid('shipping');
 elShip.className = shipping ;
```


+ comparing two expressions: 
```
//Check if scores are higher than current high scores
var comparison= (score!+ score2) > (highScorel + highScore2);
//Write the message into the page
var el = document.getElementByid( 'answer');
el .textContent ='New high score:'+ comparison;
```
  + or by using logical And &&:
```
//Check whether user passed both rounds , store result in variable
var passBoth = (scorel >= passl) && (score2 >= pass2);
//Create message
var msg = 'Both rounds passed: ' + passBoth;
//Write the message into the page
var el = document.getElementByid( ' answer') ;
el.textContent = msg;
```
  + using logical OR `||` or Not  `!`
  ```
//Check wh ether user passed one of the two rounds. store result in vari able
var minPass = ((scorel >= passl) I I (score2 >= pass2));
//Create message
var msg = 'Resit required: ' + !(minPass);
//Write the message into the page
var el = document.getElementByld('answer');
el .textContent = msg;
```
  + using if statement:
  ```
  

