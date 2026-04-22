10.1 B-Trees
		Has the following properties:
			-all keys are distinct
			-all leaf nodes are at the same level
			-an internal node with N keys has N + 1 children
			-each node's keys are sorted, leftmost key is min, and rightmost key is max
			-each key in an internal node has one left subtree and one right subtree
			-all left subtree keys are < that key
			-all right subtree keys are > that key
	Higher Order B-Trees
		-as the order of a B-trees increases, the maximum number of keys and children per node increases
		-an internal node must have one more child than keys 
		-each child of an internal node can have a different number of keys than the parent internal node
	2-3-4 Trees
		-an order 4 B-Tree
		-each internal node has 2,3, or 4 children
		-each node has 1,2, or 3 keys
		-a leaf node in. a 2-3-4 tree has no children
		-2-3-4 tree node containing three keys is said to be full
		-node with one key is called a [2-node]
		-node with two key is called a [3-node]
		-node with three key is called a [4-node]
		-2-3-4 tree subtree is any node X in the tree and all of X's descendants
		