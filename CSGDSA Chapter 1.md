==The Array: The Foundational Data Structure==
Most data structures used in four basic ways (operations):
	-[Read]: looking something up from a particular spot within the data structure, with an array, this would mean looking up a value at a particular index
	-[Search]: looking for a particular value within a data structure. with array this means looking to see if a particular value exists within the array and if so, which index it's at
	-[Insert]: adding another value to our data structure
	-[Delete]: removing a value from out data structure

*When measuring how "fast" an operation takes, we do not refer to how fast the operation takes in terms of pure time, but instead in how many steps it takes*

[Time Complexity]- measuring speed of operation

==[Reading]==
-reading from array takes just one step
-when computer reads a value at a particular index of an array, it can jump straight to that index in one step

==[Searching]==
-to search a value within an array, computer starts at index 0, checks the value, and if it doesn't find what its looking for, moves on to the next index
-it does this until it finds the value its seeking
-searching is less efficient than reading

==[Insertion]==
-efficiency of inserting a new piece of data inside an array depends on *where* inside the array you'd like to insert it
-insertion worst case scenario can take up to N + 1 steps for an array containing N elements
-inserting a value into beginning of the array N shifts (every data element of the array) and one insertion

==[Deletion]==
-eliminating the value at a particular index

==Sets: How A Single Rule Can Affect Efficiency==
[Sets]- data structure that does not allow duplicate values to be contained within it
-reading and searching in a set the same as in an array
-insertion however firstly requires a search to determine the value doesn't already exist in the set
-insertion into a set in a best case scenario will take N + 1 for N elements
-in worst case scenario, inserting a value at beginning of a set, computer searches N cells, and then another N steps to shift all data to the right and another final step to insert new value
-total of 2N + 1 steps
-deletion the same as an array