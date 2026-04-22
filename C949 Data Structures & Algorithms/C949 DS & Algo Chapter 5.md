5.1 Binary Trees
	Binary Tree Basics
		-each node has two children, known as left child and right child
		-definitions related to a binary tree:
		-[Leaf]: tree node with no children
		-[Internal node]: node with at least one child
		-[Root]: one tree node with no parent (the "top" node)
		-[Parent]: node with a child is that child's parent
		-[Node's Ancestors]: include node's parent, parent's parent, etc, up to tree's root
		-[Node's Descendants]: include node's children, children's children, etc.
	Depth, Level, and Height
		-[Edge]: the link form a node to a child
		-[Depth]: number of edge's on the path from the root to the node. root node thus had depth 0
		-[Level]: all nodes with the same depth
		-[Height]: largest depth of any node. Tree with just one node has height 0
	Special Types of Binary Trees
		-binary tree is [full] if every node contains 0 or 2 children
		-binary tree is [complete] if all levels, except possibly the last level, contain all possible nodes and all nodes in the last level are so far left as possible
		-binary tree is [perfect] if all internal nodes have 2 children and all leaf nodes are at the same level
	Subtree
		-a binary tree [subtree] is any node X in the tree and all of X's descendants. Node X is the subtree's root, and the subtree itself is a valid binary tree
5.2 Applications of Trees
	File Systems
		-used to represent hierarchical data
		-tree can represent files and directories in a file system, since a file system is a hierarchy
	Binary Space Partitioning (BSP)
		-technique of repeatedly separating a region of space into two parts and cataloging objects contained within the regions
		-BSP tree is a binary tree used to store information for binary space partitioning 
		-each node in a BSP tree contains information about a region of space and which objects are contained in the region
5.3 Binary Search Trees (BST)
		-useful form of binary tree, which has an ordering property that each node's key is > all keys in the node's left subtree and < all keys in the node's right subtree
		-that property enables fast searching for an item
	BST Search Operation
		- given a key, a BST search operation returns the first node with a matching key or [None] if no matching key is found
		- each time the search compares the search key with an unequal node key, the search need only continue down to one of the node's two children
		- search often visits only a small portion of the tree's nodes
		- BST search operation is said to [visit] a node if that node's key is accessed during the operation
	Successors and Predecessors
		-BST defines an ordering among nodes from smallest to largest
		-BST node's successor is the node that comes after in the BST ordering
		-BST node's predecessor is the node that comes before in the BST ordering
		-if node has a right subtree, node's successor is that right subtree's leftmost child: starting from the right subtrees root, follow left children until reaching a node with no left child (may be that subtree's root itself)
		-if a node doesn't have a right subtree, the node's successor is the first ancestor having this node in a left subtree
5.4 BST: Search Algorithm
	BST Search Algorithm
		-has a current_node reference that starts at the tree's root
		-search key is compared against current_node's key
		-if a match occurs, current_node is reassigned with:
			-the left child if the search key is < current_node's key
			-the right child if the search key is > current_node's key
		-algorithm continues until either a match is found or current_node is NONE
5.5 BST: Insertion
	Insertion Operation
		-inserts the new node in a proper location obeying the BST ordering property
		-simple BST insert algorithm compares the new node with the current node (initially the root)
5.6 BST: Removal
	BST Removal Operation
		-removes the first found matching node, restructuring the tree to preserve the BST ordering property
5.7 BST: Traversal
		-[Tree Traversal]: algorithm visits all nodes in the tree once and performs an operation on each node
	Inorder Traversal
		-visits all nodes in a BST from smallest to largest (useful to print tree's nodes in sorted order)
		-starting from the root, the algorithm recursively prints the left subtree, current node, and right subtree
5.11 Tries
	- a tree representing a set of strings 
	-each non-root node represents a single character
	-each node has at most one child per distinct alphabet character
	-[Terminal node]: node that represents a terminating character, which is the end of a string in the tree
	-Tries provide efficient storage and quick search for strings, and are often used to implement auto-complete and predictive text input