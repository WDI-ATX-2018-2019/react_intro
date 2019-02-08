# Welcome To ReactJS
#### Today we will have a Genderal Overview of React and its core concepts.
#####To Start Well discuss
What is React?
How does it differ from what we have learned so far?
Why should we learn React?


###Todays Learning Objectives
>	1. Basic understanding of what react is
>	2. What is the virtual DOM
>	3. How is data passed in React
>	4. What is the difference Between State and Props

```javascript
export default class Welcome extends Component {
  state = {
    todo: [
      ["Lesson", "Intro to React"],
      ["Lesson", "State vs Props"],
      ["Lab", "React Blog"],
      ["Homework", "React ATM"]
    ]
  };
  render() {
    const todoList = this.state.todo.map((item, index) => {
      return (
        <li className="list-item" id={index}>
          <h3>{item[0]}</h3>
          <p>{item[1]}</p>
        </li>
      );
    });

    return (
      <div className="App">
        <header className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <h1>Welcome To React</h1>
          <a
            className="App-link"
            href="https://reactjs.org"
            target="_blank"
            rel="noopener noreferrer"
          >
            Learn React
          </a>
          <ul>{todoList}</ul>
        </header>
      </div>
    );
  }
}

```