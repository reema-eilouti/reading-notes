# What is JavaScript Functions



## JavaScript Functions

- A _JavaScript function_ is a block of code designed to perform a particular task.

- A _JavaScript function_ is executed when "something" invokes it (calls it).

- You can reuse code: Define the code once, and use it many times.

- You can use the same code many times with different arguments, to produce different results.



## JS Functions Syntax

- A _JavaScript function_ is defined with the function keyword, followed by a name, followed by parentheses `()`.

Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).

The parentheses may include parameter names separated by commas:
`(parameter1, parameter2, ...)`

The code to be executed, by the function, is placed inside curly brackets: `{}`

```
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}
```

```
function myFunction(p1, p2) {
  return p1 * p2;   // The function returns the product of p1 and p2
}
```

## Function Invocation
The code inside the function will execute when "something" invokes (calls) the function:

- When an event occurs (when a user clicks a button)
- When it is invoked (called) from JavaScript code
- Automatically (self invoked)

## Function Return
```
function myFunction(a, b) {
  return a * b;             // Function returns the product of a and b
}

var x = myFunction(4, 3);   // Function is called, return value will end up in x
```
x = 12

**_Important Note:_** 
> Accessing a function without **()** will return the function object instead of the function result.



##### [Go Back Home](README.md)