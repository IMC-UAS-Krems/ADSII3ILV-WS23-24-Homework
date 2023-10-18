# Homework 3 - Description

The goal of this homework is to implement Search Binary Trees and **validating** they are correct and balanced.

## Task 1

Create a `bst.py` file in the `session.03` and implement the Binary Search Tree Class and the `validate` .

Binary Search Trees must support the following operations:

- Add value. Add a new value inside the tree. For simplicity we assume only integer values are admissible.
    > Note: take care of duplicates!
    
- Remove value. If the value is contained in the tree, remove the corresponding node. The BST must remain a valid BST.

- Find value. Return TRUE if the input value is in the BST, FALSE otherwise
 
- Print In Order(inverse). Print all the values in increasing (inverse == False) or decreasing (inverse == True) order. 

- Pretty Print. Print the tree in a way similar to the `tree` function:

```
root
├── left
└── right
    └── left
```

- Rotate left and rotate right (two separate methods), that given a node of BST (indicated by its value) apply the rotation.
> Note: if there are duplicates, take the FIRST occurrence of the node according to the in-order traversal

## Task 2
Create a `rbt.py` module in `session.03` and implement the basics data structure of RBTree. You can extend the BST to implement a RBTree. Next, implement a module method that VALIDATES a given RBT is valid (Hints: you can reuse the code that validates whether a BST is valid)

> NOTE: **Do not implement** fully the RBTree, only the minimum code to enable validating it!


## Tests

Implement enough unit tests to achieve 100% of statement and branch coverage.

Some hints:
    - create valid and invalid trees
    - create corner cases (skewed trees, trees with only one node, etc.