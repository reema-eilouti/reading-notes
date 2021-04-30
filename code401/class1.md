# Read : 01

## Big O Notation

- The **Big O Notation** is a Computer Science concept used to describe the **performance** or **complexity** of an algorithm.

- It helps describe "the worst-case scenario" and to also describe the **execution time required** or the **space used** *(e.g. in memory or on disk)* in an algorithm.

- *Example*: A matching `string` could be found during any iteration of a `for loop` and the function would `return` early, but **Big O** notation will always assume the upper limit where the algorithm will perform **the maximum number of iterations.**  

### **Common Orders of Growth:**

  1. **O(1)**:
     - O(1) describes an algorithm that will always execute in the same time *(or space)* regardless of the size of the input data set.

  2. **O(N)**
      - O(N) describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set. 

  3. **O(N²)**
      - O(N²) represents an algorithm whose performance is directly proportional to the square of the size of the input data set. This is common with algorithms that involve nested iterations over the data set. 
      - Deeper nested iterations will result in O(N³), O(N⁴) etc.

  4. **O(2^N)**
      - O(2^N) denotes an algorithm whose growth doubles with each addition to the input data set. 
      - The growth curve of an O(2^N) function is exponential — starting off very shallow, then rising meteorically. 
      - An example of an O(2^N) function is the recursive calculation of Fibonacci numbers.

  5. **O(logN)**
      - O(logN) describes an algorithm that produces a growth curve that peaks at the beginning and slowly flattens out as the size of the data sets increase.
      - The binary search is an example where an input data set containing 10 items may take one second to complete, a data set containing 100 items will take two seconds, and a data set containing 1,000 items will take three seconds.
      - Increasing the size of the input data set has little effect on its growth as after a single iteration of the algorithm the data set will be halved.

##### [Go Back](code_401_reading_notes.md)