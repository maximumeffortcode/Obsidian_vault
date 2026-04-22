==Speeding Up All The Things With Binary Trees==
==Binary Trees==
[Tree] = node-based data structure, but within a tree, each node can have links to multiple nodes

> Binary Tree has following rules:
	- Each node has either zero, one, or two children
	- If a node has two children, it must have one child that has a lesser value than the parent, and one child that has a greater value than the parent

Because of the unique structure of a binary tree, we can search for any value within it very, very, quickly

Algorithm for searching within a binary tree begins at root node:
	1. Inspect value at the node
	2. If found right value, great
	3. If value we're looking for is less than current node, search for it in its left subtree
	4. If value is greater than current node, search for it in its right subtree

Searching in Binary tree is 0(log N)

When creating a tree out of randomly sorted data do trees usually wind up well-balanced. If we insert sorted data into a tree, it can become unbalanced and less efficient

Deletion algorithm follows these rules:
	1. If node being deleted has no children, simply delete it
	2. If node being deleted has one child, delete it and plug the child into the spot where the deleted node was

When deleting a node with two children, replace the deleted node with the successor node. Successor node is the child node whose value is the least of all values that are greater than the deleted node

IF successor node has a right child, after plugging the successor into the spot of the deleted nod, take the right child of the successor node and turn it into the left child of the parent of the successor node. 