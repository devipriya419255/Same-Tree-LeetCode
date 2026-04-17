# Same-Tree-LeetCode

"C implementation of LeetCode #100: Same Tree. A recursive depth-first search (DFS) approach to validate structural identity and node value parity between two binary trees."

## 🧩 LeetCode 100: Same Tree (C Solution)

A simple yet fundamental algorithm to determine if two binary trees are identical in both shape and content.

## 📖 Problem Description

Given the roots of two binary trees `p` and `q`, write a function to check if they are the same. Two binary trees are considered the same if they are:
1. Structurally identical.
2. Composed of nodes with identical values.

### Example
- **Input:** `p = [1,2,3], q = [1,2,3]`
- **Output:** `true`
- **Input:** `p = [1,2], q = [1,null,2]`
- **Output:** `false`

## 🛠️ Technical Approach

The solution uses **Recursion (Depth-First Search)** to compare the trees:
1. **Base Case 1**: If both nodes are `NULL`, we've reached the end of a branch simultaneously; return `true`.
2. **Base Case 2**: If only one node is `NULL`, or if the values of the current nodes differ, the trees are not identical; return `false`.
3. **Recursive Step**: The function returns `true` only if both the **left subtrees** and **right subtrees** are identical.

## 📊 Complexity Analysis

- **Time Complexity:** $O(N)$ — In the worst case, we visit every node in both trees once.
- **Space Complexity:** $O(H)$ — Where $H$ is the height of the tree, representing the recursion stack depth. In a balanced tree, this is $O(\log N)$; in a skewed tree, it is $O(N)$.

## 🚀 How to Run

1. Save as `same_tree.c`.
2. Compile:
   ```bash
   gcc -O3 same_tree.c -o same_tree
