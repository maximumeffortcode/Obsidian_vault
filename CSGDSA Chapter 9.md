==Recursively Recurse With Recursion==
Recursion is official name for when a function calls itself

==Recurse Instead of Loop==
In almost any care you can use a loop, you can also use recursion
can end recursion by adding conditional statement
Base Case = case in which the method will not recurse

==Reading Recursive Code==
Process for reading recursive code:
	1. Identify what the base case is
	2. Walk through the function assuming it's dealing with the base case
	3. Then, walk through the function assuming it's dealing with the case immediately before the base case
	4. Progress through your analysis by moving up the cases one at a time

[Stack Overflow] = error caused by infinite recursion where program keeps on pushing the same method over and over again onto the call stack, until there's no room in computer's memory 