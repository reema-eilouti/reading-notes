# Read : 30

## Hash Tables

- In computing, a hash table *(hash map)* is a data structure that implements an associative array abstract data type, a structure that can map keys to values. 

- A hash table uses a hash function to compute an index, also called a hash code, into an array of buckets or slots, from which the desired value can be found. 

- During lookup, the key is hashed and the resulting hash indicates where the corresponding value is stored. 

- Ideally, the hash function will assign each key to a unique bucket, but most hash table designs employ an imperfect hash function, which might cause hash collisions where the hash function generates the same index for more than one key. Such collisions are typically accommodated in some way. 

- In a well-dimensioned hash table, the average cost (*number of instructions)* for each lookup is independent of the number of elements stored in the table. 

- Many hash table designs also allow arbitrary insertions and deletions of key–value pairs, at constant average cost per operation.

- In many situations, hash tables turn out to be on average more efficient than search trees or any other table lookup structure. For this reason, they are widely used in many kinds of computer software, particularly for associative arrays, database indexing, caches, and sets. 

- The idea of hashing is to distribute the entries (key/value pairs) across an array of buckets. Given a key, the algorithm computes an index that suggests where the entry can be found: 
    - `index = f(key, array_size)`
    - `hash = hashfunc(key)`
    - `index = hash % array_size`

### Hashing in Python

- Python's built-in hash table implementation, in the form of the dict type, as well as Perl's hash type (%) are used internally to implement namespaces and therefore need to pay more attention to security, i.e., collision attacks. 

- Python sets also use hashes internally, for fast lookup *(though they store only keys, not values).*

- CPython 3.6+ uses an insertion-ordered variant of the hash table, implemented by splitting out the value storage into an array and having the vanilla hash table only store a set of indices.


- **Internal Methods**
    - **Add():** When adding a new key/value pair to a hashtable:

        - send the key to the GetHash method.
        - Once you determine the index of where it should be placed, go to that index
        - Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
        - If something does exist, add the new key/value pair to the data structure within that bucket.

    - **Find():** The Find takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

    - **Contains():** The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.

    - **GetHash():** The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.


##### [Go Back](code_401_reading_notes.md)