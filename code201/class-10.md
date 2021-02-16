# Class 10 Reading Notes

## JS Error Handling & Debugging  

Debugging is the process of testing, finding, and reducing bugs *(errors)* in computer programs.
The first known computer bug was a real bug *(an insect)* stuck in the electronics.  

Programming code might contain syntax errors, or logical errors.  
Searching for *(and fixing)* errors in programming code is called **code debugging**.
  
- If you understand execution contexts *(which have two stages)* and stacks, you are more likely to find the error in your code.  

- Debugging is the process of finding errors. It involves a process of deduction.  

- The **console** helps narrow down the area in which the error is located, so you can try to find the exact error.  

- JavaScript has 7 different types of errors. Each creates its own error object, which can tell you its line number and gives a description of the error. 
    1. RangeError
        - This is thrown when a number is outside an allowable range of values.
    2. ReferenceError
        - This error is thrown when a reference made to a variable/item is broken. That is the variable/item doesn’t exist.
    3. SyntaxError
        - This is the most common error we encounter. This error occurs when we type code that the JS engine can understand.
    4. TypeError
        - TypeError is used to indicate an unsuccessful operation when none of the other NativeError objects are an appropriate indication of the failure cause.
        - TypeError occurs when an operation is performed on a wrong data type. Maybe a boolean is expected but a sting is found.
    5. URIError
        - This indicates that one of the global URI handling functions was used in a way that is incompatible with its definition.
        - URI (Uniform Resource Indicator) in JS has the functions: decodeURI, decodeURIComponent, etc.
        - If we call any of them with the wrong parameter we will get a URIError
    6. EvalError
        - This is used to identify errors when using the global eval() function.
        -This exception is not currently used within this specification. This object remains for compatibility with previous editions of this specification.
    7. InternalError
        - This error occurs internally in the JS engine, especially when it has too much data to handle and the stack grows way over its critical limit.
        - This occurs when the JS engine is overwhelmed by too many recursions, too many switch cases, etc.
  
- If you know that you may get an error, you can handle it gracefully using the **try, catch, finally statements**. Use them to give your users helpful feedback.  
  

##### [Go Back](code_201_reading_notes.md)