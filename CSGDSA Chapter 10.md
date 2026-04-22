==Recursive Algorithm for Speed==
Quicksort is an extremely fast sorting algorithm that is particularly efficient for average scenarios
Quicksort relies on concept called partitioning

==Partitioning==
To partition an array is to take a random value from the array, which is then called the pivot, and make sure that every number that is less than the pivot ends up to the left of the pivot, and that every number that is greater than the pivot ends up to the right of the pivot

partition! method accepts the starting points of the left and right pointers as parameters, and returns the end position of the left pointer once its complete

==Quicksort==
Works as follows:
	1. Partition the array. Pivot is not in its proper place
	2. Treat the subarrays to left and right of the pivot as their own arrays, and recursively repeat steps #1 and #2. That means we'll partition each subarray, and end up with even smaller subarrays to the left and right of each subarray's pivot
	3. When we have a subarray that has zero or one elements that is our base case and we do nothing

N x log N

==Quickselect==
Hybrid of Quicksort and Binary Search
Can find correct value without having to sort the entire array