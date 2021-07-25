# Read 01

### [Pain and Suffering](https://codefellows.github.io/code-401-python-guide/curriculum/class-01/notes/pain_suffering)

+ All growth comes with some degree of pain, as it pulls you out of your comfort zone. The greater the growth, the greater the pain.

+ As you experience pain, seek the remedy! Ask questions that bridge the gap between what you know and what you need to be able to do.

+ You’re here because you chose to invest in a different life. A better life.

### [Beginners Guide to Big O](https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation)

Big O notation is used in Computer Science to describe the performance or complexity of an algorithm. 

Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.

+ **O(1)** describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.

+ **O(N)** describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set.

+ **O(N2)** represents an algorithm whose performance is directly proportional to the square of the size of the input data set. This is common with algorithms that involve nested iterations over the data set.

+ **O(2N)** denotes an algorithm whose growth doubles with each additon to the input data set. The growth curve of an O(2N) function is exponential - starting off very shallow, then rising meteorically.

+ **Logarithms**
This type of algorithm is described as O(log N). 

The iterative halving of data sets described in the binary search example produces a growth curve that peaks at the beginning and slowly

flattens out as the size of the data sets increase e.g. an input data set containing 10 items takes one second to complete, a data set 

containing 100 items takes two seconds, and a data set containing 1000 items will take three seconds. Doubling the size of the input data set has little effect on 
its growth as after a single iteration of the algorithm the data set will be halved and therefore on a par with an input data set half the size. 

This makes algorithms like binary search extremely efficient when dealing with large data sets.
