==Blazing Fast Lookup With Hash Tables==
==Enter The Hash Table==
Fast reading
Has efficiency of 0(1) on average, as it takes just one step

==Hashing with Hash Functions==
process of taking characters and converting them to numbers known as [hashing]
code used to convert those letters into particular numbers called [hash function]
Hash functions need to meet only one criterion to be valid

==Dealing With Collisions==
Trying to add data to a cell that is already filled is a [collision]

-[Separate Chaining]: approach for handling collisions, when collision occurs, instead of placing a single value in the cell, it places in it a reference to an array

==The Great Balancing Act==
Hash table's efficiency depends on 3 factors:
	1. How much data we're storing in the hash table
	2. How many cells are available in the hash table
	3. Which hash function we're using

A good hash table strikes a balance of avoiding collisions while not consuming lots of memory
-[Rule of thumb]: for every 7 data elements stored in a hash table, it should have 10 cells

This ratio of data to cells is called the [load factor].
Ideal load factor is 0.7 (7 elements / 10 cells)

Hash tables are indispensable when building efficient software. With their 0(1) reads and insertions, its a difficult data structure to beat