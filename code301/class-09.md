# Read : 09

## Refactoring
- **Refactoring** is the process of restructuring existing computer code without changing its external behavior.  
- Refactoring is intended to improve the design, structure, and/or implementation of the software, while preserving its functionality.  
- **Benefits:**
    - Improved code **readability** and reduced complexity; these can improve the source code's **maintainability** and create a simpler, cleaner, or more expressive internal architecture or object model to improve **extensibility**. 
    - Improved performance; to write programs that **perform faster** or **use less memory**.

## Concepts of Functional Programming in Javascript

- **Functional programming** is a *programming paradigm* — a style of building the structure and elements of computer programs.
  
- Its goal is to treat computation as the evaluation of mathematical functions and avoids changing-state and mutable data.

  - **Pure functions**: A pure function is a function where   
    - it returns the same result if given the same arguments *(it is also referred as deterministic)*.
    - It does not cause any observable side effects.

  - **Immutability:** Unchanging over time or unable to be changed.
  
  - **Referential transparency**: pure functions + immutable data = referential transparency

  - **Functions as First-Class Entities:** Where functions are also treated as values and used as data.
    - refer to it from constants and variables
    - pass it as a parameter to other functions
    - return it as result from other functions

  - **Higher-order functions:**
    - They take one or more functions as arguments
    - Return a function as its result

##### [Go Back](code_301_reading_notes.md)