## Readings: Game of Greed 1

### [How to use Random Module](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)

#### **What ?**

The random module provides access to functions that support many operations. Perhaps the most important thing is that it allows you to generate random numbers.

#### **When ?**

We want the computer to pick a random number in a given range Pick a random element from a list, pick a random card from a deck, flip a coin etc. 

#### **Random functions :**

The Random module contains some very useful functions.

#### **Randint :** 
If we wanted a random integer, we can use the randint function Randint accepts two parameters: a lowest and a highest number. Generate integers between 1,5. The first value should be less than the second.


```mport random
print random.randint(0, 5)
This will output either 1, 2, 3, 4 or 5.
```

#### **Random**

If you want a larger number, you can multiply it.

For example, a random number between 0 and 100:

```import random
random.random() * 100
```


#### **Choice**
Generate a random value from the sequence sequence.
`random.choice( ['red', 'black', 'green'] ).`
The choice function can often be used for choosing a random element from a list.

```import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)
```


#### **Shuffle**
The shuffle function, shuffles the elements in list in place, so they are in a random order.

```from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
Output:
# print x  gives  [[9], [2], [7], [0], [4], [5], [3], [1], [8], [6]]
# of course your results will vary
```

**Randrange**
Generate a randomly selected element from range(start, stop, step)

```random.randrange(start, stop[, step])
import random
for i in range(3):
    print random.randrange(0, 101, 5)
    
 ```
    
### [What is Risk Analysis](https://www.edureka.co/blog/risk-analysis-in-software-testing/)

#### **Why use Risk Analysis?** 
In any software, using risk analysis at the beginning of a project highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks. When a test plan has been created, risks involved in testing the product are to be taken into consideration along with the possibility of the damage they may cause to your software along with solutions.

1- The time that you allocated for testing

2- A defect leakage due to the complexity or size of the application

3- Urgency from the clients to deliver the project

4- Incomplete requirements

#### **Risk Identification**

Risk Identification : come from your company or your customer,
Testing Risks : come from the platform you are working on
Premature Release Risk : come from releasing unsatisfactory or untested software
Software Risks : come from the software development process.

#### **Risk Assessment**

+ There are three perspectives of Risk Assessment:
   +Effect
   +Cause
   +Likelihood
   
 #### **How to perform Risk Analysis?**

There are three steps:
  1-Searching the risk

  2-Analyzing the impact of each individual risk

  3-Measures for the risk identified
  
  
  #### **Dependency Injection: what it is ???**

Dependency or dependent means relying on something for support

**Dependency Injection:** is a technique whereby one object (or static method) supplies the dependencies of another object. A dependency is an object that can be used (a service).

**Dependency Injection :** transferring the task of creating the object to someone else and directly using the dependency

#### **three types of dependency injection:**

**constructor injection:** the dependencies are provided through a class constructor.

**setter injection :** the client exposes a setter method that the injector uses to inject the dependency.

**interface injection :** the dependency provides an injector method that will inject the dependency into any client passed to it. Clients must implement an interface that exposes a setter method that accepts the dependency.

**dependency injection’s responsibility to:**

  +Create the objects

  +Know which classes require those objects
