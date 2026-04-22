==Big O Notation==
Linear search takes N steps for N elements in the array

==Big O: Count The Steps==
One Step = 0(1)  "O of 1"

0(1) means algorithm takes same number of steps no matter how much data there is

When operations take just one stop for arrays of any size we'd describe their efficiency as 0(1)

0(N) "0 of N"
0(N) is the "Big 0" way of saying that for N elements inside an array, the algorithm would take N steps to complete

==Constant Time vs Linear Time==
Big 0 Notation describes how many steps an algorithm takes based on the number of data elements that the algorithm is acting upon
[Big O answers:] How does the number of steps change as data increases 

Algorithm that is [0(N)] will take as many steps as there are elements of data (if array increases in size, algorithm increases by equal steps)
Algorithm that is [0(1)] will take same number of steps no matter how large array gets
[0(N)] also known as linear time

Algorithm can be described as 0(1) even if it takes more than more step.[Constant Time]

==Same Algorithm, Different Scenarios==
Big O Notation generally refers to worst-case scenario unless specified otherwise

Knowing exactly how inefficient an algorithm can get in a worst-case scenario prepares us for the worst and may have a strong impact on our choices

==An Algorithm Of The Third Kind==
In Big O, we describe binary search as having a time complexity of: [0 (log N)]
This type of algorithm is also known as having a time complexity of log time

[0(log N)] is the Big 0 way of describing an algorithm that increases one step each time the data is doubled. Most efficient to least efficient:
	1. 0(1)
	2. 0(log N)
	3. 0(N)

==Logarithms==
Log is short for logarithms. Nothing to do with algorithms
Logarithms are the inverse of exponents

==0(log N) Explained==
0(log N) really means 0(log_2 N)
0(log N) means that for N data elements, the algorithm would take log_2 N steps

0(log N) means that the algorithm takes as many steps as it takes to keep halving the data elements until we remain with one