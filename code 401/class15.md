# [Tree](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)
### Binary Trees, Binary Search Trees, and K-ary Trees.

### Common Terminology
**Node** - A Tree node is a component which may contain it’s own values, and references to other nodes

**Root** - The root is the node at the beginning of the tree

**K** - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.

**Left** - A reference to one child node, in a binary tree

**Right** - A reference to the other child node, in a binary tree

**Edge** - The edge in a tree is the link between a parent and child node

**Leaf** - A leaf is a node that does not have any children

**Height** - The height of a tree is the number of edges from the root to the furthest leaf

### Traversals


An important aspect of trees--->  is how to traverse them. 

**Traversing a tree** : allows us to search for a node, print out the contents of a tree, and much more! There are two categories of traversals when it comes to trees:

+ Depth First

+ Breadth First

#### Depth First

Depth first traversal --> is where we prioritize going through the depth (height) of the tree first. 

There are multiple ways to carry out depth **first traversal** .
Each method changes the order in which we search/print the root. 

##### Here are three methods for depth first traversal:

+ **Pre-order:** root >> left >> right
+ **In-order:** left >> root >> right
+ **Post-order:** left >> right >> root

#### Breadth First

Breadth first--> traversal iterates through the tree by going through each level of the tree node-by-node.

Breadth first traversal--->  uses a **queue** (instead of the call stack via recursion) to traverse the width/breadth of the tree. 


#### Binary Tree Vs K-ary Trees

Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our left and right children).

##### K-ary Trees

If Nodes are able have more than 2 child nodes--> we call the tree that contains them a K-ary Tree. 

We use K to refer to the maximum number of children that each Node is able to have.

**Breadth First Traversal**

Traversing a K-ary tree requires a similar approach to the breadth first traversal.

We are still pushing nodes into a queue, but we are now moving down a list of children of length k, 

instead of checking for the presence of a left and a right child.


![Traversing a K-ary tree](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/KaryTree1.png)


#### Adding a node

One strategy for adding a new node to a binary tree is to fill all “child” spots from the top down.

Leverage the use of breadth first traversal.

The first node that does not have all it’s children filled, and insert the new node as a child. 

We fill the child slots from left to right.

##### Big O

The **Big O time** complexity for inserting a new node is **O(n)**. 
Searching for a specific node will also be O(n). Because of the lack of organizational structure in a Binary Tree.
The worst case for most operations will involve traversing the entire tree. 
If we assume that a tree has n nodes, then in the worst case we will have to look at n items, hence the O(n) complexity.


The **Big O space** complexity for a node insertion using breadth first insertion will be **O(w)** , where w is the largest width of the tree. For example, in the above tree, w is 4.

