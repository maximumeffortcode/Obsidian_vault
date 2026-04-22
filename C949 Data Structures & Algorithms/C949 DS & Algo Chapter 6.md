6.1 AVL: A Balanced Tree
	Balanced BST
		-[AVL Tree]: BST with a height balance property and specific operations to rebalance the tree when a node is inserted or removed
		-BST is [height balanced] if for any node, the heights of the node's left and right subtree differ by only 0 or 1
		-node's [balance factor] is the left subtree height minus the right subtree height, which is 1, 0, -1 in an AVL tree
			-for calculating a balance factor, a non-existent left or right child's subtree's height is said to be -1
	AVL Tree Height
		-minimizing binary tree height yields the fastest searches, insertions, and removals
6.2 AVL Rotations
	Tree Rotation To Keep Balance
		-[Rotation]: rearrangement of a BST that maintains the BST ordering property while rebalancing the tree
		-rotating is said to be done at the node
6.3 AVL Insertions
		-inserting an item into an AVL tree may cause the tree to become unbalances
		-one or two rotations can rebalance tree
6.5 Red-Black Tree: A Balanced Tree
		-Red-Black Tree is a BST with two node types. red and black, and supporting operations that ensure the tree is balanced when a node is inserted or removed
		-Red-Black Tree's requirements ensure that a tree with N nodes has a height of O(log N):
			-every node is colored either red or black
			-root node is black
			-red node's children cannot be red
			-child assigned with None is considered to be a black leaf node
			-all paths from a node to any None leaf descendant node must have the same number of black nodes
		-When a node's child is assigned with None, that child is a null leaf node. Null leaves are conceptual and don't represent actual nodes in memory