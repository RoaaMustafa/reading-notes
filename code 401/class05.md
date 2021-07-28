## Read 05
### Implementation: Linked Lists

What is a Linked List? 

A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.


Linked List -
A data structure that contains nodes that links/points to the next node in the list.


Terminologies:

Singly - 
Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.

Doubly - 
Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

Node - 
Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.

Next -
Each node contains a property called Next. This property contains the reference to the next node.

Head -
The Head is a reference of type Node to the first node in a linked list.

Current -
The Current is a reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list.


Implementations: There are usually two forms of linked list:

Without a dummy head (refer to the top singly linked list in the following diagram), or
With a dummy head (bottom one). Dummy headers are often used because they help with the implementation.

## creation linked list
``` class Node:
    def __init__(self, dataval=None):
        self.dataval = dataval
        self.nextval = None

class SLinkedList:
    def __init__(self):
        self.headval = None

list1 = SLinkedList()
list1.headval = Node("Mon")
e2 = Node("Tue")
e3 = Node("Wed")
# Link first Node to second node
list1.headval.nextval = e2

# Link second Node to third node
e2.nextval = e3
```



![linked-list](https://i.ytimg.com/vi/HNCMqOVj-VA/maxresdefault.jpg)


![memory-allocation](https://miro.medium.com/max/2400/1*G43FVT5xJ1n1QDKVNZUxXQ.jpeg)


 ###  Big O equations to remember are O(1) and O(n).
 
 + An O(1) function takes constant time, which is to say that it doesn’t matter how many elements we have, or how huge our input is: it’ll always take the same amount of time and memory to run our algorithm.
 + 
 + An O(n) function is linear, which means that as our input grows (from ten numbers, to ten thousand, to ten million), the space and time that we need to run that algorithm grows linearly.
 

![bbigO](https://miro.medium.com/max/2400/1*FC0XX0-9Vx7yCS0dTS2Zrw.jpeg)



![comparassion](https://miro.medium.com/max/2400/1*cUehR5S18XSoVLaPNfNzlA.jpeg)
