[ARRAY]
Pattern: Array (List)
Use when: Ordered data / index access / iteration
Strength: Fast access by index
Time: O(1) access, O(n) search
Watch for: Insert/delete is slow (O(n))
Example: Looping, storing sequences, sliding window

[HASHMAP(DICTIONARY)]
Pattern: Hashmap (dict)
Use when: Fast lookup / duplicates / key-value mapping
Strength: O(1) lookup
Time: O(1) average (lookup, insert)
Watch for: Unordered, uses more memory
Example: Two Sum, counting frequency, caching

[SET]
Pattern: Set
Use when: Need unique values / fast membership check
Strength: No duplicates + fast lookup
Time: O(1) lookup
Watch for: No order, no indexing
Example: Detect duplicates, remove duplicates

[STACK]
Pattern: Stack (Last In First Out)
Use when: Need to track previous states / reverse order
Strength: Simple push/pop
Time: O(1) push/pop
Watch for: Only access top element
Example: Valid parentheses, undo operations

[QUEUE]
Pattern: Queue (First In First Out)
Use when: Process in order / scheduling
Strength: Maintains order
Time: O(1) enqueue/dequeue (with deque)
Watch for: Slower if using list instead of deque
Example: BFS, task scheduling

[LINKED LIST]
Pattern: Linked List
Use when: Frequent insert/delete without shifting
Strength: Dynamic size
Time: O(1) insert (if pointer known), O(n) search
Watch for: No index access, pointer management
Example: Reverse list, cycle detection

[TREE (BINARY TREE)]
Pattern: Tree
Use when: Hierarchical data / recursive structure
Strength: Fast search (if balanced)
Time: O(log n) (balanced), O(n) worst
Watch for: Recursion, base cases
Example: DFS, BFS, tree traversal

[BINARY SEARCH TREE(BST)]
Pattern: Binary Search Tree
Use when: Sorted data with fast insert/search
Strength: Ordered structure
Time: O(log n) average
Watch for: Can degrade to O(n) if unbalanced
Example: Search, insert, sorted traversal

[HEAP]
Pattern: Heap (Priority Queue)
Use when: Need min/max quickly
Strength: Fast access to smallest/largest
Time: O(log n) insert, O(1) peek
Watch for: Not fully sorted
Example: Top K elements, scheduling

[GRAPH]
Pattern: Graph
Use when: Relationships between items
Strength: Flexible structure
Time: Depends (DFS/BFS = O(V + E))
Watch for: Cycles, visited tracking
Example: Networks, shortest path
