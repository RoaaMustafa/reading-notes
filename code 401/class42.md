#  Pythonisms




## [Dunder Methods](https://dbader.org/blog/python-dunder-methods)


Dunder or magic methods in Python are the methods having two prefix and suffix underscores in the method name. 

Dunder here means “Double Under (Underscores)”. 

These are commonly used for operator overloading. Few examples for magic methods are: 
`__init__`, `__add__`, `__len__`, `__repr__` etc.


## [Iterators](https://dbader.org/blog/python-iterators)


Iterator in python is an object that is used to iterate over iterable objects like lists, **tuples**, **dicts**, and **sets**. 

The iterator object is initialized using the `iter()` method. 

It uses the `next()` method for iteration.

`__iter(iterable)__` method that is called for the initialization of an iterator. 

This returns an iterator object next ( `__next__` in Python 3) The next method returns the next value for the iterable. 

When we use a for loop to traverse any iterable object, internally it uses the `iter()` method to get an iterator object which further uses `next()` method to iterate over. 

This method raises a StopIteration to signal the end of the iteration.


## [Generators](https://dbader.org/blog/python-generators)


Generator functions are syntactic sugar for writing objects that support the iterator protocol.

Generators abstract away much of the boilerplate code needed when writing class-based iterators.

The yield statement allows you to temporarily suspend execution of a generator function and to pass back values from it. 

Generators start raising StopIteration exceptions after control flow leaves the generator function by any means other than a yield statement.


