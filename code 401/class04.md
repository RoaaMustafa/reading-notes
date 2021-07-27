## Read 04
### [lasses and Objects](https://www.learnpython.org/en/Classes_and_Objects)

Python is an object oriented programming language.

Almost everything in Python is an object, with its properties and methods.

A Class is like an object constructor, or a "blueprint" for creating objects.

`
Create a class named MyClass, with a property named x:
class MyClass:
  x = 5

Now we can use the class named MyClass to create objects:

p1 = MyClass()
print(p1.x)`

The `__init__()` Function The examples above are classes and objects in their simplest form, and are not really useful in real life applications.

To understand the meaning of classes we have to understand the built-in `__init__() `function.

All classes have a function called __init__(), which is always executed when the class is being initiated.

Use the `__init__()` function to assign values to object properties, or other operations that are necessary to do when the object is being created:

Create a class named Person, use the `__init__()` function to assign values for name and age:

`class Person:
  def `__init__`(self, name, age):
    self.name = name
    self.age = age

p1 = Person("John", 36)

print(p1.name)
print(p1.age)`

### [Thinking Recursively in Python:](https://realpython.com/python-thinking-recursively/)

Along the way on your programming journey, there are a few milestones that you need to conquer to advance ahead. 
For example, getting comfortable with classes, understanding pointers, master the art of functionalizing your code, 
and so on. One of the trickest programming concepts to learn for newcomers and master for those who have been programming for a while is recursion.

Steps to train your mind to think recursively:

1-Use the iterable-approach first.
2-Extract the parameters of your function.
3-Deduct minimal problem instance.
4-Add the solution to the minimal problem instance.
5-Expand your function.


![image](https://files.realpython.com/media/state_3.3e8a68c4fde5.png)

### [Pytest Fixtures and Coverage](https://www.linuxjournal.com/content/python-testing-pytest-fixtures-and-coverage)

What Does Fixtures Mean? Fixtures, in the context of insurance, are movable or personal property attached to an immovable property that they become a part of the immovable or real property and are covered under a real estate insurance policy.

Insuranceopedia Explains Fixtures Fixtures are said to form part of the immovable when they are attached or affixed permanently, such as when they are embedded, rooted, or permanently attached with cement, glue, nails, screws, bolts, or plaster. There are four types of fixtures, namely:

Agricultural fixtures, or those attached for the purpose of farming; Domestic fixtures, or those attached to a home in order to make it more livable; Ornamental fixtures, or those attached to a property in order to make it more attractive; and Trade fixtures, or those necessary in the conduct of business in the real property. To determine whether a personal property is a fixture or not, the following shall be considered:

Method of attachment; Adaptability of use; Intent of the buyer and the seller in a contract of sale; Agreement of the parties; and Relationship of the parties.

Example :

`def only_odd_mul(x, y):
   if x%2 and y%2:
       return x * y
   else:
       raise NoEvenNumbersHereException(f'{x} and/or {y}
 ↪not odd')`
 
 Test:
` def test_odd_numbers():
   assert only_odd_mul(3, 5) == 15`
 `  
   # content of test_sample.py
def inc(x):
    return x + 1


def test_answer():
    assert inc(3) == 5`
 
