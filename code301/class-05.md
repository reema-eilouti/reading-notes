# Read : 05

## Heroku Deployment

- **Heroku** is a container-based cloud Platform as a Service *(PaaS)*.  
  
- Developers use **Heroku** to deploy, manage, and scale modern apps. 
   
- The platform is elegant, flexible, and easy to use, offering developers the simplest path to getting their apps to market.  
  
- **Heroku** is fully managed, giving developers the freedom to focus on their core product without the distraction of maintaining servers, hardware, or infrastructure.  
  
- The **Heroku** experience provides services, tools, workflows, and polyglot support — all designed to enhance developer productivity.  
  
### Node.js

- **Node.js** is an open-source, cross-platform, back-end JavaScript runtime environment that runs on the V8 engine and executes JavaScript code outside a web browser.

- As an asynchronous event-driven JavaScript runtime, **Node.js** is designed to build scalable network applications.

- In the following *"hello world"* example, many connections can be handled concurrently.

- Upon each connection, the callback is fired, but if there is no work to be done, **Node.js** will sleep.

```
const http = require('http');

const hostname = '127.0.0.1';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World');
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

##### [Go Back](code_301_reading_notes.md)