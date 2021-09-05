# Permissions & Postgresql

## Permissions :permissions determine whether a request should be granted or denied access.

Permission checks will typically use the authentication information in the `request.user` and `request.auth` properties to determine if the incoming request should be permitted.

Permissions are used to grant or deny access for different classes of users to different parts of the API.
 This corresponds to the IsAuthenticated class in REST framework.
This corresponds to the IsAuthenticatedOrReadOnly class in REST framework.

## How permissions are determined

Permissions in REST framework are always defined as a list of permission classes.

 If any permission check fails an exceptions.PermissionDenied or exceptions.NotAuthenticated exception will be raised, and the main body of the view will not run.
 
 When the permissions checks fail either a "403 Forbidden" or a "401 Unauthorized" response will be returned, according to the following rules:

The request was successfully authenticated, but permission was denied. — An HTTP 403 Forbidden response will be returned.
The request was not successfully authenticated, and the highest priority authentication class does not use WWW-Authenticate headers. — An HTTP 403 Forbidden response will be returned.
The request was not successfully authenticated, and the highest priority authentication class does use WWW-Authenticate headers. — An HTTP 401 Unauthorized response, with an appropriate WWW-Authenticate header will be returned.

## Object level permissions

Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.


Object level permissions are run by REST framework's generic views when` .get_object() `is called. As with view level permissions, an exceptions.PermissionDenied exception will be raised if the user is not allowed to act on the given object.

This will either raise a PermissionDenied or NotAuthenticated exception, or simply return if the view has the appropriate permissions.

## Setting the permission policy

The default permission policy may be set globally, using the `DEFAULT_PERMISSION_CLASSES setting`. 


 For example.
```
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}
```

```
If not specified, this setting defaults to allowing unrestricted access:

'DEFAULT_PERMISSION_CLASSES': [
   'rest_framework.permissions.AllowAny',
]
```

## API Reference

### AllowAny

The AllowAny permission class will allow unrestricted access, regardless of if the request was authenticated or unauthenticated.

This permission is not strictly required, since you can achieve the same result by using an empty list or tuple for the permissions setting, but you may find it useful to specify this class because it makes the intention explicit.


### IsAuthenticated


The `IsAuthenticated` permission class will deny permission to any unauthenticated user, and allow permission otherwise.

This permission is suitable if you want your API to only be accessible to registered users.


### IsAdminUser

The `IsAdminUser` permission class will deny permission to any user, unless user.is_staff is True in which case permission will be allowed.

This permission is suitable if you want your API to only be accessible to a subset of trusted administrators.


### IsAuthenticatedOrReadOnly


The `IsAuthenticatedOrReadOnly` will allow authenticated users to perform any request. Requests for unauthorised users will only be permitted if the request method is one of the "safe" methods; `GET`, `HEAD` or OPTIONS.

This permission is suitable if you want to your API to allow read permissions to anonymous users, and only allow write permissions to authenticated users.

## DjangoModelPermissions

This permission class ties into Django's standard` django.contrib.auth` model permissions. 
This permission must only be applied to views that have a `.queryset` property or `get_queryset()` method.


## Custom permissions


To implement a custom permission, override BasePermission and implement either, or both, of the following methods:

.has_permission(self, request, view)
.has_object_permission(self, request, view, obj)


+ `queryset/get_queryset():` Limits the general visibility of existing objects from the database.
   The queryset limits which objects will be listed and which objects can be modified or deleted.
   The `get_queryset()` method can apply different querysets based on the current action.
   
   
+ `permission_classes/get_permissions()`: General permission checks based on the current action, request and targeted object.
    Object level permissions can only be applied to retrieve, modify and deletion actions.
    Permission checks for list and create will be applied to the entire object type.
+ `serializer_class/get_serializer()`: Instance level restrictions that apply to all objects on input and output. 

   The `serializer` may have access to the request context.
   The `get_serializer()` method can apply different serializers based on the current action.
