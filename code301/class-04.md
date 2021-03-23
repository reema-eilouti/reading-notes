# Read : 04

## Responsive Web Design and Regular Expressions

### CSS Grid

- The **CSS Grid Layout Module** offers a grid-based layout system, with rows and columns, making it easier to design web pages without having to use *floats* and *positioning*.

- A grid layout consists of a parent element, with one or more child elements.

```
<div class="grid-container">
  <div class="grid-item">1</div>
  <div class="grid-item">2</div>
  <div class="grid-item">3</div>
  <div class="grid-item">4</div>
  <div class="grid-item">5</div>
</div>
```

- An HTML element becomes a grid container when its display property is set to grid or inline-grid.

```
.grid-container {
  display: grid;
}
```

- Grid containers consist of grid items, placed inside columns and rows.

- The `grid-template-columns` property defines the number of columns in your grid layout, and it can define the width of each column.

- If you want your grid layout to contain 4 columns, specify the width of the 4 columns, or `auto` if all columns should have the same width.

```
.grid-container {
  display: grid;
  grid-template-columns: 80px 200px auto 40px;
  grid-template-rows: 80px 200px;
}
```

### RegEx

- **Regular expressions** are extremely useful in extracting information from any text by searching for one or more matches of a specific search pattern.

- One of the most interesting features is that once you’ve learned the syntax, you can actually use this tool in *(almost)* all programming languages.

  - **Anchors** : `^` and `$`
  - **Quantifiers** : `*` `+` `?` and `{}`
  - **OR operator** : `|` or `[]`
  - **Character classes** : `\d` `\w` `\s` and `.`
  - **Grouping and capturing** : `()`
  - **Bracket expressions** : `[]`
  - **Boundaries** : `\b` and `\B`
  - **Back-references** : `\1`
  - **Look-ahead and Look-behind** : `(?=)` and `(?<=)`

```
^The        matches any string that starts with The
end$        matches a string that ends with end
^The end$   exact string match (starts and ends with The end)
roar        matches any string that has the text roar in it
```

```
abc*        matches a string that has ab followed by zero or more c 
abc+        matches a string that has ab followed by one or more c
abc?        matches a string that has ab followed by zero or one c
abc{2}      matches a string that has ab followed by 2 c
abc{2,}     matches a string that has ab followed by 2 or more c
abc{2,5}    matches a string that has ab followed by 2 up to 5 c
a(bc)*      matches a string that has a followed by zero or more copies of the sequence bc
a(bc){2,5}  matches a string that has a followed by 2 up to 5 copies of the sequence bc
```

```
a(b|c)     matches a string that has a followed by b or c (and captures b or c)
a[bc]      same as previous, but without capturing b or c
```

```
\d         matches a single character that is a digit
\w         matches a word character (alphanumeric character plus underscore)
\s         matches a whitespace character (includes tabs and line breaks)
.          matches any character
```

##### [Go Back](code_301_reading_notes.md)