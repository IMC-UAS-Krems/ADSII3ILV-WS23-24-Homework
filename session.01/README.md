# Exercise Description

Other, more complex data structures exist besides the ones you studied the previous semester. We will study in this semester Trees and Graphs as examples of more complex data structures.

In this exercise/homework, you must implement a generic Tree implementation. 

The implementation must be stored inside a `session01.py` and must include:

- a class Node that contains a field `key` and is linked to other Nodes to form a Tree.

```
class Node():

    __init__(self, value: int):
        """ Keep it simple and assume only integer values/keys """
        pass
```

- a class Tree that ensures
    - a tree has only one and one root node;
    - each node in the tree that is not the root has one and only one parent node

Implement the following operations: 

```
class Tree():

    __init__(self, root: Node):
        """ Create a new tree given a node """
        pass

    find(self, value) -> Optional[Node]:
        """ Return a node that contains the given value or None if no nodes contain it."""
        pass

    find_all(self, value) -> List[Node]
        """ Return all nodes that contain the given value or an empty list if there are no such nodes in tree. """
        pass
        
    add_child(self, parent: Node, child: Node) -> None :
        """ Add a node at a given position, i.e., as a child of another node. Raise a ValueError in case the child node cannot be added. """
        pass

    add_subtree(self, parent: Node, subtree: Tree) -> None :        
        """ Add a tree as a child of a node (Grafting). Raise a ValueError in case the subtree cannot be added. """
        pass
    
    prune(self, node: Node) -> None:
        """ Delete the node and all its children recursively (Pruning). If the node does not belong to the tree, do nothing. """
        pass
        
    print_values(self) -> None:
        """ Print all the elements in the tree to system output as comma separated list of values. 1,2,3 is ok; 1,   2 ,3 is NOT ok (spaces) """
        pass
```


## Tests

Implement enough unit tests to achieve 100% of statement and branch coverage.
 
Pay attention that `pytest` redirects system output and error; check this [link](https://docs.pytest.org/en/7.1.x/how-to/capture-stdout-stderr.html) to see how you can capture system output and error. You need it to check that `print_values` works correctly.

Below some sample unit tests (you might need to adjust the syntax)

```python
import pytest

def test_nodes_can_have_only_one_parent_self_loop():
    root = Node(1)
    tree = Tree(root)
    
    with pytest.raises(ValueError) as excinfo:
        tree.add_child(root, root)

def test_nodes_can_have_only_one_parent_loop():
    root = Node(1)
    tree = Tree(root)

    child = Node(2)
    tree.add_child(root, child)

    with pytest.raises(ValueError) as excinfo:
        tree.add_child(child, root)

def test_nodes_can_have_only_one_parent():
    root = Node(1)
    tree = Tree(root)

    parent_1 = Node(2)
    parent_2 = Node(3)
    
    tree.add_child(root, parent_1)
    tree.add_child(root, parent_2)
    
    child = Node(4)
    tree.add_child(parent_1, child)

    with pytest.raises(ValueError) as excinfo:
        tree.add_child(parent_2, child) 
```



