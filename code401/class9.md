# Read : 09

## Game of Greed 4

### Dunder Methods

- In Python, special methods are a set of predefined methods you can use to enrich your classes.

- They are easy to recognize because they start and end with double underscores, for example `__init__` or `__str__`.

- As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term *“dunder methods”*, a short form of *“double under.”*

- These *“dunders”* or *“special methods”* in Python are also sometimes called *“magic methods.”*

- Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call `len('string')`. But an empty class definition doesn’t support this behavior out of the box:
```
class NoLenSupport:
    pass
>>> obj = NoLenSupport()
>>> len(obj)
TypeError: "object of type 'NoLenSupport' has no len()"
```
```
class LenSupport:
    def __len__(self):
        return 42
>>> obj = LenSupport()
>>> len(obj)
42
```

### Statistics - Probability

- Probability is the branch of mathematics concerning numerical descriptions of how likely an event is to occur, or how likely it is that a proposition is true. 

- The probability of an event is a number between 0 and 1, where, roughly speaking, 0 indicates impossibility of the event and 1 indicates certainty.

- At the most basic level, probability seeks to answer the question, “What is the chance of an event happening?”

- To calculate the chance of an event happening, we also need to consider all the other events that can occur.

- To calculate the probability of an event occurring, we count how many times are event of interest can occur *(say flipping heads)* and dividing it by the sample space. 

- **From statistics to probability**: 
  - Statistics is the discipline that concerns the collection, organization, analysis, interpretation, and presentation of data. 

  - **Methods**: 
    - A **descriptive statistic** is a summary statistic that quantitatively describes or summarizes features of a collection of information, while descriptive statistics in the mass noun sense is the process of using and analyzing those statistics. 

    - **Statistical inference** is the process of using data analysis to deduce properties of an underlying probability distribution. Inferential statistical analysis infers properties of a population, for example by testing hypotheses and deriving estimates.


##### [Go Back](code_401_reading_notes.md)