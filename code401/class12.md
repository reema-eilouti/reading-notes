# Read : 12

## pandas

- **pandas** is a software library written for the Python programming language for data manipulation and analysis. 
  
- In particular, it offers data structures and operations for manipulating numerical tables and time series. 
  
- It is free software released under the three-clause BSD license. 
  
- The name is derived from the term "*panel data*", an econometrics term for data sets that include observations over multiple time periods for the same individuals. Its name is a play on the phrase "*Python data analysis*" itself.

- *Wes McKinney* started building what would become pandas at AQR Capital while he was a researcher there from 2007 to 2010.

#### Library features:

1. DataFrame object for data manipulation with integrated indexing.
2. Tools for reading and writing data between in-memory data structures and different file formats.
3. Data alignment and integrated handling of missing data.
4. Reshaping and pivoting of data sets.
5. Label-based slicing, fancy indexing, and subsetting of large data sets.

### pandas for Data Science:

```
import pandas as pd
```
- reading data:
```
data = pd.read_csv('my_file.csv')
data = pd.read_csv('my_file.csv', sep=';', encoding='latin-1', nrows=1000, skiprows=[2,5])
```
- writing data:
```
data.to_csv('my_new_file.csv', index=None)
```
- checking the data:
```
data.shape
data.describe()
```
- seeing the data:
```
data.head(3)
data.loc[8]
data.loc[8, 'column_1']
data.loc[range(4,6)]
```
- basic plotting:
```
data['column_numerical'].plot()
data['column_numerical'].hist()
```

##### [Go Back](code_401_reading_notes.md)