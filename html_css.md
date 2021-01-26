# What is HTML/CSS

## HTML

**HTML** stands for Hypertext Markup Language. It is the standard markup language for documents designed to be displayed in a web browser. 

*HTML* describes the structure of a web page semantically and originally included cues for the appearance of the document.
Web browsers receive *HTML* documents from a web server or from local storage and render the documents into multimedia web pages. 

*HTML* elements are the building blocks of *HTML* pages. It can include headings, paragraphs, lists, links, quotes and other items. *HTML* elements are written in tags using angle brackets. 

## CSS
**CSS** stands for Cascading Style Sheets. It is a style sheet language used for describing the presentation of a document written in a markup language such as *HTML*. 

*CSS* is designed to enable the separation of presentation and content, including layout, colors, and fonts. 
This separation can improve content accessibility, provide more flexibility and control in the specification of presentation characteristics.

### Sample Code 
```
<html>
    <head>
        <title>This is the Title of the Page</title>
    </head>
    <body>
        <h1>This is the Body of the Page</h1>
        <p>
        Anything within the body of a web page is
        displayed in the main browser window.
        </p>
    </body>
</html>
```

### Main Structure Tags

1. The first tag that needs to be included in your *HTML* file is:
    **`<html></html>`**
    - This tag is the root tag, it contains all of the *HTML* content of the webpage.
2. The second tags written within the first tag are: 
   **`<head></head>`** and **`<body></body>`**
    - The `<head>` element contains information about the page (**not** shown within the main part of the browser window).
    - Everything inside the `<body>` element is shown inside the main browser window.
3. Within the *head* tag we add: 
   **`<title></title>`**
    - The contents of the `<title>` element are shown on the tab headline of your page in your browser.


### Other Tags

- `<h1></h1>`
    * This tag is used for the title of a page or post. The formatting of an h1 will make its content bold and big. 
      Going up in the numbers like (h2, h3, h4, h5, h6) will make content smaller.
- `<p></p>`
    * This tag is used to write paragraphs in.
- `<div></div>`
    * This element allows you to group a set of elements together in one block-level box.


### Using Styling
Each **_CSS Rule_** contains a *property* and a *value*.
This is how we add CSS Rules to our HTML elements:

```
<h1 style="background-color:Blue;">Hello, World.</h1>

<p style="background-color:Red;">Hey, everyone!</p>
```
Here, the attribute `style` has a *property* `background-color` and its value is `Red`.
This will give the text a background color on the webpage.

### Other Properties
- `style="text-align:center;"`
- `style="width:200px;"`
- `alt="logo of html and css"`


## Example
You can view a simple HTML/CSS Webpage here: [Index](reading-notes/../index.html)