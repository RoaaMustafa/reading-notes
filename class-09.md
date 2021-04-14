# Read: 09 - Forms and Events
## HTML
### Forms
+ **WHAT?** a printed document that contains spaces for you to fill in information.IN HTML :elements that allow you to collect information from visitors to your site.
+ **Why Forms?** 
    +  enabling users to search.
    +  also allow users to perform other functions online.
+  **types of form controls** can use to collect information from visitors to your site.
    1. ADDING TEXT:Text input (single-line),Password input,Text area (multi-line)
    2. Making Choices: Radio buttons,Checkboxes,Drop-down boxes.
    3. Submitting Forms:Submit buttons,Image buttons.
    4. Uploading Files: File upload.
+ **How Forms Work?** 
  1. A user fills in a form and then presses a button to submit the information to the server.
  2. The name of each form control is sent to the server along with the value the user enters or selects.
  3. The server processes the information using a programming language such as PHP, C#, VB.net, or Java. It may also store the information in a database.
  4. The server creates a new page to send back to the browser based on the information received.
+  `username(Name)=Ivy(value)`
+  **Form Structure**
   + `<form>`:This element should always carry the action attribute and will usually have a method and id attribute too.
   + `action` : Every `<form>` element requires an action attribute. Its value is the URL for the page on the server that will receive the information in the form when it is               submitted.
   + `method `: get or post.
      + get: the values from the form are added to the end of the URL specified in the action attribute.
      + post: values are sent in what are known as HTTP headers. 
          1. allows users to upload a file
          2. is very long
          3. contains sensitive data (e.g. passwords)
          4. adds information to, or deletes information from, a database

   + `id`: the value is used to identify the form distinctly from other elements on the page
   + **Text input** 
      + `<input>` : element is used to create several different form controls.
      + `type="text"` : attribute   When the type attribute has a value of text, it creates a singleline text input.
      + `name `:attribute  When users enter information into a form.
      + `size `: attribute to indicate the width of the text input
      + `maxlength`: attribute to limit the number of characters a user may enter into the text field.
  + **Password Input**
      + `<input>`: `type="password"` : attribute has a value of password it creates a text box that acts just like a single-line text input, except the characters are blocked                out.
      + `name`: attribute indicates the name of the password input/
      + `size, maxlength`: attributes like the the single-line text input.
  + **Text Area**
      + `<textarea>` element is used to create a mutli-line text input.
      + `type="radio"` Radio buttons allow users to pick just one of a number of options.` name`,` value`, `checked`
      + Check box: `type="checkbox"` ,`name`,`value`,` checked`
  + **Drop Down List Box** 
      1. `<select>` element is used to create a drop down list box. It contains two or more <option> elements.
      2.` name` attribute indicates the name of the form control being sent to the server,
      3. `value `attribute to indicate the value that is sent to the server along with the name of the control if this option is selected.
      4. `select `attribute can beused to indicate the option that
  


## CSS
### Lists, Tables & Forms
Learned :
  1. Specify the type of bullet point or numbering on lists
  2. Add borders and backgrounds to table cells
  3. Control the appearance of form controls
+ 



## JS
### Events
