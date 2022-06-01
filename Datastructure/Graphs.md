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
