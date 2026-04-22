==Crafting Elegant Code with Stacks and Queues==
Stacks and Queues are great tools for handling temporary data
Temporary data is info that doesn't have any meaning after it's processed, so you don't need to keep it around
Stacks and queues allow you to handle data in order, and then get rid of it once you don't need it anymore

==Stacks==
Stores data same way arrays do
Have following 3 constraints:
	1. Data can only be inserted at end of a stack
	2. Data can only be read form the end of a stack
	3. Data can only be removed from end of a stack
(Think of stack as an actual stack of dishes)

Inserting new value into a stack also called pushing onto the stack

Removing elements from the top of the stack is called popping form the stack

Stack if LIFO, "Last In, First Out"-means the last item pushed onto a stack is always the first item popped from it

Stacks ideal for processing any data that should be handled in reverse order to how it was received 
"Undo" function in a word processor, or function calls in a networked application, examples of when to use a stack

==Queues==
Same as stack except 1st item added to the queue is the 1st item to be removed
"FIFO", First In, First Out

Queues are arrays with 3 restrictions:
	1. Data can only be inserted at the end of a queue
	2. Data can only be read from front of a queue
	3. Data can only be removed from front of a queue

Queues common in many applications, ranging from printing jobs to background workers in web applications

Queues ensure that the requests are processed in the order they are received