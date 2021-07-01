# Read : 42 a

## Pythonisms

### Dunder Methods

- In Python, special methods are a set of predefined methods you can use to enrich your classes. 

- They are easy to recognize because they start and end with double underscores, for example `__init__` or `__str__`.

- As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term “dunder methods”, a short form of “double under.”

- These “dunders” or “special methods” in Python are also sometimes called “magic methods.” But using this terminology can make them seem more complicated than they really are—at the end of the day there’s nothing “magical” about them. You should treat these methods like a normal language feature.

- Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call `len('string')`. But an empty class definition doesn’t support this behavior out of the box:
```
class NoLenSupport:
    pass
>>> obj = NoLenSupport()
>>> len(obj)
TypeError: "object of type 'NoLenSupport' has no len()"
```
- To fix this, you can add a `__len__` dunder method to your class:
```
class LenSupport:
    def __len__(self):
        return 42
>>> obj = LenSupport()
>>> len(obj)
42
```

### Iterators Methods

- We’ll begin by writing a class that demonstrates the bare-bones iterator protocol in Python. 

- Over the next few paragraphs we’re going to implement a class called Repeater that can be iterated over with a for-in loop, like so:
```
repeater = Repeater('Hello')
for item in repeater:
    print(item)
```

- Like its name suggests, instances of this Repeater class will repeatedly return a single value when iterated over. So the above example code would print the string Hello to the console forever.

- To start with the implementation we’ll define and flesh out the Repeater class first:
```
class Repeater:
    def __init__(self, value):
        self.value = value
    def __iter__(self):
        return RepeaterIterator(self)
```

- What’s the RepeaterIterator object we’re creating and returning from `__iter__`? It’s a helper class we also need to define for our for-in iteration example to work:
```
class RepeaterIterator:
    def __init__(self, source):
        self.source = source
    def __next__(self):
        return self.source.value
```

1. In the `__init__` method we link each RepeaterIterator instance to the Repeater object that created it. That way we can hold on to the “source” object that’s being iterated over.

2. In `RepeaterIterator.__next__`, we reach back into the “source” Repeater instance and return the value associated with it.

- In this code example, Repeater and RepeaterIterator are working together to support Python’s iterator protocol. The two dunder methods we defined, `__iter__` and `__next__`, are the key to making a Python object iterable.

```
>>> repeater = Repeater('Hello')
>>> for item in repeater:
...     print(item)
```
- Output:
```
Hello
Hello
Hello
Hello
Hello
...
```

### Python Generators

- [python_generators](https://dbader.org/blog/python-generators) 


##### [Go Back](code_401_reading_notes.md)