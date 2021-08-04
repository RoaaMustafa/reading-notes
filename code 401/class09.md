# Read 09
## Game of Greed 4
## [Dunder Methods](https://dbader.org/blog/python-dunder-methods)
**WHAT?**
+ a set of predefined methods you can use to enrich your classes. 
+ They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.
+ These “dunders” or “special methods” in Python are also sometimes called “magic methods.” 

**WHAY?**
emulate the behavior of built-in types.
#### dunder methods to unlock the following language features:
+ Initialization of new objects
+ Object representation
+ Enable iteration
+ Operator overloading (comparison)
+ Operator overloading (addition)
+ Method invocation
+ Context manager support (with statement)

#### Special Methods and the Python Data Model:
##### Object Initialization: __init__  
To construct account objects from the Account class I need a constructor
##### Object Representation: __str__, __repr__
__repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

__str__: The “informal” or nicely printable string representation of an object. This is for the enduser.
##### Iteration: __len__, __getitem__, __reversed__

__reversed__ To iterate over transactions in reversed order 
##### Operator Overloading for Comparing Accounts: __eq__, __lt__
##### Operator Overloading for Merging Accounts: __add__
##### Callable Python Objects: __call__
##### Context Manager Support and the With Statement: __enter__, __exit__

## [Statistics - Probability](https://www.dataquest.io/blog/basic-statistics-in-python-probability/)

### What is probability?

“What is the chance of an event happening?”,  To calculate the chance of an event happening,
### Z-score
The Z-score is a simple calculation that answers the question,
“Given a data point, how many standard deviations is it away from the mean?” 
The equation below is the Z-score equation.

![z-score-equation](https://www.thoughtco.com/thmb/ZHmzJvAo0WjzWIcqH8USLftKS6o=/735x0/zscore-56a8fa785f9b58b7d0f6e87b.GIF)

