# Binary Tree Paths - W13D1

## Problem

Find all paths in binary tree from root node (i.e., top node) to all leaf nodes (i.e., nodes without children) by using a function that takes root of tree and returns a list of all these paths.

## Explanation

1. TreeNode Class - Defines structure of a node in the binary tree. Each node has a value (val), a left child (left), and a right child (right).
2. Solution Class - Contains method binaryTreePaths which will return all root-to-leaf paths.
3. find_paths Function - Helper function used to traverse tree and collect paths.
    - If current node is not None, add its value to current path.
    - If current node is a leaf (without left or right child), add current path to list of paths.
    - If current node is not a leaf, recursively call find_paths on left and right children, appending ‘->’ to path to indicate direction.
4. Initialize - Initialize empty list paths to store all paths and start traversal from root node with an empty path.
5. Return - Return list of paths.

## Optimization

1. Uses Depth-First Search (DFS) to traverse tree, ensuring that each path is explored from root to leaf before moving to another path.
2. Space complexity is O(N) where N is number of nodes in tree, due to the recursion and storage of paths.
3. Time complexity is also O(N) because each node is visited once.
