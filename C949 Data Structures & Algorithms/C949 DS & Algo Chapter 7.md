7.1 Heaps
		-[Max-Heap]: is a complete binary tree that maintains the simple property that a node's key is greater than or equal to the node's children's keys
		-max-heap's root always has the maximum key in the entire tree
		-insert into a max-heap starts by inserting the node in the tree's last level, and then swapping the node with the node's parent until no max-heap property violation occurs
		-inserts fill a level (left to right) before adding another level, so tree's height is always the minimum possible
		-[Percolate-Up operation]: operation that moves the node upward
		-max-heap percolate down operation swaps a node with the node's greatest child until no max-heap violation occurs
		-remove operation always removes the root, and is done by replacing the root with the last level's last node then performing a percolate-down operation on the root node
		-both insert and remove operations leave the tree with the minimum height possible
		-[Min-Heap]: similar to max-heap, but node's key is less than or equal to the node's children's keys
			-commonly used to manage prioritized queues of customers awaiting supporting
7.2 Heaps Using Arrays
	Heap Storage 
			-heaps typically stored using arrays
			-heap's array form is produced by traversing the tree's levels from left to right and top to bottom
			-root node always entry at index 0 in the array
			-left child at index 1, right child is entry at index 2, and so on
7.3 Heapsort
	Heapify Operation
		-heapsort is a sorting algorithm that takes advantage of a max-heaps properties by repeatedly removing the max and building a sorted list in reverse order
		-heapify operation is used to turn a list into a heap
7.4 Priority Queue Abstract Data Type (ADT)
	[Priority Queue]: - - a queue where each item has a priority, and items with higher priority are closer to the front of the queue than items with lower priority
	-[Enqueue] - operation inserts an item such that the item in closer to the front than all items of lower priority, and closer to the end than all items of equal or higher priority
	-[Dequeue]: operation removes and returns the item at the front of the queue, which has the highest priority
	-[Enqueue-with-priority]: enqueue operation that includes an argument for the enqueued item's priority  
7.5 Treaps
		-uses a main key that maintains a binary search tree ordering property, and a secondary key generated randomly (often called "priority") during insertions that maintains a heap property
		-Algorithms for basic treap operations include:
			- treap search is the same as a BST search using the main key, sine the treap is a BST
			- treap insert initially inserts a node as in a BST using the main key, then assigns a random priority to the node, and percolates the node up until the heap property is not violated
			- treap delete can be done by setting the node's priority such that the node should be a leaf, percolating the node down using rotations until the node is a leaf, and then removing the node