# Read : 10

## The Call Stack and Debugging

- A **call stack** is a mechanism for an interpreter to:
  - keep track of its place in a script that calls multiple functions.
  - keep track of what function is currently being run and what functions are called from within that function.

1. When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.

2. Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
  
3. When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
  
- If the stack takes up more space than it had assigned to it, it results in a **_"stack overflow"_** error.

### **Types of error messages:**

  - **Reference errors.**
    - when using `const` and `let`, they are hoisted like `var` and `function` but there is a time between the hoisting and being declared so when you try to access them a reference error occurs, 
    - the fact that this happens to `let` and `const` is called **Temporal Dead Zone _(TDZ)_**. 
  
  - **Syntax errors.**
    - this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.
    - some syntax errors like sending a trailing comma when calling a function are handled without error by most recent browsers, but older ones you have to be careful.

  - **Range errors.**
    - manipulating an object with some kind of length and giving it an invalid length will raise this error.
    - for example an array for instance cannot have a negative length in **JavaScript**.
  
  - **Type errors.**
    - when the types *(`number`, `string` and so on)* you are trying to use or access are incompatible, like accessing a property in an **`undefined`** type of variable.
    - it's the most frequent error in **JS**, like trying to access a property or method that hasn’t been declared yet.


##### [Go Back](code_301_reading_notes.md)