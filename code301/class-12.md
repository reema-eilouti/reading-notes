# Read : 12

## Components
### EJS Partials

- **Partials** come in handy when you want to reuse the same *HTML* across multiple views.  
  
- **EJS Partials** help us avoid repetition of the same code on several web pages.  
 
- You define that reusable bundle of code in a file and include it wherever you need it.  
 
- For example, you may want the same `header` for several web pages.

- You should have **Node.js** installed in your before you can start using **EJS**.
  - To begin, ensure you have _**EJS**_ and **_express_** installed via `npm`.

#### Includes
- **Includes** are relative to the template with the `include` call.
  - This requires the '`filename`' option.
  - **Example**: `<%- include('user/show'); %>`

- Use the raw output tag **(`<%-`)** with your `include` to avoid *double-escaping* the **HTML** output.

- **Example on embedding the `include` in the HTML :**
- 
```
<body>
<header>
<% include ./base/header %> 
</header>
<main>
<h1> Other mark up here </h1>
</main>
<footer>
<% include ./base/footer %>
</footer>
</body> 
```
##### [Go Back](code_301_reading_notes.md)