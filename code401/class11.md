# Read : 11

## Data Analysis

### NumPy

- NumPy is a library for the Python programming language, adding support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays.
  
- The ancestor of NumPy, Numeric, was originally created by *Jim Hugunin* with contributions from several other developers. 
  
- In 2005, *Travis Oliphant* created NumPy by incorporating features of the competing Numarray into Numeric, with extensive modifications. NumPy is open-source software and has many contributors. 

- The Python programming language was not originally designed for numerical computing, but attracted the attention of the scientific and engineering community early on.

#### Examples:

- Array creation:
```
>>> import numpy as np
>>> x = np.array([1, 2, 3])
>>> x
array([1, 2, 3])
>>> y = np.arange(10)  # like Python's list(range(10)), but returns an array
>>> y
array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])s
```

- Basic operations:
```
>>> a = np.array([1, 2, 3, 6])
>>> b = np.linspace(0, 2, 4)  # create an array with four equally spaced points starting with 0 and ending with 2.
>>> c = a - b
>>> c
array([ 1.        ,  1.33333333,  1.66666667,  4.        ])
>>> a**2
array([ 1,  4,  9, 36])
```

### Jupyter

- Project Jupyter is a project and community whose goal is to "*develop open-source software, open-standards, and services for interactive computing across dozens of programming languages*".
  
- It was spun off from IPython in 2014 by *Fernando Pérez*. Project Jupyter's name is a reference to the three core programming languages supported by Jupyter, which are **Julia**, **Python** and **R**, and also a homage to Galileo's notebooks recording the discovery of the moons of Jupiter. 
  
- Project Jupyter has developed and supported the interactive computing products Jupyter Notebook, JupyterHub, and JupyterLab. 

#### Jupyter Notebook

- Jupyter Notebook *(formerly IPython Notebooks)* is a web-based interactive computational environment for creating Jupyter notebook documents. 
  
- The "notebook" term can colloquially make reference to many different entities, mainly the Jupyter web application, Jupyter Python web server, or Jupyter document format depending on context. 
  
- A Jupyter Notebook document is a **JSON** document, following a versioned schema, containing an ordered list of input/output cells which can contain code, text *(using Markdown)*, mathematics, plots and rich media, usually ending with the "**.ipynb**" extension. 

##### [Go Back](code_401_reading_notes.md)