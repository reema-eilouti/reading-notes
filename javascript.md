# What is JavaScript



## JavaScript

**JS** is a high-level programming language. Alongside *HTML* and *CSS*, *JavaScript* is one of the core technologies of the World Wide Web. It enables interactive web pages and is an essential part of web applications. 

*JavaScript* engines were originally used only in web browsers, but they are now embedded in some servers, usually via *Node.js*. 

Although there are similarities between *JavaScript* and *Java*, including language name, syntax, and respective standard libraries, the two languages are distinct and differ greatly in design.



## JavaScript Syntax

- We write *JavaScript* code inbetween an *HTML* tag:
    - **`<script></script>`**
  
- We **declare variables** as:
    - var x, y, z;       // Declare Variables
    - x = 5; y = 6;      // Assign Values
    - z = x + y;         // Compute Values
  
- Lower Camel Case **variable naming**
    - JavaScript programmers tend to use camel case that starts with a lowercase letter
    - Examples: firstName, lastName, masterCard, interCity
  
- **JS Output**
    - Writing into an HTML element, using `innerHTML`
    - Writing into the HTML output using `document.write()`
    - Writing into an alert box, using `window.alert()`
    - Writing into the browser console, using `console.log()`
  
- **Change HTML Content**
    - `document.getElementById("demo").innerHTML = "Hello JavaScript";`

- **Data Types**
```
var length = 16;                               // Number
var lastName = "Johnson";                      // String
var x = {firstName:"John", lastName:"Doe"};    // Object
var cars = ["Saab", "Volvo", "BMW"];           // Array
```
also, Booleans: `(5 == 5) // Returns true` `(x == z)// Returns false`

##### [Go Back Home](README.md)