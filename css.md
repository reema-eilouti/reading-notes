# What is CSS


## CSS
**CSS** stands for Cascading Style Sheets. It is a style sheet language used for describing the presentation of a document written in a markup language such as *HTML*. 

*CSS* is designed to enable the separation of presentation and content, including layout, colors, and fonts. 
This separation can improve content accessibility, provide more flexibility and control in the specification of presentation characteristics.

This was reviewed in [What is HTML/CSS](html_css.md)
Now, I'll add more details. 

### Ways to Insert CSS
There are three ways of inserting a style sheet:
1. Inline
    - An inline style may be used to apply a unique style for a single element.
    - To use inline styles, add the style attribute to the relevant element. The style attribute can contain any CSS property.
    - ```<p style="color:red;">This is a paragraph.</p>```
2. Internal
    - An internal style sheet may be used if one single HTML page has a unique style.
    - The internal style is defined inside the `<style>` element, inside the head section.
    - ```body { background-color: lightblue; }```
3. External
    - With an external style sheet, you can change the look of an entire website by changing just one file!
    - Each HTML page must include a reference to the external style sheet file inside the `<link>` element, inside the head section.
    - ```<link rel="stylesheet" href="styles.css">```

### Sample Code 
An external style sheet can be written in any text editor, and must be saved with a .css extension.

The external .css file should not contain any HTML tags.

Here is how my "style.css" file looks:

```
body {
  background-color: powderblue;
}
h1 {
  color: blue;
}
p {
  color: red;
}
```


##### [Go Back Home](README.md)