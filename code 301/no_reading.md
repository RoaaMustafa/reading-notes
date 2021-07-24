# no raeding
the most important thing that i learned
NODE.JS
What is node.js?
Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.
In your own words, what is Chrome’s V8 JavaScript Engine?
The V8 Engine is the javascript open source engine that runs on google chrome .
It also runs on other chromium based browsers .
It was enhanced by :
file system API .
HTTP library .
number of operating system related utilities .
What is npm?
A package manager that comes with nodeJS .

We can install a package using the command npm install the name of the package .

We can also use npm to install packages locally.

What command would you type to install a library/package called ‘jshint’?
npm install jshint

What is node used for?
When working with any modern JS library you are expected to be familiar with node .
most of modern libraries depends on node and npm .
Node allows us to start JS projects on a server .
Node is particularly suited to building applications that require some form of real-time interaction or collaboration — for example, chat sites, or apps and also it is suitable for building API’s .
APIs
What does REST stand for?
Representational State Transfer (REST) as an architectural approach to designing web services .
REST APIs are designed around resources .
What is an identifer of a resource?
A resource has an identifier, which is a URI that uniquely identifies that resource .
REST APIs use a stateless request model .
POST requests should be based on nouns .
GET retrieves a representation of the resource at the specified URI. The body of the response message contains the details of the requested resource.
POST creates a new resource at the specified URI. The body of the request message provides the details of the new resource. Note that POST can also be used to trigger operations that don’t actually create resources.
PUT either creates or replaces the resource at the specified URI. The body of the request message specifies the resource to be created or updated.
PATCH performs a partial update of a resource. The request body specifies the set of changes to apply to the resource.
DELETE removes the resource at the specified URL.
Filter and paginate data (Links to an external site.)
the API can allow passing a filter in the query string of the URI Which will increase the efficency .
Also consider imposing an upper limit on the number of items returned .
Give all optional parameters in query strings meaningful defaults.
