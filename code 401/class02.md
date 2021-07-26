## Read 02
### [In Tests We Trust - TDD with Python](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)

In Tests We Trust — TDD with Python Unit tests are some pieces of code to exercise the input,the output and the behaviour of your code.

example : (Links to an external site.)

we wand to get female or male depand on name , from api lets write unit tests , we dont hace code to test ;Important aspects about the unit test.

Unit tests: Unit tests are some pieces of code to exercise the input, the output and the behaviour of your code. You can write them anytime you want.


### [If name equals main](https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/)

If the python interpreter is running that module (the source file) as the main program, it sets the special name variable to have a value “main”. If this file is being imported from another module, name will be set to the module’s name. Module’s name is available as value to name global variable.

A module is a file containing Python definitions and statements. The file name is the module name with the suffix .py appended.

When we execute file as command to the python interpreter,

python script.py


### [Recursion](https://www.geeksforgeeks.org/recursion/)

The process in which a function calls itself directly or indirectly

enables solving certain problems easily

In recursive functions it is important to use base condition.

the solution to the base case is provided and the solution of the bigger problem is expressed in terms of smaller problems.
Example

int fact(int n) { if (n < = 1) // base case return 1; else return n*fact(n-1) }}

If the base case is not reached or not defined, then the stack overflow problem may arise.

There are two types of recursion (direct & indirect)

Recursion provides a clean and simple way to write code.
