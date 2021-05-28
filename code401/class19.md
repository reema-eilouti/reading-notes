# Read : 19

## Automation

- Automation describes a wide range of technologies that reduce human intervention in processes.

- Human intervention is reduced by predetermining decision criteria, subprocess relationships, and related actions and embodying those predeterminations in machines.

- Automation covers applications ranging from a household thermostat controlling a boiler, to a large industrial control system with tens of thousands of input measurements and output control signals.

- Automation has also found space in the banking sector.

- In control complexity, it can range from simple on-off control to multi-variable high-level algorithms. 

- In the simplest type of an automatic control loop, a controller compares a measured value of a process with a desired set value and processes the resulting error signal to change some input to the process, in such a way that the process stays at its set point despite disturbances.

- This closed-loop control is an application of negative feedback to a system. The mathematical basis of control theory was begun in the 18th century and advanced rapidly in the 20th. 

- The term automation, inspired by the earlier word automatic *(coming from automaton)*, was not widely used before 1947, when Ford established an automation department.

-  It was during this time that industry was rapidly adopting feedback controllers, which were introduced in the 1930s.


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

##### [Go Back](code_401_reading_notes.md)