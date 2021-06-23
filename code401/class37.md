# Read : 37

## React 1

- **React** *(also known as **React.js** or **ReactJS**)* is an open-source front-end JavaScript library for building user interfaces or UI components. 

- It is maintained by Facebook and a community of individual developers and companies.

- React can be used as a base in the development of single-page or mobile applications. 

- However, React is only concerned with state management and rendering that state to the DOM, so creating React applications usually requires the use of additional libraries for routing, as well as certain client-side functionality.


- **The smallest React example looks like this:**
```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

- **Variable declaration:**
```
const element = <h1>Hello, world!</h1>;
```

- **Embedding Expressions in JSX**:
```
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;
ReactDOM.render(
  element,
  document.getElementById('root')
);
```

```
function formatName(user) {
  return user.firstName + ' ' + user.lastName;
}
const user = {
  firstName: 'Harper',
  lastName: 'Perez'
};
const element = (
  <h1>
    Hello, {formatName(user)}!  </h1>
);
ReactDOM.render(
  element,
  document.getElementById('root')
);
```

```
function getGreeting(user) {
  if (user) {
    return <h1>Hello, {formatName(user)}!</h1>;  }
  return <h1>Hello, Stranger.</h1>;}
```

- **Specifying Attributes with JSX:**
```
const element = <div tabIndex="0"></div>;
```

```
const element = <img src={user.avatarUrl}></img>;
```

- **Specifying Children with JSX:**

```
const element = <img src={user.avatarUrl} />;
```

```
const element = (
  <div>
    <h1>Hello!</h1>
    <h2>Good to see you here.</h2>
  </div>
);
```

### Handling Events:

- **HTML**:
```
<button onclick="activateLasers()">
  Activate Lasers
</button>
```

- **React:**
```
<button onClick={activateLasers}>  Activate Lasers
</button>
```

- Another difference is that you cannot return false to prevent default behavior in React. You must call preventDefault explicitly.
```
function Form() {
  function handleSubmit(e) {
    e.preventDefault();    console.log('You clicked submit.');
  }
  return (
    <form onSubmit={handleSubmit}>
      <button type="submit">Submit</button>
    </form>
  );
}
```

##### [Go Back](code_401_reading_notes.md)