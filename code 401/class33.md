# Authentication & Production Server

## JSON Web Tokens

### What is JSON Web Token?
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. 

### When should you use JSON Web Tokens?

+ Authorization: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token.

+ Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties.

### What is the JSON Web Token structure?

+ Header: consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.
+ Payload:  contains the claims. Claims are statements about an entity (typically, the user) and additional data. 
       +  Registered claims: These are a set of predefined claims which are not mandatory but recommended, to provide a set of useful, interoperable claims.
       +  Public claims: These can be defined at will by those using JWTs. 
       +  Private claims: These are the custom claims created to share information between parties that agree on using them and are neither registered or public claims.
+ Signature: To create the signature part you have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.


### How do JSON Web Tokens work?


In authentication, when the user successfully logs in using their credentials, a JSON Web Token will be returned. Since tokens are credentials, great care must be taken to prevent security issues. In general, you should not keep tokens longer than required.



## DRF JWT Authentication

### How to Use JWT Authentication with Django REST Framework?

**JWT** stand for JSON Web Token and it is an authentication strategy used by client/server applications where the client is a Web application using JavaScript and some frontend framework like Angular, React or VueJS.

**How JWT Works?**
The JWT is just an authorization token that should be included in all requests: 
```
curl http://127.0.0.1:8000/hello/ -H 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNTQzODI4NDMxLCJqdGkiOiI3ZjU5OTdiNzE1MGQ0NjU3OWRjMmI0OTE2NzA5N2U3YiIsInVzZXJfaWQiOjF9.Ju70kdcaHKn1Qaz8H42zrOYk0Jx9kIckTn9Xx7vhikY'
```


#### The JWT is acquired by exchanging an username + password for an access token and an refresh token.

+ The access token is usually short-lived (expires in 5 min or so, can be customized though).

+ The refresh token lives a little bit longer (expires in 24 hours, also customizable). It is comparable to an authentication session. After it expires, you need a full login with username + password again.


### Why is that?

It’s a security feature and also it’s because the JWT holds a little bit more information. If you look closely the example I gave above, you will see the token is composed by three parts:

`xxxxx.yyyyy.zzzzz`

### Installation & Setup

`pip install djangorestframework_simplejwt`

#### settings.py
```
REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': [
        'rest_framework_simplejwt.authentication.JWTAuthentication',
    ],
}
```
#### urls.py
```
from django.urls import path
from rest_framework_simplejwt import views as jwt_views

urlpatterns = [
    # Your URLs...
    path('api/token/', jwt_views.TokenObtainPairView.as_view(), name='token_obtain_pair'),
    path('api/token/refresh/', jwt_views.TokenRefreshView.as_view(), name='token_refresh'),
]

```
Obtain Token
First step is to authenticate and obtain the token. The endpoint is /api/token/ and it only accepts POST requests.

`http post http://127.0.0.1:8000/api/token/ username=vitor password=123`

Refresh Token
To get a new access token, you should use the refresh token endpoint /api/token/refresh/ posting the refresh token:


```
http post http://127.0.0.1:8000/api/token/refresh/ refresh=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4cCI6MTU0NTMwODIyMiwianRpIjoiNzAyOGFlNjc0ZTdjNDZlMDlmMzUwYjg3MjU1NGUxODQiLCJ1c2VyX2lkIjoxfQ.Md8AO3dDrQBvWYWeZsd_A1J39z6b6HEwWIUZ7ilOiPE
```


#### What’s The Point of The Refresh Token?


At first glance the refresh token may look pointless, but in fact it is necessary to make sure the user still have the correct permissions. If your access token have a long expire time, it may take longer to update the information associated with the token. That’s because the authentication check is done by cryptographic means, instead of querying the database and verifying the data. So some information is sort of cached.

## Django Runserver Is Not Your Production Server


### Django Runserver Is Not Your Production Server

You’ve been running your app locally with `python manage.py runserver`.
That’s a fine command, built for development convenience, but it’s not meant to be used as part of a production setup.

`runserver `is not guaranteed to be performant (it’s very slow), and it hasn’t been built with security concerns in mind. Not a good fit for production use.

### So, what’s the right way to approach this?

+ A Production Stack: A production setup usually consists of multiple components, each designed and built to be really good at one specific thing. They are fast, reliable and very focused.


 ### How Does Django Fit In?
 
 Your Django app does not actually run as you would think a server would - waiting for requests and reacting to them. Your project provides a uwsgi.py file, which contains a function to be called by the application server. This function gets a Python object representing the incoming request.

This function calls your code, and produces a response object which is passed to the WSGI server. There the response is translated into a HTTP response and is passed back to the web server, which finally delivers it to the user.
