# Class 06 Reading Notes

## JS Object Literals and The DOM

### JavaScript Objects

- This code assigns a simple **value** *(Fiat)* to a **variable** named *car*:
```
let car = "Fiat";
```
- Objects are variables too. But objects can contain many values.
- This code assigns **many values** *(Fiat, 500, white)* to a **variable** named *car*:
```
let car = {type:"Fiat", model:"500", color:"white"};
```
- The values are written as **name:value** pairs *(name and value separated by a **colon**)*.
- JavaScript objects are containers for named values called **properties** or **methods**.
- You can access object properties in two ways:
    - `objectName.propertyName`
    - `objectName["propertyName"]`
- **Methods** are stored in properties as **function definitions**.
```
let person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```


### Document Object Model

With the HTML DOM, JavaScript can access and change all the elements of an HTML document.  
When a web page is loaded, the browser creates a Document Object Model of the page.  

The HTML DOM model is constructed as a tree of Objects:  

![DOM](./../images/DOM.gif)  

With the object model, JavaScript gets all the power it needs to create dynamic HTML:  

- JavaScript can change all the HTML elements in the page
- JavaScript can change all the HTML attributes in the page
- JavaScript can change all the CSS styles in the page
- JavaScript can remove existing HTML elements and attributes
- JavaScript can add new HTML elements and attributes
- JavaScript can react to all existing HTML events in the page
- JavaScript can create new HTML events in the page  

- The browser represents the page using a DOM tree.
- DOM trees have four types of nodes: **document nodes**, **element nodes**, **attribute nodes**, and **text nodes**.
- You can select element nodes by their **id** or **class** attributes, by **tag name**, or using **CSS selector** syntax.
- Whenever a DOM query can return more than one node, it will always return a **NodeList**.
- From an element node, you can access and update its content using properties such as **textContent** and **innerHTML** or using DOM manipulation techniques.
- An element node can contain multiple text nodes and child elements that are siblings of each other.
- In older browsers, implementation of the DOM is inconsistent *(and is a popular reason for using jQuery)*. 
- Browsers offer tools for viewing the DOM tree.


##### [Go Back](code_201_reading_notes.md)