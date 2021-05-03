# Read : 03

## Python File Handling

- File handling is an important part of any web application. **Python** has several functions for creating, reading, updating, and deleting files.

1. **open()**
   - The key function for working with files in Python is the open() function.
  
   - The `open()` function takes two parameters; *filename*, and *mode*.
  
   - There are four different *modes* for opening a file:
       - **"r"** (Read) Default value. Opens a file for reading, error if the file does not exist.
       - **"a"** (Append) Opens a file for appending, creates the file if it does not exist.
       - **"w"** (Write) Opens a file for writing, creates the file if it does not exist.
       - **"x"** (Create) Creates the specified file, returns an error if the file exists.
   - In addition you can specify if the file should be handled as binary or text mode:
       - **"t"** (Text) Default value. Text mode.
       - **"b"** (Binary) Binary mode *(e.g. images)*.

    - **Syntax**: `f = open("demofile.txt", "rt")`.

2. **.read()**
```
f = open("demofile.txt", "r")
print(f.read())
```
- To read 5 characters only:
```
f = open("demofile.txt", "r")
print(f.read(5)) 
```
- To read one line:
```
f = open("demofile.txt", "r")
print(f.readline()) 
```
- To read the whole file line by line:
```
f = open("demofile.txt", "r")
for x in f:
  print(x)
```
- **NOTE: Always close the files after you're done using them.**
```
f = open("demofile.txt", "r")
print(f.readline())
f.close()
```

3. **.write()**
```
f = open("demofile2.txt", "a")
f.write("Now the file has more content!")
f.close()
```
```
f = open("demofile3.txt", "w")
f.write("Woops! I have deleted the content!")
f.close()
```

4. **.remove()**
```
import os
if os.path.exists("demofile.txt"):
  os.remove("demofile.txt")
else:
  print("The file does not exist") 
os.rmdir("myfolder") 
```


## Python Error Handling

- The `try` block lets you test a block of code for errors.

- The `except` block lets you handle the error.

- The `finally` block lets you execute code, regardless of the result of the *try and except* blocks.

```
try:
  print(x)
except:
  print("An exception occurred") 
```
- The `try` block will generate an exception, because `x` is not defined:

- Since the `try` block raises an error, the `except` block will be executed.

- Without the `try` block, the program will crash and raise an error.

- Print one message if the `try` block raises a `NameError` and another for other errors.
```
try:
  print(x)
except NameError:
  print("Variable x is not defined")
except:
  print("Something else went wrong") 
```

- You can use the `else` keyword to define a block of code to be executed if no errors were raised.
```
try:
  print("Hello")
except:
  print("Something went wrong")
else:
  print("Nothing went wrong") 
```


##### [Go Back](code_401_reading_notes.md)