# Read: 06 - JS Object Literals; The DOM
## JS book
### Object Literals
+ **WHAT IS AN OBJECT?**
   Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on    new names.
   + If a **variable** is part of an object, it is called a **property**
   + If a **function** is part of an object, it is called a **method**.
   + The value of a method is always a function.
   + An object cannot have two keys with the same name.
+ **How to creat an obect?**
   + one of the metods is : **Literal notation**
   + Accessing an object used : dot notation or sqare brackets
   +  you can use the object name followed by the method `name.hotel .checkAvailability()`
   
### The Document Object Model (DOM)
+ **What is DOM?**
+  specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.
+  The DOM is neither part of HTML, nor part of JavaScript; it is a separate set of rules.
+  (the DOM tree) is made of **objects**.
+  DOM an Application Programming Interface **(API)**.
+  As a browser loads a web page, it creates a model of that page. The model is called a **DOM tree**, and it is stored in the browsers' memory. It consists of four main types of        nodes.
+  Every element, attribute, and piece of text in the HTML is represented by its own **DOM node**.
1. Each node is an object with methods and properties.
2.  Scripts access and update this DOM tree (not the source HTML file).
3.  Any changes made to the DOM tree are reflected in the browser.
+ **WORKING WITH THE DOM TREE**
   1. Locate the node that represents the element you want to work with.
   2. Use its text content, child elements, and attributes.
   + **Step1:ACCESS THE ELEMENTS**
      + select an individual element: `getElementByld ()` ,`querySe1ector ()`
      + select multiple elements: `getElementsByClassName()`, `getElementsByTagName()`, `querySelectorAll()`
      + move from one element node to a related element node:
         1. `parentNode`: Selects the parent of the current element node (which will return just one element). 
         2. `previousSibl ing / nextSibl ing`: Selects the previous or next sibling from the DOM tree.
         3. `firstChild / lastChild` :Select the first or last child of the current element.
   + The terms elements and element nodes are used interchangeably but when people say the DOM is working with an element, it is actually working with a node that represents          that element.      
   + **Step2: WORK WITH THOSE ELEMENTS**
      + ACCESS OR UPDATE ATTRIBUTE VALUES:
         1. Select the `<li>` element
         2. Use the `firstChild` property to get the text node
         3. Use the text node's only property **(nodeValue)** to get the text from the element
            `nodeValue` This property lets you access or update contents of a text node.
       + WORK WITH HTML CONTENT
          1. **innerHTML** : access to child elements and text content 
          2. **extContent**: just the text content 
          3. create new nodes, add nodes to a tree, and remove nodes from a tree: **create Element()**,**createTextNode()**, **appendChild () / removeChild ()**; This is called              DOM manipulation.
       + ACCESS OR UPDATE ATTRIBUTE VALUES
          1. **className /id** :Lets you get or update the value of the class and id attributes.
          2. **hasAttribute()**: checks if an attribute exists.
          3. **getAttribute()**:gets its value.
          4. **setAttribute()**:updates the value.
          5. **removeAttribute()**:removes an attribute.
          
    + **DOM queries** :To find element in DOM tree.
    + **caching the selection** : store the location of the element in a variable
    + **Nodelists** :they are a type of object called a collection.
    + **live Nodelist**: is updated at the same time, faster to generate
    + **static Nodelist** : not updated to reflect the changes made by the script.
    + four different DOM queries that all return a Nodelist.
       1. getElementsByTagName('hl') :returns one element
       2. getElementsByTagName('li'): returns four elements
       3. getElementsByClassName('hot'): contains only three of the `<li>` elements
       4. querySelectorA11('li[id]'): returns four elements.
   + to select an element from a Nodelist:
      + THE `item()` METHOD: return an individual node from the Node list.    
      + Array syntax

       
    
