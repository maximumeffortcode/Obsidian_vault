8.1 Set Abstract Data Type (ADT)
		-[Set]: an ADT representing a collection of distinct elements
		-[Add operation]: adds an element to the set (as long as equal element doesn't already exist in the set)
		- a set is an unordered collection
		- [Equal Sets]: two sets that contain the same elements
			- [Ex:] set {3,7,9} equals set {9,3,7}
		- [Cardinality]: (or Set's Length) is number of elements in the set
		- [Remove operation]: removes an element form the set
- Union, Intersection, and Difference
	- [Union]: a set that contains every element from X, every element from Y, and no additional elements
	- [Intersection]: a set that contains every element that is in both X and Y, and no additional elements
	- [Difference]: a set that contains every element that is in X but not in Y, and no additional elements
- Filter and Map
	- filter operation on set X produces a subset containing only elements from X that satisfy a particular condition
	- condition for filtering is commonly represented by a [filter predicate]: function that takes an element indicating whether or not that element will be in the filtered subset
	- map operation on set X produces a new set by applying some function F to each element
8.3 Python Set Class
		-Python includes a built-in set class that implements a set ADT. Set can be initialized using curly braces
			Ex: number_set = {42,12,24} declares a set with new items 42, 12, and 24 