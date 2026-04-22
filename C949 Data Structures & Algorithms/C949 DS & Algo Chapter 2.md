2.1 List Abstract Data Type (ADT)
	A list is a common ADT for holding ordered data, having operations like append a data item, remove a data item, check if a data item exists, and print the list
2.2 Singly-Linked Lists
	data structure for implementing a list ADT, where each node has data and a reference to the next node
	-list structure typically has references to the lists first node and last node
	-first node is called the head
	-last node is called the tail
	-singly-linked list is a type of positional list: a list where elements contain references to the next and/or previous elements in the list
Append Operation
	inserts a new node after the list's tail node
	-append operations algorithm behavior differs if the list is empty versus not empty:
			-append to empty list: if the lists head is NONE, the list's head and tail are assigned with the new node
			-prepend to non-empty list: tail node's next is first assigned with the new node, then the list's tail is assigned with the new node
			-Prepend to non-empty list: the new node's next attribute is first assigned with the lists head node, then the list's head attribute is assigned with the new node
Prepend Operation
	inserts the new node before the list's head node 
	-Prepend to empty list: the list's head and tail attributes are assigned with the new node
	-Prepend to non-empty list: New node's next attribute is 1st assigned with the list's head node, then the list's head attribute is assigned with the new node

2.3 Singly-Linked Lists: Search and Insert
Search Operation
	-returns the first node whose data equals that data value, or None if no such node exists
Insert-Node-After Operation
	-inserts the new node after a provided existing list node

This algorithm considers 3 insertion scenarios:
1. Insert as list's first node: algorithm assigns the lists head and tail attributes with the new node
2. Insert after lists tail node: algorithm assigns the tail node's next attribute and the list's tail attribute with the new node
3. Insert in the middle of list: algorithm assigns the new node's next attribute with the current node's next node, and then assigns current node's next with the new node
Insert-After Operation
	-when using a singly-linked list to implement a list ADT an insert_after(current item, new item) method is implemented
	-calls search() to find the node containing the current item
	-if found, a new node is allocated for the new item, and insert_node_after() is called to insert the new node after the current node
2.4 Single-Linked Lists: Remove
Remove-Node-After Operation
	-removes the node after the specified list node
	-existing node must be specified because each node in a singly-linked list only maintains a reference to the next node
	-existing node specified with current-node parameter
	-if current_node is None, operation removes the list's 1st node
	-otherwise the node after current_node is removed
2.5 Doubly-Linked Lists
	-data structure for implementing a list ADT, where each node has data, a reference to the next node, and a reference to the previous node
	-similar to singly-linked list but each node has a reference to the next and previous nodes
	-doubly linked list is type of **positional list:** a list where elements contain references to the next and/or previous elements in the list
2.8 Circular Lists
	-linked list where the tail node's next attribute references the head of the list, instead of None
	-can be used to represent repeating processes
	-head of circular linked list often referred to as the start node
	-traversal through circular list must terminate after reaching the head node a second time, as opposed to terminating when reaching None
2.9 Linked List Traversal
	-list traversal algorithm visits all nodes in the list once and performs an operation on each node
	-common traversal operation prints all list nodes
	-algorithm starts by assigning a node variable with the lists head
	-while not None, node's data is printed, then the node variable is reassigned with the node that follows after list's tail node visited, node variable is reassigned with None, and traversal ends
	-traversal algorithm works for both singly-linked and doubly-linked lists
Doubly-Linked List Reverse Traversal
	-visits all nodes starting with the list's tail node and ending after visiting the list's head node

2.10 Sorting Linked Lists
Insertion Sort for Doubly-Linked Lists
	-starting with the 2nd list element, each element in the linked list is visited
	-each visited element is moved back as needed and inserted into the correct position in the list's sorted portion
	-link must be double-linked list
Sorting Linked-Lists VS. Arrays
	-sorting algorithms for arrays, require constant-time access to arbitrary, indexed locations to operate efficiently
	-linked lists do not allow indexed access, making for difficult adaptation of such sorting algorithms to operate on linked lists


| Sorting Algorithm | Adaptation to Linked-Lists                                                                                                                          |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| Insertion Sort    | Operates similarly on double linked lists. requires searching from the head of the list for an element's insertion position for singly linked lists |
| Merge Sort        | Finding the middle of the list requires searching linearly from head of list. Merge algorithm can also merge lists without additional storage       |

| Sorting Algorithm | Challenge                                                                                                                             |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Shell Sort        | Jumping the gap between elements cannot be done on a linked list, as each element between two elements must be traversed              |
| Quicksort         | Partitioning requires backward traversal through the right portion of elements. Singly-Linked lists do not support backward traversal |
| Heap Sort         | Indexed access is required to find child nodes in constant time when percolating down                                                 |
2.11 Linked List Dummy Nodes
	-Dummy Node (or header node): node with an unused data member that always resides at the list head and cannot be removed
	-using a dummy node simplifies the algorithms for a linked list because the head and tail attributes are never None
	-an empty list consists of the dummy node, which has the next attribute assigned with None, and the list's head and tail attributes reference the dummy node
Dummy Head and Tail Node
	-Doubly-Linked list implementation can use two dummy nodes:
		-one at head
		-one at tail
	-doing so removes additional conditionals and further simplifies the implementation of most methods 
2.12 Linked Lists: Recursion
Forward Traversal
	-can be implemented using a recursive method writes a node parameter
	-if not None, the node is visited first
	-then a recursive call is made on the node's next attribute to traverse the remainder of the list
2.13 Array-Based Lists
	-a list ADT implemented using an array
	-array-based list supports the common list ADT operations like append, prepend, insert-after, remove, and search
Resize Operation
	-array-based list must be resized if an item is added when the allocation size equals the list length
	-a new array is allocated with a length greater than the existing array
	-doubling the current allocation size is common
	-the existing array elements are then copied to the new array, which becomes the list's storage array
	