# Read : 04

## Python Classes/Objects

- **Python** is an object oriented programming language.

- Almost everything in **Python** is an object, with its *properties* and *methods*.

- A **Class** is like an object constructor, or a *"blueprint"* for creating objects. 

- To create a class, use the keyword `class`:
```
class MyClass:
  x = 5
```
- Now we can use the class named `MyClass` to create objects:
```
p1 = MyClass()
print(p1.x) 
```

- **The __init__() Function**
  - All classes have a function called `__init__()`, which is always executed when the class is being initiated.
  
  - Use the `__init__()` function to assign values to object *properties*, or other operations that are necessary to do when the object is being created.

```
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age
p1 = Person("John", 36)
print(p1.name)
print(p1.age) 
```

- **Object Methods:**
  - Objects can also contain methods. Methods in objects are **functions** that belong to the object. 

  - The `self` parameter is a reference to the current instance of the class, and is used to access variables that belong to the class.

```
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age
  def myfunc(self):
    print("Hello my name is " + self.name)
p1 = Person("John", 36)
p1.myfunc() 
```

- **Delete Objects**:
 - You can delete objects by using the `del` keyword: ```del p1 ```

- **Delete Object Properties**:
 - You can delete properties on objects by using the `del` keyword: ```del p1.age ```


##### [Go Back](code_401_reading_notes.md)