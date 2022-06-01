# Graphs
A type of non linear data structures that consists of nodes connected with lines called edges.

elements of Graphs:
- **Vertex** --> also called a **node**, is a data object that can have zero or more adjacent vertices.
- **Edge** --> the connection between two nodes.
- **Neighbor** --> the node attached to another through edge.
- **Degree** --> the number of edges connected to that vertex.

## Directed vs Undirected
### Undirected Graphs
it is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.


Example:

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/UndirectedGraph.PNG)

The undirected graph we are looking at has 6 vertices and 7 undirected edges.

Vertices/Nodes = {a,b,c,d,e,f}

Edges = {(a,c),(a,d),(b,c),(b,f),(c,e),(d,e),(e,f)}

### Directed Graphs (Digraph)
A Directed Graph also called a Digraph is a graph where every edge is directed.
- Each node is directed at another node with a specific requirement of what node should be referenced next.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DirectedGraph.PNG)

The directed graph above has six vertices and eight directed edges

Vertices = {a,b,c,d,e,f}

Edges = {(a,c),(b,c),(b,f),(c,e),(d,a),(d,e)(e,c)(e,f)}

## Complete vs Connected vs Disconnected
### Complete Graphs
A complete graph is when all nodes are connected to all other nodes.

### Connected
A connected graph is graph that has all of vertices/nodes have at least one edge.

--> A Tree is a form of a connected graph.

### Disconnected
A disconnected graph is a graph where some vertices may not have edges.


## Acyclic vs Cyclic
### Acyclic Graph
An acyclic graph is a directed graph without cycles.

A cycle is when a node can be traversed through and potentially end up back at itself.

Here is an example of 3 acyclic graphs:

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/threeAcyclic.png)

A directed acyclic graph is also called a DAG. This can also be represented as what we know as a tree.

### Cyclic Graphs
A Cyclic graph is a graph that has cycles.

A cycle is defined as a path of a positive length that starts and ends at the same vertex.

Here is an example of a two different cyclic graph:

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/cyclic.PNG)

## Graph Representation
We represent graphs through:

1. Adjacency Matrix
2. Adjacency List

We will represent the following graph as both an Adjacency Matrix and an Adjacency List:
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/UndirectedGraph.PNG)

### Adjacency Matrix
An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix

Each Row and column represents each vertex of the data structure. The elements of both the column and the row must add up to 1 if there is an edge that connects the two, or zero if there isn’t a connection.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/AdjMatrix.PNG)

A few things to note from the above:
- Looking at the graph we are representing, you can see that Vertex A connects to both Vertex D and Vertex C. To show this, we place a 1 in the position of (a,c) and (a,d).
- We follow this same pattern for the other vertex’s and where they are connected.
- If there is not an edge/connection between the vertex’s, we represent this by placing a 0 in the appropriate point of the matrix.

a sparse graph is when there are very few connections. a dense graph is when there are many connections

Within an adjacency matrix, an undirected graph will always be symmetric. This is not the case for a directed graph.

### Adjacency List
An adjacency list is the most common way to represent graphs.

An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.

Adjacency lists make it easy to view if one vertices connects to another.

This is what an Adjacency List looks like:
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/AdjList.PNG)

Looking at the original graph that we are representing, we can see that Vertex A has an edge to both Vertex C and Vertex D. As a result, we will place both Vertex C and Vertex D in the adjacency list. Just from observation, we can see that we will only place the vertices that are connected in the list. If there is no connection between the vertices, they are not listed.

## Traversals
### Breadth first
```
ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    DECLARE visited <-- new Set()

    breadth.Enqueue(vertex)
    visited.Add(vertex)

    while (breadth is not empty)
        DECLARE front <-- breadth.Dequeue()
        nodes.Add(front)

        for each child in front.Children
            if(child is not visited)
                visited.Add(child)
                breadth.Enqueue(child)

    return nodes;
```

### Depth First
______
[Graphs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)
