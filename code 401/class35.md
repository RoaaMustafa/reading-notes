# Implementation: Graphs
![The source](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)
## What is graph?

A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.


## common terminology used when working with Graphs:

+ **Vertex** - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
+ **Edge** - An edge is a connection between two nodes.
+ **Neighbor** - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
+ **Degree** - The degree of a vertex is the number of edges connected to that vertex.

## Undirected Graphs

An Undirected Graph is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.


 There are no “directions” given to point to specific vertices. The connection is bi-directional.
 
![Undirected](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/UndirectedGraph.PNG)

## Directed Graphs (Digraph)
A Directed Graph also called a Digraph is a graph where every edge is directed.

Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

![Directed](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DirectedGraph.PNG)

## Complete Graphs
A complete graph is when all nodes are connected to all other nodes.

![Complete](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/CompleteGraph.PNG)


### Connected
A connected graph is graph that has all of vertices/nodes have at least one edge.

![Connected](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/ConnectedGraph.PNG)

### Disconnected
A disconnected graph is a graph where some vertices may not have edges.
1[Disconnected](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DisconnectedGraph.PNG)

## Real World Uses of Graphs
Graphs are extremely popular when it comes to it’s uses. Here are just a few examples of graphs in use:

+ GPS and Mapping
+ Driving Directions
+ Social Networks
+ Airline Traffic
+ Netflix uses graphs for suggestions of products
