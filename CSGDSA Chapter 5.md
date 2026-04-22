==Optimizing Code With and Without Big 0==
==Selection Sort==
Steps of Selection Sort:
	1. Check each cell of the array (left to right) determining which value is least. Moving cell to cell, keep in a variable the lowest value encountered so far. If a cell with lesser value encountered, its replaced so the variable now points to the new index
	2. Once lowest value is determined, swap that index with the value we began the passthrough. 1st passthrough would by index 0, then index 1 on next passthrough etc..
	3. Repeat steps 1 and 2 til all data is sorted

==Selection Sort Efficiency==
Big 0 Notation ignores constants 
Selection and Bubble sort described as 0(N^2) but, selection sort is twice as fast

==Role of Big 0==
if 2 algorithms fall under different classifications of Big 0, you'll generally know algorithm to use

When two algorithms fall under the same classification of Big 0, it doesn't necessarily mean both algorithms process at the same speed