# Homework 4 - Description

The goal of this homework is to implement Graphs as adjacency list and graph traversals.

## Task 1

Create a `graph.py` file in the `session.04` folder and provide a basic implementation of an undirected graph as an adjacency list.

Please refer to the code snipped below. 

> Note: Assume only integers are stored as keys and no duplicate keys are allowed.

```
class Graph():

    def add_vertex(key):
        """ 
            Add a new vertex containing key, if no other vertices contain key.
            Do nothing otherwise.
        """
        pass

    def remove_vertex(key):
        """ 
            Remove the vertex containing key, if it exists.
            Do nothing otherwise.
        """
        pass

    def contain_vertex(key):
        """
            Return true if a vertex with the give key exists; false, otherwise.
        """
        pass
        
    def add_edge(key_1, key_2):
        """
            Add an edge between the vertices containing key_1 and key_2 if they exist. Do nothing otherwise. If an edge already exist, raise an AssertionError("Edge already exists").
        """
        
        pass

    def remove_edge(key_1, key_2):
            """
            Remove the edge between the vertices containing key_1 and key_2 if the edge and the vertices exist. Do nothing otherwise.
            """
        pass
```

## Task 2

Extend your implementation of the graph to implement the following two methods:
    - `breadth_first_search(self, starting_key)`
    - `depth_first_search(self)`

Those methods must print on the console the keys of the vertices that they visit in the order they visit them. 

`depth_first_search` generates a forest, so the expected output takes the form of a nested list (e.g., `[[1,2][3]]`).
When `depth_first_search` "jumps" between nodes because it gets stuck, assume that nodes are visited in the natural order defined by the keys stored in the node.


## Tests

Implement enough unit tests to achieve 100% of statement and branch coverage.
