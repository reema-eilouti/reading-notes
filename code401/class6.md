# Read : 06

## Game of Greed 1

### How to use Random Module

- The random module provides access to functions that support many operations. Perhaps the most important thing is that it allows you to **generate random numbers**.

- **When to use it?** When we want the computer to pick a random number in a given range, pick a random element from a list, pick a random card from a deck, flip a coin etc.

#### Random Functions:

- **Randint**
  - *Randint* accepts two parameters: a lowest and a highest number. 
  - The first value should be less than the second.
```
import random
print random.randint(0, 5)
```

- **Random**
  - If you want a larger number, you can multiply it.
```
import random
random.random() * 100
```

- **Choice**
  - Generate a random value from the sequence sequence.
```
import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)
```

### What is Risk Analysis

- **Risk analysis** is a technique used to identify and assess factors that may jeopardize the success of a project or achieving a goal. 

- **Possible risks that you could encounter**:
  
  - Use of new hardware.
  - Use of new technology.
  - Use of new automation tool.
  - The sequence of code.
  - Availability of test resources for the application. 


- **How to perform Risk Analysis**
There are three steps:

  - Searching the risk.
  - Analyzing the impact of each individual risk.
  - Measures for the risk identified.


- **The perspective of Risk Assessment**
There are three perspectives of Risk Assessment:

  - **Effect** – To assess risk by Effect. In case you identify a condition, event or action and try to determine its impact.

  - **Cause** – To assess risk by Cause is opposite of by Effect. Initialize scanning the problem and reach to the point that could be the most probable reason behind that.

  - **Likelihood** – To assess risk by Likelihood is to say that there is a probability that a requirement won’t be satisfied.

##### [Go Back](code_401_reading_notes.md)