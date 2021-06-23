# Read : 38

## React 2

### Conditional Rendering

- In React, you can create distinct components that encapsulate behavior you need. 

- Then, you can render only some of them, depending on the state of your application.

```
function UserGreeting(props) {
  return <h1>Welcome back!</h1>;
}
function GuestGreeting(props) {
  return <h1>Please sign up.</h1>;
}
```

```
function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) {    
      return <UserGreeting />;  
      }  
      return <GuestGreeting />;
      }
ReactDOM.render(
  // Try changing to isLoggedIn={true}:
  <Greeting isLoggedIn={false} />,  
  document.getElementById('root')
  );
```

### Lists and Keys

```
function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    <li key={number.toString()}>      {number}
    </li>
  );
  return (
    <ul>{listItems}</ul>
  );
}
const numbers = [1, 2, 3, 4, 5];
ReactDOM.render(
  <NumberList numbers={numbers} />,
  document.getElementById('root')
);
```

### Forms

```
class NameForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: ''};
    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }
  handleChange(event) {    this.setState({value: event.target.value});  }
  handleSubmit(event) {
    alert('A name was submitted: ' + this.state.value);
    event.preventDefault();
  }
  render() {
    return (
      <form onSubmit={this.handleSubmit}>        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} />        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```

### Thinking in React

- One of the many great parts of React is how it makes you think about apps as you build them.

- Step 1: Break The UI Into A Component Hierarchy.
- Step 2: Build A Static Version in React.
- Step 3: Identify The Minimal (but complete) Representation Of UI State.
- Step 4: Identify Where Your State Should Live.
- Step 5: Add Inverse Data Flow.

##### [Go Back](code_401_reading_notes.md)