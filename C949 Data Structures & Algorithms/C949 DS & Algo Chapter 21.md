21.1 Recursive Functions
	 - Function that calls itself is a recursive function
21.2 Recursive Algorithm: Search
	- Any recursive solution can be done using loops. In some cases using a recursive algorithm may make a solution more clear, concise, and understandable
21.3 Adding Output Statements for Debugging
21.4 Creating A Recursive Function
	- Creating a recursive function can be accomplished in two steps:
		1. Write base case - Every recursive function must have a case that returns a value without performing a recursive call (aka base case). Programmer may write that part of the function first and then test. There may be multiple base cases.
		2. Write recursive case - programmer then adds the recursive case to the function. 
	- Recursion is useful when dealing with data structures of unknown size and connectivity, properties most commonly associated with tree-shaped data structures. 
	- Before writing a recursive function, a programmer should determine: (1) Whether the problem has a naturally recursive solution, and (2) whether that solution is better than a non-recursive solution. 
	- A common error is to not cover all possible bases cases in a recursive function. 
	- Another common error is to write a recursive function that doesn't always reach a base case. 
	- Commonly programmers will use two functions for recursion. An "outer" function is intended to be called from other parts of the program. An "inner" function is intended only to be called from that outer function. 
	- Inner function has parameters that are mainly of use as part of the recursion, and need not be part of the outer function, keeping the outer function more intuitive. 
21.5 Recursive Math Functions
	- Depth of recursion is a measure of how many recursive calls of a function have been made but have not yet returned. Default recursion depth limit is typically 1000.
21.6 Recursive Exploration Of All Possibilities 
	- Recursion is a powerful tool for exploring all possibilities. 