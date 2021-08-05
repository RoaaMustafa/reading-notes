## Implementation: Stacks and Queues
### [Stacks and Queues What is a Stack](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)

**WHAT is STACK?**
A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

+ **Push** - Nodes or items that are put into the stack are pushed
+ **Pop** - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
+ **Top** - This is the top of the stack.
+ **Peek** - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
+ **IsEmpty** - returns true when stack is empty otherwise returns false.

+ **FILO** First In Last Out :first item added in the stack will be the last item popped out of the stack.
+ **LIFO** Last In First Out : ast item added to the stack will be the first item popped out of the stack.

+ **Push O(1)** : alaways push value in a stack take O(1) because it takes the same amount of time no matter how many Nodes (n) you have in the stack.
```
ALOGORITHM push(value)
   node = new Node(value)
   node.next <-- Top
   top <-- Node
```
+ **Pop O(1)** : 
  ```
    ALGORITHM pop()

      Node temp <-- top
      top <-- top.next
      temp.next <-- null
      return temp.value
  ```
  
+ Peek O(1) :
```
   ALGORITHM peek()
     // INPUT <-- none
     // OUTPUT <-- value of top Node in stack
     // EXCEPTION if stack is empty

     return top.value
```
+ **IsEmpty O(1)** :
```

ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean

return top = NULL
```
