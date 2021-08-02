## READ 07
### [Python Scope](https://realpython.com/python-scope-legb-rule/)

+ **WHAT?** how variables and names are looked up in your code. It determines the visibility of a variable within the code. 
+ The scope of a name or variable depends on the place in your code where you create that variable. 
+ The Python scope concept is generally presented using a rule known as the LEGB rule (Local, Enclosing, Global, and Built-in scopes).
 #### Understanding Scope
  +  scope of a name defines the area of a program in which you can access that name, such as variables, functions, objects, and so on. 
  +  A name will only be visible to and accessible by the code in its scope. 
  + **WHY?** for avoiding name collisions and unpredictable behaviors.
  #### two general scopes:

     + **Global scope:** The names that you define in this scope are available to all your code.

      + **Local scope:**  The names that you define in this scope are only available or visible to the code within the scope.
      
 + with global names, you’d need to keep all the code in mind at the same time to know what the value of
  a given name is at any time. This was an important side-effect of not having scopes.
  
    ##### assign a value to a name inside a function ----> then that name will have a local Python scope
    ##### assign a value to a name outside of all functions ---> hen that name will have a global Python scope.
  
  #### Names and Scopes in Python:
| Operation                                       | Statement                                       |
| -----------------------------------------------:| -----------------------------------------------:|
| Assignments                                     | 	x = value                                     |
| Import operations                               | import module or from module import name        |
| Function definitions                            | 	def my_func(): ...                            |
| Argument definitions in the context of functions| 	def my_func(arg1, arg2,... argN): ...         |
| Class definitions                               | 	class MyClass: ...                            |

#### Python Scope vs Namespace
   + In Python, the concept of scope is closely related to the concept of the namespace. 
   + Python scopes are implemented as `dictionaries` that map names to objects. 
   + hese dictionaries are commonly called `namespaces`. 
   + They’re stored in a special attribute called `.__dict__.`
   
   ```
       >>> import sys
       >>> sys.__dict__.keys()
      dict_keys(['__name__', '__doc__', '__package__',..., 'argv', 'ps1', 'ps2'])
  ```
  
     + dot notation on the module’s name in the form` module.name`
     + subscription operation on `.__dict__ `in the form module`.__dict__['name']`
     
     ```
         >>> sys.ps1
        '>>> '
        >>> sys.__dict__['ps1']
       '>>> '
    ```
#### Using the LEGB Rule for Python Scope
+ **Local (or function) scope** is the code block or body of any Python function or lambda expression(contains the names that you define inside the function.). 
+ **Enclosing (or nonlocal) scope** is a special scope that only exists for nested functions. If the local scope is an inner or nested function, 
 then the enclosing scope is the scope of the outer or enclosing function(contains the names that you define in the enclosing function. ). 
+ **lobal (or module) scope** is the top-most scope in a Python program, script, or module. (This Python scope contains all of the names that you define at the top level of a program or a module).
+ **Built-in scope** is a special Python scope that’s created or loaded whenever you run a script or open an interactive session. 
 (his scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python). 
 

   
