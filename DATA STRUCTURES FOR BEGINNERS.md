==BIG O NOTATION==
[O(1)]= Constant time, Fastest an algorithm can operate (ie: Speed of Light)
		Same amount of time no matter how much data there is. Top item in a list
[O(n)]= Linear time, pretty fast still but not fastest (ie: super car)(n represents amount of data we have) 
		amount of data increase the amount of time it takes at the same rate. Last item in a list
[O(n^2)]= Quadratic time, very slow (ie: biking from NY to California)
		when every item in a data set needs to interact with every other item
[O(log n)] = Logarithmic time, faster than O(n) but slower than O(1) (ie: Speed of Sound) Binary Search

==DATA STRUCTURES==
[ARRAYS]
	> stores data side by side in memory (think of a row of lockers)
	> to add an item you need to copy all data, create a new larger array and carry over all data plus new item
	> accessing an item is O(1)
	> inserting an item is O(1) if replacing an item
	> inserting a completely new item is O(n)
	> deleting an element is also O(n), unless deleting at very end of array then its O(1)
	
[LINKED LIST]
	> (like a train with multiple cars, can't teleport to a specific car, need to interact with each one til you get to the one you want)
	> each element is stored in a node, each node contains a value and pointer to the next node
	> can easily add or remove element 
	> accessing elements is slower cause you have to start at the beginning
	> accessing is O(n)
	> inserting is O(1) if you know where to insert, if not then its O(n)
	> deletion is O(1) if you have right reference, if not then its O(n)
	
[STACK]
	> Last In, First Out
	> Last added, first removed
	> (Stack of dishes)
	> accessing is O(n) because you have to go through each element
	> inserting/pushing is O(1) because you insert on top of stack
	> deletion is O(1)
	> used alot for Depth First Search
	
[QUEUE]
	> First In, First Out
	> first added, first removed
	> (line at store, as orders are received, the orders go out)
	> only added elements in back, only removed elements in front
	> accessing is O(n)
	> inserting/deletion is O(1)
	> highly used in Breadth First Search
	
[HEAP (PRIORITY QUEUE)]
	> like a pyramid of boxes with smallest box always at the top, always need a box at top
	> Min-Heap, every parent is smaller than its children, top element is the smallest
	> Max Heap, every parent is larger than its children, top element is the largest
	> accessing top element (root) is O(1), any other element is O(n)
	> inserting is O(log n)
	> Heap is a balanced binary tree
	> deletion is O(log n)
	
[HASHMAP/HASH TABLE/DICTIONARIES]
	> "mailbox", every person has dedicated mailbox
	> stores data using key value pairs
	> key use a hash function to determine where the value should be stored
	> example of hash function could be length of a string (ex: John = 4 letters and is stored at index 4)
	> accessing is O(1) but can be O(n) worst case
	> hash collision - multiple elements at same storage location
	> insertion is O(1) but can be O(n) worst case
	> deletion is 0(1) but can be O(n) worst case
	
[BINARY SEARCH TREE]
	> family tree where left child contains nodes with values less than the parent, right child contains nodes with values greater than parent
	> accessing, inserting, and deleting is O(log n) can be O(n) if tree unbalanced 
	
[SET]
	> "Thanos Gauntlet"
	> No Duplications
	> No order
	> useful if searching through trees or graphs and want to keep track if you visited certain node or not
	> Set = unordered collection if unique elements typically implemented using a hash table
	> accessing is O(1) but can be O(n)
	> inserting/deleting is O(1) can be O(n)