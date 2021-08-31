# Django CRUD and Forms

## Django Forms

Working with forms can be complicated! Developers need to write HTML for the form, validate and properly sanitize entered data on the server (and possibly also in the browser), repost the form with error messages to inform users of any invalid fields, handle the data when it has successfully been submitted, and finally respond to the user in some way to indicate success. 

Django Forms take a lot of the work out of all these steps, by providing a framework that lets you define forms and their fields programmatically, and then use these objects to both generate the form HTML code and handle much of the validation and user interaction.

### HTML Forms

The form is defined in HTML as a collection of elements inside < form >...< /form > tags, containing at least one input element of type="submit".
```
<form action="/team_name_url/" method="post">
    <label for="team_name">Enter name: </label>
    <input id="team_name" type="text" name="name_field" value="Default name for team.">
    <input type="submit" value="OK">
</form>
```


Django's form handling uses all of the same techniques that we learned about in previous tutorials (for displaying information about our models): the view gets a request, performs any actions required including reading data from the models, then generates and returns an HTML page (from a template, into which we pass a context containing the data to be displayed). What makes things more complicated is that the server also needs to be able to process data provided by the user, and redisplay the page if there are any errors.


### The arguments that are common to most fields are listed below (these have sensible default values):

+ required: If True, the field may not be left blank or given a None value. Fields are required by default, so you would set required=False to allow blank values in the form.

+ label: The label to use when rendering the field in HTML. If a label is not specified, Django will create one from the field name by capitalizing the first letter and replacing underscores with spaces (e.g. Renewal date).

+ label_suffix: By default, a colon is displayed after the label (e.g. Renewal date:). This argument allows you to specify a different suffix containing other characters (s).

+ initial: The initial value for the field when the form is displayed.

+ widget: The display widget to use.

+ help_text (as seen in the example above): Additional text that can be displayed in forms to explain how to use the field.

+ + error_messages: A list of error messages for the field. You can override these with your own messages if needed.

+ validators: A list of functions that will be called on the field when it is validated.

+ localize: Enables the localization of form data input (see link for more information).

+ disabled: The field is displayed but its value cannot be edited if this is True. The default is False.


