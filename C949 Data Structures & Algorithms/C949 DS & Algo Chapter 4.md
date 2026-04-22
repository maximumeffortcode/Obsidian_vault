4.1 Map ADT
	Map Abstract Data Type
	Map (or dictionary): ADT that associates (or maps) keys with values
		-each key in a map is distinct; duplicate keys are not allowed
		-map insert operation takes two parameters [key and value]:
		-if the key does not exist in the map, the key-value pair is inserted
		-if the key does not exist the value is updated
		-the map get operation takes one parameter for the key and returns the associated value or [None] if the key does not exist in the map

4.2 Hash Tables
	A Limited Map ADT Implementation
		-if all keys are integers in the range[0,9], then a map ADT implementation can use a 10 element array to store items
	Hash Codes and Hash Functions
		-[Hash Code]: non-negative integer that attempts to uniquely identify a key
		-[Hash Function]: function that computes a hash code for a given value. Commonly specific to a data type
	Hash Table Overview
		-[Hash Table]: data structure that stores unordered items by mapping (of hashing) each item to a location in an array. Each hash table array element is called a bucket
		-[Hash Map]: implementation of a map ADT using a hash table. Operations like insert, get, and remove each have a key parameter. The key is converted to a bucket index with the following logic:
			1. hash_code = call hash function for key
			2. bucket_index = hash_code % array_allocation_size
	Collisions
		-occurs when two different keys map to the same bucket index
		-[Channing]: collision resolution technique where each bucket has a list of items
		-[Open addressing]: collision resolution technique where collisions are resolved by looking for an empty bucket elsewhere in the table
4.3 Chaining
		-handles hash tables collisions by using a list for each bucket, where each list stores the items that map to that bucket
		-[Get]: return the value corresponding to the key, or None if not found
		-[Insert]: if the search finds a node, update that node's value. If not, append a new node with the inserted key and value to the bucket's linked list
		-[Remove]: if the search finds a node, remove that node from the bucket's linked list
4.4 Linear Probing
		-Hash table with liner probing handles a collision by starting at the key's mapped bucket, and then linearly searches subsequent buckets until an empty bucket is found
    Empty bucket types, search, and removal
	    Two types of empty buckets:
		    -[empty-since-start]: bucket has been empty since hash table was created
			-[empty-after-removal]: bucket had an item removed that caused the bucket to now be empty
4.5 Quadratic Probing
	Quadratic Probing Overview and Insertion
		-Hash table with quadratic probing handles a collision by starting at the key's mapped bucket, and then quadratically searches subsequent buckets until an empty bucket is found
		-Insertion uses the formula starting with i=0, to repeatedly search the hash table until an empty bucket is found. Each time an occupied bucket is found, i is incremented by 1
		-If items hash code is H, the formula (H + c1 * i + c2 i^2) mod tablesize yields the items bucket index. c1 and c2 are programmer defined non-negative integer constants
		-Iterating through sequential i values to obtain the desired index is called the probing sequence
		-Choosing c1=1 and c2=1 is common, simplifying the formula to (H + i+ i^2)
	Search and Removal
		-search algorithm uses the probing sequence until the key being searched for is found or an empty-since-start bucket is found
		-removal algorithm searches for the key to remove and if found, marks the bucket as empty-after-removal
	Choosing c1 and c2
		-Some choices for c1 and c2 are problematic
		-c1 and c2 should not be multiples of the number of buckets
		-some quadratic probing implementations choose c1=0 and c2=1, simplifying the probing sequence formula to : [(H + i^2)] mod tablesize
		-many real world implementations also use a prime number of buckets
4.6 Double Hashing
		-an open-addressing collision resolution technique that uses two different hash functions to compute bucket indices
		-using hash functions H1 and H2, a keys index in the table is computed with the formula [(H1(key) + i * H2(key))] mod tablesize 
	Insertion, Search, and Removal
		-using double hashing a hash table search algorithm probes each bucket using the probing sequence defined by the two has functions
		-search continues until either the matching key is found, an empty-since-start bucket is found or all buckets are probed without a match
4.7 Hash Table Resizing
	Resize Operation
		-increases the number of buckets while preserving all existing items
		-resize operations time complexity = O(N)
	When to Resize
		-hash table's load factor is the number of items in the hast table divided by the number of buckets
			Ex: hash table with 18 items and 31 buckets has a load factor of 18/31 = 0.58
		-implementation may choose to resize the hash table when one or more of the following values exceeds a certain threshold:
			-load factor
			-when using open-addressing, number of collisions during an insertion
			-when using chaining, the size of a bucket's linked list
		-hash table using open addressing, load factor cannot exceed 1.0
4.8 Common Hash Functions
	A Good Hash Function Minimizes Collisions
		-hash table operations are fast if the has function minimizes collisions
		-[Perfect Hash Functions]: maps items to buckets with no collisions
			-can be created if the number of items and all possible item keys are known beforehand
			-runtime for insert, search, and remove is 0(1) with perfect hash function
			-hash functions performance depends on the hash table size and knowledge of the expected keys
	Modulo Hash Function
		-uses the remainder from division of the key the hash tables size
	Mid-Square Hash Function
		-squares the key, extracts R digits from the result's middle, and returns the remainder of the middle digits divided by has table size N
	Multiplicative String Hash Functions
		-repeatedly multiplies the hash value and adds the ASCII (or Unicode) value of each character in the string
		-a multiplicative has function for strings initializes string_hash with a large initial value. For each character, string_hash is reassigned with string_hash times a multiplier (after prime) plus the characters value
		-after iterating through all characters, string_hash is returned
4.9 Direct Hashing
	Direct Hash Function
		-uses the item's key as the bucket index
			Ex: if the key is 937, the index is 937. 
		-hash table with a direct hash function is called a direct access table
	Limitations of Direct Hashing
		-Direct access table has the advantage of no collisions: Each key is unique, and each gets a unique bucket, so no collisions can occur
		-Direct access table has 2 main limitations:
			-all keys must be non-negative integers
			-the hash table's size equals the largest key value plus 1, which may be very large
4.10 Hashing Algorithms: Cryptography, Password Hashing Cryptography
	Cryptography
		-field of study focused on transmitting data securely
		-secure data transmission commonly starts with [encryption]: alteration of data to hide the original meaning
		-[decryption]: opposite of encryption, reconstruction of original data from encrypted data
	Hashing Functions for Data
		-hash functions can be used to produce a hash value for data in contexts other than inserting the data into a hash table
		-commonly used for the purpose of verifying data integrity
		-hash value cannot be used to reconstruct the original data, but can be used to help verify that data isn't corrupt and hasn't been altered 
	Cryptographic Hashing
		-cryptographic hash function is a hash function designed specifically for cryptography
		-commonly used for encrypting and decrypting data
		-[password hash function]: cryptographic hash function that produces a hash value for a password
			-Databases for online services store user's password hash as opposed to the actual password. When user attempts a login, the supplied password is hashed, and the hash is compared against the database's hash value. Because password hashes is breached. attackers may still have a difficult time determining a user's password.
	

		
