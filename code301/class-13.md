# Read : 13

## Update/Delete

### Sending Form Data

- An HTML form on a web page is nothing more than a convenient user-friendly way to configure an HTTP request to send data to a server.

- The `<form>` element defines how the data will be sent. All of its attributes are designed to let you configure the request to be sent when a user hits a *submit button*. 
  
- The two most important attributes are `action` and `method`:
  - **The `action` attribute**:
    - The action attribute defines where the data gets sent.
    - Its value must be a valid relative or absolute URL.
    - `<form action="https://example.com">` or `<form action="/somewhere_else">`
    - When specified with no attributes, the `<form>` data is sent to the same page that the form is present on.

  - **The `method` attribute**:
    - The method attribute defines how data is sent.
    - The most common methods are the **`GET`** method and the **`POST`** method.
      - The **`GET`** method is the method used by the browser to ask the server to send back a given resource.
        - After the URL web address has ended, we include a question mark **(`?`)** followed by the *name/value pairs*, each one separated by an ampersand **(`&`)**.
      - The **`POST`** method is the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request.
        - When the form is submitted using the **POST** method, you get no data appended to the URL.

##### [Go Back](code_301_reading_notes.md)