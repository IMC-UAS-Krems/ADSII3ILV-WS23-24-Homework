# Homework 5 - Description

The goal of this homework is to keep practising on Graphs.

# Task 1

Create a `ugraph.py` file in the `session.05` folder and provide an implementation of a **weighted** undirected graph as an adjacency matrix. Call the class `UndirectedGraph`.
 
Create a `dgraph.py` file in the `session.05` folder and provide an implementation of a **weighted** directed graph as an adjacency matrix. Call the class `DirectedGraph`.

Both graph implementations should offer the following API:

```
    def add_vertex(key):
        """ 
            Add a new vertex containing the given key, if no other vertices contain that key.
            Do nothing otherwise.
        """
        pass

    def remove_vertex(key):
        """ 
            Remove the vertex containing the given key, if it exists.
            Do nothing otherwise.
        """
        pass

    def contain_vertex(key):
        """
            Return true if a vertex with the given key exists, false, otherwise.
        """
        pass
        
    def add_edge(key_1, key_2, weight):
        """
            Add an edge between the vertices containing key_1 and key_2 if they exist with the given weight.
            Do nothing otherwise. If an edge already exists, raise an AssertionError("Edge already exists").
        """
        
        pass

    def remove_edge(key_1, key_2):
        """
            Remove the edge between the vertices containing key_1 and key_2 if the edge and the vertices exist.
            Do nothing otherwise.
        """
        pass
```

`UndirectedGraph` should also provide a method: `is_connected()`, which returns `True` _iff_ the undirected graph is connected.

`DirectedGraph` should provide two methods:

- `is_strongly_connected()` which returns `True` _iff_ the directed graph is strongly connected (i.e., connected must consider the direction of the edges).
- `is_weakly_connected()` which returns `True` _iff_ the directed graph is weakly connected (i.e., connected without considering the direction of the edges). 

> Note: Assume only integers are stored as keys. No duplicate keys are allowed.

> Hint: You can leverage graph traversal algorithms to check for connectivity


# Task 2:

Create a `gutils.py` file in the `session.05` folder and provide an implementation of Prim's and Dijkstra's algorithms. Those module-level methods take a graph (either UndirectedGraph or DirectedGraph, depending on the algorithm) and a source node and return a tree.

Use the following names for the methods:

```
def prim(g, u):
  """ 
    Returns a Minimum spanning tree rooted in u. u must be a node of g.
  """

def dijkstra(g, u)"
    """
        Returns the tree rooted in u containing the minimum paths from u to all the other nodes (reachable from u) in g. u must be a node of g.
    """
```

## Tests

Implement enough unit tests to achieve 100% of statement and branch coverage.
