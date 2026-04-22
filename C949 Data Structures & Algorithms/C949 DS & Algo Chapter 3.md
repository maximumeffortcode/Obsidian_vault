3.1 Stack Abstract Data Type (ADT)
	-Stack is an ADT representing a collection of items in which items are only inserted on or removed from the top
		-push operation- inserts an item on the top of the stack 
		-pop operation- removes and returns the item at the top of the stack
	-Stack is referred to as a last-in-first-out(LIFO) ADT
	-Stack commonly implemented using a linked list or an array
Common Stack ADT Operations

| Operation    | Description                                  | Example            |
| ------------ | -------------------------------------------- | ------------------ |
| push()       | Inserts x on top of stack                    | stack.push()       |
| pop()        | Removes and returns the stack's top item     | stack.pop()        |
| peck()       | Returns but does not remove stack's top item | stack.peck()       |
| is_empty()   | Returns True if stack has no items           | stack.is_empty()   |
| get_length() | Returns the number of items in the stack     | stack.get_length() |
3.2 Stacks Using Linked Lists
Using A Singly-Linked List for a Stack
	-Stack is often implemented using a singly-linked list
	-Stack object has a reference to the top node, and each node references the node below
Push and Pop Operations
	-push is performed by creating a new list node, assigning the node's data with the item, and prepending the node to the linked list
	-pop is performed by assigning a local variable with the top node's data, removing the list's top node, and then returning the local variable
3.3 Array-Based Stacks
	-Stack can be implemented with an array
	-Two variables are needed in addition to the array:
		1. allocation size: an integer for the array's allocation size
		2. length: an integer for the stack's length
	-Stacks bottom item = array[0]
	-Top item = array[length -1]
	-if stack is empty, length is 0
Unbounded Stack
	-stack with no upper limit on length
Bounded Stack
	-stack with a length that does not exceed a maximum value
	-maximum value is commonly the array's initial allocation size
	-bounded stack with a length equal to the maximum length is said to be full
3.4 Queue Abstract Data Type (ADT)
	-Queue is an ADT representing a collection of items in which items are inserted at the end and removed from the front 
	-Enqueue operation inserts an item at the end of a queue
	-Dequeue operation removes and returns the item at the front of the queue
	-Queue also FIFO ADT and can be implemented using a linked list or an array
3.6 Array-Based Queues
Array-Based Queue Storage
	Two variables needed in addition to the array:
	1. length: integer for numbers of items in the queue
	2. front-index: integer for the queue's front item index
- Queue's content starts at array[front_index] and continues forward through length items
- If array's end reached before encountering all items, remaining items are stored starting at index 0
Bounded VS. Unbounded Queue
	-for bounded queue an additional variable, max_length is needed
	-max_length commonly assigned at construction time and does not change for the queue's lifetime
Enqueue and Dequeue Operations
Enqueue Operation:
	1. Compares self.length and self.max_length. If equal, the queue is full and so no change occurs and False is returned
	2. Compares self.length and len(self.queue_list). If equal, a resize operation occurs
	3. Computes the enqueue item's index as (self.front_index + self.length) % len(self.queue_list) and assigns to queue list at that index
	4. Increments the length attribute and then returns True
	
Dequeue Operation:
	1. Makes a copy of the list item at front_index
	2. Decrements length
	3. Increments front_index, resetting to 0 if the incremented value equals the allocation size
	4. Returns the list item from step 1
3.7 Deque ADT
	an ADT in which items can be inserted and removed at both the front and back



 