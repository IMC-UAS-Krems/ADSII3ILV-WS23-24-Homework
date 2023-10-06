# Homework 2 - Description

The goal of the second homework is to implement tree traversals and binary trees (but **not** binary search trees!).

Tree traversals' implementation must be stored inside `treetraversal.py` while the implementation of Binary Tree must be stored inside `binarytree.py`.
For simplicity, create a `tree.py` module and copy into it your implementation of generic tree (and node) from the previous homework.

> Note: Copying around code is NOT a best-practice; however, since we want all the sessions to be completely isolated from each other, this is the safest and fastest way to achieve it.

The `treetraversal` module contains the following four methods, each taking an instance of `Tree` as input:

```
from typing import List
from tree import Node, Tree

def breadth_first(t: Tree) -> List[Node]:
    """ 
    Implement the classic BreadthFirst traversal
    and returns the actual nodes of the tree ordered in a List.
    Returns an empty list if the t is empty.
    """
    pass

def in_order_depth_first(t: Tree) -> List[Node]:
    """ 
    Implement the classic Depth First In-Order traversal
    and returns the actual nodes of the tree ordered in a List.
    Returns an empty list if the t is empty.
    """
    pass
    

def pre_order_depth_first(t: Tree) -> List[Node]:
    """ 
    Implement the classic Depth First Pre-Order traversal
    and returns the actual nodes of the tree ordered in a List.
    Returns an empty list if the t is empty.
    """
    pass
    

def post_order_depth_first(t: Tree) -> List[Node]:
    """ 
    Implement the classic Depth First Post-Order traversal
    and returns the actual nodes of the tree ordered in a List.
    Returns an empty list if the t is empty.
    """
    pass
```

The `binarytree` module contains the implementation of the Binary Tree as subclass of the generic Tree:


```
from tree import Node, Tree

class BinaryTree(Tree):

    pass
    
```


## Tests

Implement enough unit tests to achieve 100% of statement and branch coverage.
 
Pay attention that `pytest` redirects system output and error; check this [link](https://docs.pytest.org/en/7.1.x/how-to/capture-stdout-stderr.html) to see how you can capture system output and error. You need it to check that `print_values` works correctly.

Below some sample unit tests (you might need to adjust the syntax)

```python
import pytest

from tree import Node, Tree
from binarytree import BinaryTree
from treetraversal import breadth_first, in_order_depth_first, pre_order_depth_first, post_order_depth_first


def test_breadth_first():
    """ Given a Tree with one node, the traversal returns that node"
    root = Node(1)
    tree = Tree(root)

    expected_order = [root]
    actual_order = breadth_first(tree)

    # Check: https://docs.pytest.org/en/latest/example/reportingdemo.html
    assert actual_order == expected_order

def test_in_order_depth_first():
    """ Given a Tree with one node, the traversal returns that node"
    root = Node(1)
    tree = Tree(root)

    expected_order = [root]
    in_order_depth_first = in_order_depth_first(tree)

    # Check: https://docs.pytest.org/en/latest/example/reportingdemo.html
    assert actual_order == expected_order


def test_pre_order_depth_first():
    """ Given a Tree with one node, the traversal returns that node"
    root = Node(1)
    tree = Tree(root)

    expected_order = [root]
    actual_order = pre_order_depth_first(tree)

    # Check: https://docs.pytest.org/en/latest/example/reportingdemo.html
    assert actual_order == expected_order


def test_post_order_depth_first():
    """ Given a Tree with one node, the traversal returns that node"
    root = Node(1)
    tree = Tree(root)

    expected_order = [root]
    actual_order = post_order_depth_first(tree)

    # Check: https://docs.pytest.org/en/latest/example/reportingdemo.html
    assert actual_order == expected_order


def test_breadth_first_with_bt():
    """ Given a BinaryTree with one node, the traversal returns that node"
    root = Node(1)
    tree = BinaryTree(root)

    expected_order = [root]
    actual_order = breadth_first(tree)

    # Check: https://docs.pytest.org/en/latest/example/reportingdemo.html
    assert actual_order == expected_order


def test_in_order_depth_first_with_bt():
    """ Given a BinaryTree with one node, the traversal returns that node"
    root = Node(1)
    tree = BinaryTree(root)

    expected_order = [root]
    in_order_depth_first = in_order_depth_first(tree)

    # Check: https://docs.pytest.org/en/latest/example/reportingdemo.html
    assert actual_order == expected_order


def test_pre_order_depth_first_with_bt():
    """ Given a BinaryTree with one node, the traversal returns that node"
    root = Node(1)
    tree = BinaryTree(root)

    expected_order = [root]
    actual_order = pre_order_depth_first(tree)

    # Check: https://docs.pytest.org/en/latest/example/reportingdemo.html
    assert actual_order == expected_order


def test_post_order_depth_first_with_bt():
    """ Given a BinaryTree with one node, the traversal returns that node"
    root = Node(1)
    tree = BinaryTree(root)

    expected_order = [root]
    actual_order = post_order_depth_first(tree)

    # Check: https://docs.pytest.org/en/latest/example/reportingdemo.html
    assert actual_order == expected_order


def test_binary_tree_does_not_allow_more_than_two_nodes():
    root = Node(1)
    tree = BinaryTree(root)
    
    left_child = Node("L")
    right_child = Node("R")
    
    tree.add_child(root, left_child)
    tree.add_child(root, right_child)
    
    with pytest.raises(ValueError) as excinfo:
        tree.add_child(root, Node("Another child")) 
```



