11.1 Searching and Algorithms
	-[Algorithm]: a sequence of steps for accomplishing a task
	-[Linear Search]: search algorithm that starts from the beginning of a list, and checks each element until the search key is found or the end of the list is reached
11.2 Binary Search
	Linear Search vs Binary Search
		-[Binary Search]: algorithm for searching a sorted list, 1st checks middle element of the list
			-incredibly efficient in finding an element within a sorted list
			-maximum number of steps required to reduce the search space to an empty sublist is [log^2 N] + 1
11.4 Constant Time Operations
		-an operation that for a given processor always operates in the same amount of time, regardless of input values
11.5 Growth of Functions and Complexity
		-an algorithm with runtime complexity T(N) has a lower bound and and upper bound 
		-two additional criteria are commonly used to choose a preferred upper to lower bound:
			1. is a single-term polynomial and
			2. bounds T(N) as tightly as possible
	Growth Rates and Asymptotic Notations
		-[Asymptotic notation]: the classification of runtime complexity that uses functions that indicate only the growth rate of a bounding function
		-[Big O Notation]: provides a growth rate for an algorithm's upper bound
		-[Big Omega Notation]: provides a growth rate for an algorithm's lower bound
		-[Big Theta Notation]: provides a growth rate that is both an upper and lower bound
11.6 O Notation
	Big O Notation
		-given a function that describes the running time of an algorithm, the Big O notation for that function can be determined using the following rules:
		1. if f(N) is a sum of several terms, the highest order term (the one with the fastest growth rate) is kept and others are discarded
		2. if f(N) has a term that is a product of several factors, all constants(those that re not in terms of N) are omitted
Common Big O Complexities

| Constant     | 0(1)       |
| ------------ | ---------- |
| Logarithmic  | 0(log N)   |
| Linear       | 0(N)       |
| Linearithmic | 0(N log N) |
| Quadratic    | 0(N^2)     |
| Exponential  | 0(c^2)     |
11.7 Algorithm Analysis
	Worst-Case Algorithm Analysis
		-[worst-case runtime]: runtime complexity for an input that results in the longest execution
11.8 Algorithm Efficiency
		-typically measure by the algorithm's computational complexity
		-computational complexity is the amount of resources used by the algorithm 
		-most common considered are runtime and memory usage
11.9 Recursive Algorithms
		-an algorithm that breaks the problem into smaller subproblems and applies the algorithm itself to solve the smaller subproblems
		-[Base case]: a case where a recursive algorithm complexes without applying itself to a smaller subproblem
		-[Recursive function]: function that calls itself. commonly used to implement recursive algorithms
11.11 Analyzing the Time Complexity of Recursive Algorithms
		-[Recurrence Relation]: a function f(N) that is defined in terms of the same function operating on a value < N
		-[Recursion Tree]: visual diagram of an operation done by a recursive function that separates operations done directly by the function and operations done by recursive calls
11.12 Overview of Fast Sorting Algorithms
		-[Fast Sorting Algorithm]: sorting algorithm that has an average runtime complexity of 0(N log N) or better
	Comparison Sorting
		-[Element Comparison Sorting Algorithm]: sorting algorithm that operates on a list of elements that can be compared to each other 
11.13 Sorting
		-process of putting a collection of elements into ascending (or descending) order
		-sorting just by swapping values is an important part of sorting algorithms
11.14 Selection Sort
		-sorting algorithm that treats the input as two parts, a sorted part and an unsorted part, and repeatedly selects the minimum value to move from the unsorted part to the end of the sorted part
11.15 Insertion Sort
		-sorting algorithm that treats the input as two parts, a sorted part and an unsorted part, and repeatedly insets the next value from the unsorted part into the correct location in the sorted part
		-a [nearly sorted] list only contains a few elements not sorted in order
11.16 Shell Sort 
		-sorting algorithm that treats the input as a collection of interleaved lists, and sorts each list individually with a variant of the insertion sort algorithm
		-uses gap values to determine the number of interleaved lists
		-[Gap Value]: positive integer representing the distance between elements in an interleaved list
	Shell Sort Algorithm
		-shall sort begins by picking an arbitary collection of gap values
		-tends to perform well when choosing gap values in descending order
		-common option is to choose powers of 2 minus 1, in descending order
11.17 Quicksort
		-sorting algorithm that repeatedly partitions the input into low and high parts, and then recursively sorts each part
		-to partition, quicksort chooses a pivot to divide the data into low and high parts
		-the [pivot] can be any value within the list being sorted and is commonly the middle element's value
11.18 Merge Sort
		-sorting algorithm divides a list into two halves, recursively sorts each half, and then merges the sorted halves to produce a sorted list
		-merge sort merges the two sorted partitions into a single list by repeatedly selecting the smallest element from either the left or right partition and adding that element to a temporary merged list
		-once fully merged, the elements in the temporary merged list are copid back to the original list
11.20 Radix Sort
		-sorting algorithm designed specifically for integers
		-[bucket]: collection of integer values that all share a particular digit value
		-radix sort is sorting algorithm specifically for a list of integers:
			-algorithm processes one digit at a time starting with the least significant digit and ending with the most significant
11.22 Bubble Sort
		-sorting algorithm that iterates through a list, comparing and swapping adjacent elements if the second element is less than the first element
		-uses nested loops
		-often considered impractical for real-world use because many faster algorithms exist
11.23 Quickselect
		-algorithm that selects the Kth smallest element in a list
11.24 Bucket Sort
		-numerical sorting algorithm that distributes numbers into buckets, sorts each bucket with an additional sorting algorithm, and then concatenates buckets together to build the sorted result
		-bucket sort is designed for arrays with non-negative numbers
	