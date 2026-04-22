1.1 Data Structures
	- way of organizing, storing, and performing operations on data
	- operations performed on a data structure include accessing or updating stored data, searching for specific data, inserting new data, and removing data. 
Basic Data Structures:

| Data Structure | Description                                                                                                                                                                                                                                                     |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| RECORD         | The data structure that stores subitems, often called fields, with a name associated with each subitem                                                                                                                                                          |
| ARRAY          | Data structure that stores an ordered collection of elements, where each element is directly accessible by a positional index                                                                                                                                   |
| LINKED LIST    | Data structure that stores an ordered list of items in nodes, where each node stores data and has a reference to the next node                                                                                                                                  |
| BINARY TREE    | Data structure in which each node stores data and has up to two children, known as left child and right child                                                                                                                                                   |
| HASH TABLE     | Data structure that stores unordered items by mapping (or hashing) each item to a location in an array                                                                                                                                                          |
| HEAP           | A max-heap is a tree that maintains the simple property that a node's key is greater than or equal to the node's children's keys. A min-heap is a tree that maintains the simple property that a node's key is less than or equal to the node's children's key. |
| GRAPH          | Data structure for representing connections among items, and consists of vertices connected by edges. A **vertex** represents an item in a graph. An **edge** represents a connection between two vertices  in a graph.                                         |
Choosing Data Structures
	- Selection of data structures used in a program depends on both the type of data being stored and the operations the program may need to perform on that data
	- Choosing the best data structure often requires determining which data structure provides a good balance given expected uses.

1.2 Algorithms Overview
	-Algorithm - set of commands that must be followed for a computer to perform calculations or other problem solving operations.
Characteristics of an Algorithm
	-Well-defined Inputs
	- Well-defined Outputs
	- Unambiguity
	- Finiteness
	- Language Independent
	- Effectiveness and Feasibility
Well-Defined Inputs
	- expected inputs of an algorithm must be well-defined to ensure its correctness, predictability, and repeatability
	- ensures that the algorithms behavior is deterministic, which means that the same input will always produce that same output
	- unambiguous inputs help prevent incorrect implementations and misunderstanding of the algorithm's requirements
	- easier to optimize the algorithm based on the characteristics of the input
Well-Defined Outputs
	- outputs of an algorithm should be well defined to ensure that the algorithm produces the intended and accurate result for a given set of inputs
	- avoids ambiguity and guarantees that the algorithm solves the problem correctly
	- also easy to verify the correctness of the algorithms implementation
	- allow you to optimize the algorithm further to achieve the results more efficiently
Unambiguity
	- ambiguity in the algorithm's description can lead to incorrect implementation and unreliable results
	- allows algorithm to be predictable, which makes debugging an implementation easier
	- easier for unambiguous to be standardized and used widely for different applications
	- while implementing unambiguous algorithms, you can focus more on optimizations rather than handling unexpected errors and edge cases
Finiteness
	-algorithm should end after a finite amount of time and should have a limited number of instructions
	 -finite algorithm ensures that will eventually stop executing and produce a result
	 -an infinite algorithm would never reach a conclusion, impractical in real world scenarios where computation cannot be performed infinitely
	 -time and space complexity can be analyzed in the case of a finite algorithm which is important for performing further optimizations
Language Independent
	-language-independent algorithm can be easily ported to different programming languages and platforms, making it more adaptable and useable across various enviroments
	-also makes an algorithm future-proof which means it can be implemented easily using newer programming languages
	-makes it easier to compare the algorithms performance using different programming languages
Effectiveness and Feasibility
	-avoids excessive execution times, which can make an algorithm unusable in real-world scenarios
	-feasible algorithms can be easily implemented using existing hardware infrastructure without using specialized resources
	-they are adopted easily for usage across different fields dur to its practical hardware requirements 

Types of Algorithms

Brute-Force Algorithm
	-most basic approach to solving a problem

Searching Algorithm
	-searches for particular element or a set of elements in a data structure. Can be linear search, binary search, or any other search algorithm

Recursive Algorithm
	-breaks a problem into more minor problems and calls the same function repeatedly for those sub-problems. It contains to do so until it reaches a base case that terminates the function provided the given conditions are met 

Backtracking Algorithm
	-searches for all possible solutions. For each path, we becktrack to the first failure point of that path and then search again for the possible solution in the next path until we find desired solution. Takes more amount of time

Divide and Conquer Algorithm
	-divide a problem set into smaller subsets, solve each seperately, and then combine them for the final solution of the main problem. These include merge sort, quick sort, and more

Greedy Algorithm 
	-looks for the best possible solution at each step and continue with that to obtain the final solution. Solutions obtained by this algorithm may or may not be optimal, but it compares solutions relatively quickly

Dynamic Programming Algorithm
	-uses already computed results to avoid the repetition of the same calculations. This algorithm gaurantees an optimal solution to the problem

Randomized Algorithm
	-employs random integers to choose what action to take at any point in its logic. Due to added randomness, output can be different for the same inputs on different runs. Commonly used in cryptographic algorithms to ensure safety. Helps you avoid worst-case scenarios that a deterministic algorithm may run into

Algorithm Complexity

Time Complexity
	-amount of time an algorithm needs to run entirely, depending on the size of the input given
	-generally time complexity of an algorithm is determined using big O notation
Space Complexity
	-measure of the memory required by an algorithm to run entirely, depending on the size of the input given
	-also determined using big O notation

Advantages of Algorithm
	-Efficiency: Algorithms provide systematic and optimized approaches to solving problems, ensuring that solutions are obtained with minimal time and resource usage
	-Reproducibility: Algorithms are well-defined and deterministic producing the same output for a given set of inputs consistently. Ensures reliable results and easy verification
	-Scalability: Well-designed algorithms can handle large problem sizes, making them suitable for various applications, including big data processing and complex computations
	-Abstraction: Algorithms provide an abstraction over complicated processes by describing them with a set of clear and concise instructions, which makes it easy for you to understand them

Disadvantages of Algorithm
	-Complexity: Some can be complex and difficult to understand or implement
	- Time-Consuming: Developing and optimizing algorithms can be time-intensive
	- Space Consumption: Certain algorithms require significant memory, affecting performance
	- Problem-Specific: Often tailored to specific problems and may not be easily adaptable
	- Maintenance: May require frequent updates and maintenance as requirements change
	- Efficiency: Not all algorithms are efficient, some may have high time or space complexity
	- Scalability: Some may not scale well with increased data or input size

1.3 Into to Algorithms
Algorithms
	-sequence of steps to solve a computational problem or perform a calculation. Can be described in english, pseudocode, programming language, hardware, etc.

**Computational Problem-** specifies an input, a question about the input that can be answered using a computer, and a desired output

Practical Applications of Algorithms
	-Finding the best algorithm to solve a problem can be challenging. Many computational problems have common subproblems for which efficient algorithms have been developed

Efficient Algorithms and Hard Problems
	-An efficient algorithm is one whose runtime increases no more than polynomially with respect to the input size. Some problems exist for which an efficient algorithm is unknown 
NP-complete problems are a set of problems for which no known efficient algorithm exists. NP-complete problems have the following characteristics:
	-No efficient algorithm has been found to solve an NP-complete problem
	-No one has proven that an efficient algorithm to solve an NP-complete problem is impossible
	-If an efficient algorithm exists for one NP-complete problem, than all NP-complete problems can be solved efficiently

1.4 Relation between Data Structures and Algorithms
Algorithms for Data Structures
	-while common operations include inserting, removing, and searching for data, the algorithms to implement those operations are typically specific to each data structure
Algorithms Using Data Structures
	-some algorithms utilize data structures to store and organize data during the algorithm execution

1.5 Abstract Data Types
	-data type described by predefined user operations such as "insert data at rear", without indicating how each operation is implemented. An ADT can be implemented using different underlying data structures
		Ex: a list is a common ADT for holding ordered data, having operations like append a data item, remove a data item, search whether a data item exists, and print the list. A list ADT is commonly implemented using an array or a linked list data structure
Common ADTs

| Abstract Data Type | Description                                                                                                                       | Common Underlying Data Structures |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------- |
| List               | ADT for holding ordered data                                                                                                      | Array, Linked List                |
| Dynamic Array      | ADT for holding ordered data and allowing indexed access                                                                          | Array                             |
| Stack              | ADT in which items are only inserted on or removed from top of a stack                                                            | Linked List, Array                |
| Queue              | ADT which items are inserted at the end of the queue and removed from the front of the queue                                      | Linked List, Array                |
| Deque              | ADT in which items can be inserted and removed at both the front and the back                                                     | Linked List, Array                |
| Bag                | ADT for storing items in which the order does not matter and duplicate items are allowed                                          | Array, Linked List                |
| Set                | ADT for a collection of distinct items                                                                                            | Binary Search Tree, Hash Table    |
| Priority Queue     | Queue where each item has a priority, and items with higher priority are to the front of the queue than items with lower priority | Heap                              |
| Dictionary (Map)   | ADT that associates (or maps) keys with values                                                                                    | Hash Table, Binary Search Tree    |

1.6 Application of ADTs

Abstraction and Optimization
	**Abstraction**- to have a user interact with an item at a high-level, with lower-level internal details hidden from the user
	-ADTs support abstraction by hiding the underlying implementation details and providing a well-defined set of operations for using the ADT

ADTs in Standard Libraries
	Some languages allow programmers to choose the underlying data structure used for the ADTs

1.8 Huffman Compression
Basic Compression Idea
	Compression transforms the data to use fewer bits. Compressed data uses less storage and can be communicated faster than uncompressed data. 
	Basic idea of compression is to encode frequently-occuring items using fewer bits
Huffman Coding
	Common compression technique that assigns fewer bits to frequent items, using a binary tree
Decompressing Huffman Coded Data
	Huffman tree can be used to decompress a compressed string

1.9 Huffman Compression: Implementation

Building a Character Frequency Table
	-1st step in Huffman Compression is to build a character frequency table for the input string. The table contains each distinct character from the input string and each character's number of occurences
	-A dictionary with character keys and integer values can be used to store the frequency table

Building A Huffman Tree
	-can be built from a character frequency table. 
	-1st each (character, frequency) pair from the table becomes a leaf node
	-Next, all leaf nodes are inserted into a priority queue
	-Then a loop does the following while the priority queue's length is at least two:
		-Dequeue the two nodes with the two lowest frequencies
		-Make an internal parent node with the two dequeued nodes as children
		-Insert the parent node into the priority queue

Getting Huffman Codes
	Huffman codes for each character are built from a Huffman tree. Each character corresponds to a leaf node
	Huffman code for a character is built by tracking a path from the root to that character's leaf node, appending 0 when branching left or 1 when branching right

Compression and Decompression Methods
	-to compress an input string, the Huffman codes are first obtained for each character
	-then each character of the input string is processed, and corresponding bit codes are concatenated to produce the compressed result
	-decompressing begins by assigning a node with the tree's root and a result string with an empty string
	-then a loop iterates through each bit in the compressed data
	-the node is reassigned with the node's left child on 0, right child on 1.
	-upon encountering a leaf, the leaf's character is appended to the result and the node is reassigned with the tree's root
	-when no more bits remain in the compressed data, decompression is complete

1.10 Heuristics
	technique that willingly accepts a non-optimal or less accurate solution in order to improve execution speed

Heuristic Optimization
	**heuristic algorithm-** algorithm that quickly determines a near optimal or approximate solution
Self-Adjusting Heuristic
	-algorithm that modifies a data structure based on how that data structure is used

1.11 Greedy Algorithms
	algorithm when presented with a list of options, chooses the option that is optimal at that point in time
	The choice of option does not consider additional subsequent options and may or may not lead to an optimal solution

Activity Selection Problem
	-problem where one or more activities are available, each with a start and finish time, and the goal is to build the largest possible set of activities without time conflicts. 
	- greedy algorithm provides the optimal solution to the activity selection problem

1.12 Dynamic Programming
	problem solving technique that splits a problem into smaller subproblems, computes, and stores solutions to subproblems in memory, and then uses the stored solutions to solve the larger problem
Longest Common Substring
	-algorithm takes 2 strings as input and determines the longest substring that exists in both substrings