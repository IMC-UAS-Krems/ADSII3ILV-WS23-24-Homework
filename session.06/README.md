# Homework 6 - Description

The goal of this homework is to start developing metaheuristics.

# Task 1

Create a `maximize.py` file in the `session.06` folder and implement an algorithm that solves the "Max One Problem"

The Max One Problem finds the maximum sum of a string of bit of length N:

Maximise: f(x1, ..., xn) = SUM xi


The obvious solution is x=(1,1,…,1); however, you must implement an algorithms that explore the "search space".

You can start implementing:

```
def random_search(n):
    """ Tries to find the optimal solution by guessing it """
    pass
    
def better_search(n):
    """ Invent a smart trial-and-error algorithm that finds the solution (generally) faster than random_search """
    pass
```

# Task 2

Find a way to measure `better_search` and `random_search` performance.

Think of a way to conclude that `better_search` is indeed better than `random_search`.

> Note: By increasing the value of n the difference in performance between the two algorithms should become more and more evident
