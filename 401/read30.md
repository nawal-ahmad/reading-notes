# Read#30: Hash Tables

## Hash tables
It is atype of a data structure that utilize key value pairs,every Node or Bucket has both a key, and a value.

**Terminology**

- Hash: its the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose.

- Buckets: its what contained in each index of the array of the hashtable.

- Collisions: what happens when more than one key gets hashed to the same location of the hashtable.


* reasone why we use hash tables

1. Hold unique values
2. Dictionary
3. Library

 **advantages**
- Hash maps take advantage of an array’s O(1) read access.
- the hash function takes a key and returns an integer. We use the integer to determine where the key/value pair should be placed in the array.

**Structure**

- a hash code turns a key into an integer, hash codes are deterministic: their output is determined only by their input. 
- Hash codes should never have randomness to them, The same key should always produce the same hash code.
- hashtable is created from an array, After creating array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a how:

1. Add or multiply all the ASCII values together.
2. Multiply it by a prime number such as 599.
3. Use modulo to get the remainder of the result, when divided by the total size of the array.
4. Insert into the array at that index.

example:

```
Key = "Cat"
Value = "Josie"

67 - 97 - 116 = 280

280 * 599 = 69648

69648 % 1024 = 16

// Key gets placed in index of 16
```

- Each index of the array can hold many types of values.

- Each Index of the array contain “buckets”. Each of these “buckets” holds one key/value pair combination.


**how hash table store a value:**

1. accept a key
2. calculate the hash of the key
3. use modulus to convert the hash into an array index
4. store the key with the value by appending both to the end of a linked list

**how hash table read a value:**

1. accept a key
2. calculate the hash of the key
3. use modulus to convert the hash into an array index
4. use the array index to access the short LinkedList representing a bucket
5. search through the bucket looking for a node with a key/value pair that matches the key you were given


**Bucket Sizes**

- Hash Maps can have any number of buckets.
- If a hash map has only a few buckets it will be densely full and have many collisions.
- If a hash map has more buckets it will be more sparsely populated.
- The load factor tells us something about how full the hash table is.
- A hash table can start with only a few buckets, calculate it’s own load factor, recognize when it gets too full and automatically grow and add more buckets to itself to accommodate more data.


 **Internal Methods**

1. Add(): When adding a new key/value pair to a hashtable.
2. Find(): The Find takes in a key, gets the Hash, and goes to the index location specified.
3. Contains(): accept a key, and return a bool on if that key exists inside the hashtable.
4. GetHash(): accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.


