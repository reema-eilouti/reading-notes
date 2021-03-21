# Read : 02

## jQuery, Events, and The DOM

- **jQuery** is a lightweight, *"write less, do more"*, **JavaScript** library.

- The purpose of **jQuery** is to make it much easier to use **JavaScript** on your website.

- The **jQuery** library contains the following features:
    - **DOM** manipulation.
    - **Event** methods.

- The **jQuery** syntax is tailor-made for selecting HTML elements and performing some action on the element(s).
    - Basic syntax is: `$(selector).action()`

- **jQuery** uses **CSS** syntax to select elements.
```
$(this).hide() // hides the current element.

$("p").hide() // hides all <p> elements.

$(".test").hide() // hides all elements with class="test".

$("#test").hide() // hides the element with id="test".
```

- In **jQuery**, most **DOM** events have an equivalent **jQuery** method.
    - ` $("p").click( function() { //action goes here! }); `

```
$("#p1").mouseenter(function(){
  alert("You entered p1!");
});

$("#p1").mouseleave(function(){
  alert("Bye! You now leave p1!");
});

$("p").on("click", function(){
  $(this).hide();
});
```

##### [Go Back](code_301_reading_notes.md)