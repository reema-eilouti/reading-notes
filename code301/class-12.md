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
    - The `<%- %>` tags allow us to output the unescaped content onto the page *(notice the -)*. 
    - This is important when using the `include()` statement since you don’t want **EJS** to escape your **HTML** characters like ‘`<`’, ‘`>`’.

- In **EJS**, any **JavaScript** or *non-HTML* syntax you include in your templates is always surrounded by `<% %>` delimiters.

- You can create partials for the **_navbar_** HTML code or the **_footer_** or any part of your template that you keep writing for more than one web page.


##### [Go Back](code_301_reading_notes.md)