# Lua Nested Table Iteration Bug

This repository demonstrates a common, subtle bug in Lua when iterating over nested tables using the `pairs` iterator.  The issue stems from the fact that `pairs` does not guarantee a specific iteration order, which can lead to unexpected results when the table structure is modified during iteration.

The `bug.lua` file contains code that reproduces the problem. The `bugSolution.lua` file offers a solution using a depth-first traversal to ensure predictable iteration.

## Reproducing the Bug

1. Clone this repository.
2. Run `bug.lua` using a Lua interpreter.
3. Observe the unpredictable output due to the order of iteration.

## Solution

The `bugSolution.lua` file provides a solution using a recursive function that iterates over the table in a depth-first manner, guaranteeing consistent iteration order regardless of changes to the table during traversal.