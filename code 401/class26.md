# Intro to Django

## What is Django?

Django is a high-level Python web framework that enables rapid development of secure and maintainable websites With Django,

you can take Web applications from concept to launch in a matter of hours.

Django takes care of much of the hassle of Web development, so you can focus on writing your app without needing to reinvent the wheel.

It’s free and open source.

## Django helps you write software that is:
Complete
Versatile
Secure
Scalable
Maintainable
Portable


## What does Django code look like?

![djangoo-code](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Introduction/basic-django.png)


+ **URLs**: While it is possible to process requests from every single URL via a single function, it is much more maintainable to write a separate view function to handle each resource. A URL mapper is used to redirect HTTP requests to the appropriate view based on the request URL. The URL mapper can also match particular patterns of strings or digits that appear in a URL and pass these to a view function as data.

+ **View**: A view is a request handler function, which receives HTTP requests and returns HTTP responses. Views access the data needed to satisfy requests via models, and delegate the formatting of the response to templates.

+ **Models**: Models are Python objects that define the structure of an application's data, and provide mechanisms to manage (add, modify, delete) and query records in the database. 

+ **Templates**: A template is a text file defining the structure or layout of a file (such as an HTML page), with placeholders used to represent actual content. A view can dynamically create an HTML page using an HTML template, populating it with data from a model. A template can be used to define the structure of any type of file; it doesn't have to be HTML!
