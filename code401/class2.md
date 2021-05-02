# Read : 02

## Recursion

- The process in which a function calls itself directly or indirectly is called recursion.
  
- The corresponding function is called as **recursive function**.

- It can be quite easy to slip into writing a function which never terminates, or one that uses excess amounts of memory or processor power.

- However, when written correctly recursion can be a very efficient and mathematically-elegant approach to programming.

- **Recursion Example:**
```
def tri_recursion(k):
  if (k > 0):
    result = k + tri_recursion(k-1)
    print(result)
  else:
    result = 0
  return result
tri_recursion(6)
```
-  In this example we use the `k` variable as the data, which decrements **_(-1)_** every time we recurse.

- One of the ways to tracing recursion is the **Tree/Stack** memory representation.

- Examples of famous problems best solved with recursion is **_Factorial_** and **_Fibonacci_**.

##### [Go Back](code_401_reading_notes.md)