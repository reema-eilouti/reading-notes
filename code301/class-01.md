# Read : 01

## SMACSS and Responsive Web Design

### 1. SMACSS
Scalable and Modular Architecture for CSS is an approach to web development written by **Jonathan Snook**.

By categorizing CSS rules, we begin to see patterns and can define better practices around each of these patterns.

There are five types of categories:
1. **Base.** To define what an element should look like anywhere on the page. They are the defaults.
2. **Layout.** To divide the page into major top-level sections.
3. **Module.** Smaller bits of code that are reusable on the page, and they are part of a single layout.
4. **State.** To describe how our modules look in different dynamic situations.
5. **Theme.** To contain the rules of the primary colors, shapes, borders, shadows, and such.


### 2. Responsive Web Design

Responsive web design written by **Ethan Marcotte** is broken down into three main components.

- **Flexible Layouts.**
- **Media Queries.**
- **Flexible Media.**

**Flexible Layouts** formula helps identify the proportions of a flexible layout using relative values:  
```target ÷ context = result```

- Before:
```
.container {
  width: 538px;
}
section,
aside {
  margin: 10px;
}
section {
  float: left;
  width: 340px;
}
aside {
  float: right;
  width: 158px;
}
```
- After:
```
section,
aside {
  margin: 1.858736059%; /*  10px ÷ 538px = .018587361 */
}
section {
  float: left;
  width: 63.197026%;    /* 340px ÷ 538px = .63197026 */   
}
aside {
  float: right;
  width: 29.3680297%;  /* 158px ÷ 538px = .293680297 */
}
```

### 3. Float

- The float property specifies how an element should float.
- Absolutely positioned elements ignore the float property.
- Elements after a floating element will flow around it. To avoid this, use the clear property or the clearfix hack.
- ``` float: none|left|right|initial|inherit; ```
- **none** : The element does not float *(will be displayed just where it occurs in the text)* This is default.  
**left** : The element floats to the left of its container.  
**right** : The element floats the right of its container.  
**initial** : Sets this property to its default value.  
**inherit** : Inherits this property from its parent element.
```
img  {
  float: left;
}
```

##### [Go Back](code_301_reading_notes.md)