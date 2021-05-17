# Read : 08

## Game of Greed 3

### List Comprehensions in Python

- List comprehensions provide a concise way to create lists.

- It consists of brackets containing an expression followed by a for clause, then zero or more for or if clauses.

- The expressions can be anything, meaning you can put in all kinds of objects in lists.

- The result will be a new list resulting from evaluating the expression in the context of the for and if clauses which follow it.

- The list comprehension always returns a result list.

- **Before:**
```
new_list = []
for i in old_list:
    if filter(i):
        new_list.append(expressions(i))
``` 

- **After:**
```
new_list = [expression(i) for i in old_list if filter(i)]
```

- **Syntax:**
``` [ expression for item in list if conditional ] ```


### Python Decorators

- A decorator is a design pattern in Python that allows a user to add new functionality to an existing object without modifying its structure.

- Decorators are usually called before the definition of a function you want to decorate.

- This is also called metaprogramming because a part of the program tries to modify another part of the program at compile time.

-**First Class Objects**: In Python, functions are first class objects that means that functions in Python can be used or passed as arguments.

- **Properties of first class functions:**

    - A function is an instance of the Object type.
    - You can store the function in a variable.
    - You can pass the function as a parameter to another function.
    - You can return the function from a function.
    - You can store them in data structures such as hash tables, lists. etc.

- **Syntax for Decorator:**
```
@gfg_decorator
def hello_decorator():
    print("Gfg")
```
```
def hello_decorator():
    print("Gfg")
hello_decorator = gfg_decorator(hello_decorator)
```

- In the above code, `gfg_decorator` is a callable function, will add some code on the top of some another callable function, `hello_decorator` function and return the wrapper function.

##### [Go Back](code_401_reading_notes.md)