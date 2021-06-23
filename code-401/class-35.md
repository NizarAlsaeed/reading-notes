
# Graphs

## Directed vs Undirected
### Undirected Graphs
An Undirected Graph is a graph where each edge is undirected or bi-directional.
### Directed Graphs (Digraph)
A Directed Graph also called a Digraph is a graph where every edge is directed.
## Complete vs Connected vs Disconnected
### Complete Graphs
A complete graph is when all nodes are connected to all other nodes.
### Connected
A connected graph is graph that has all of vertices/nodes have at least one edge.
### Disconnected
A disconnected graph is a graph where some vertices may not have edges.
## Acyclic vs Cyclic
### Acyclic Graph
An acyclic graph is a directed graph without cycles.
### Cyclic Graphs
A Cyclic graph is a graph that has cycles.
A cycle is defined as a path of a positive length that starts and ends at the same vertex.
## Graph Representation
We represent graphs through:
### Adjacency Matrix
An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix

Each Row and column represents each vertex of the data structure. The elements of both the column and the row must add up to 1
if there is an edge that connects the two, or zero if there isn’t a connection.
### Adjacency List
An adjacency list is the most common way to represent graphs.

An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.
## Weighted Graphs
A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights.
## Traversals
### Breadth First
 The breadth-first traversal of a graph is like that of a tree, with the exception that graphs can have cycles.
 we need to have some way to keep track of whether a vertex has been “visited” before
### Depth First
The algorithm for a depth first traversal is as follows:

1. Push the root node into the stack
2. Start a while loop while the stack is not empty
3. Peek at the top node in the stack
4. If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.
5. If the top node does not have any unvisited children, Pop that node off the stack
6. repeat until the stack is empty.


