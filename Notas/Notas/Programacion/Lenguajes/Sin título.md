### JavaScript Basics

#### Variables

```markdown
# JavaScript Basics - Variables

## Let and Const
- `let`: Used to declare a variable that can be reassigned.
  ```javascript
  let age = 30;
  age = 31;
  ```

- `const`: Used to declare a constant variable that cannot be reassigned.
  ```javascript
  const name = "John";
  // name = "Doe"; // This will cause an error
  ```

## Var (Avoid Using)
- `var`: Old way to declare variables. Scoped to function, not block.
  ```javascript
  var height = 170;
  ```
```

#### Data Types

```markdown
# JavaScript Basics - Data Types

## Primitive Types
- `Number`
  ```javascript
  let age = 25;
  ```

- `String`
  ```javascript
  let name = "Alice";
  ```

- `Boolean`
  ```javascript
  let isStudent = true;
  ```

- `Null`
  ```javascript
  let emptyValue = null;
  ```

- `Undefined`
  ```javascript
  let notAssigned;
  ```

- `Symbol`
  ```javascript
  let sym = Symbol("description");
  ```

## Reference Types
- `Object`
  ```javascript
  let person = {
    name: "John",
    age: 30
  };
  ```

- `Array`
  ```javascript
  let numbers = [1, 2, 3, 4, 5];
  ```

- `Function`
  ```javascript
  function greet() {
    console.log("Hello!");
  }
  ```

- `Date`
  ```javascript
  let now = new Date();
  ```
```

#### Functions

```markdown
# JavaScript Basics - Functions

## Function Declaration
- Traditional way to define a function.
  ```javascript
  function add(a, b) {
    return a + b;
  }
  ```

## Function Expression
- Define a function as part of a variable declaration.
  ```javascript
  const subtract = function(a, b) {
    return a - b;
  };
  ```

## Arrow Functions
- Shorter syntax introduced in ES6.
  ```javascript
  const multiply = (a, b) => a + b;
  ```

## Immediately Invoked Function Expressions (IIFE)
- Functions that run as soon as they are defined.
  ```javascript
  (function() {
    console.log("IIFE");
  })();
  ```
```

### JavaScript Intermediate

#### Asynchronous JavaScript

```markdown
# JavaScript Intermediate - Asynchronous JavaScript

## Callbacks
- Function passed as an argument to another function.
  ```javascript
  function fetchData(callback) {
    setTimeout(() => {
      callback("Data fetched");
    }, 1000);
  }
  ```

## Promises
- Object representing eventual completion or failure of an asynchronous operation.
  ```javascript
  let promise = new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve("Data fetched");
    }, 1000);
  });

  promise.then(data => {
    console.log(data);
  });
  ```

## Async/Await
- Syntactic sugar for Promises, making asynchronous code look synchronous.
  ```javascript
  async function fetchData() {
    let data = await promise;
    console.log(data);
  }

  fetchData();
  ```


#### DOM Manipulation
markdown
# JavaScript Intermediate - DOM Manipulation

## Selecting Elements
- `getElementById`
  ```javascript
  let element = document.getElementById("myId");
  ```

- `getElementsByClassName`
  ```javascript
  let elements = document.getElementsByClassName("myClass");
  ```

- `querySelector`
  ```javascript
  let element = document.querySelector(".myClass");
  ```

- `querySelectorAll`
  ```javascript
  let elements = document.querySelectorAll(".myClass");
  ```

## Modifying Elements
- Change text content
  ```javascript
  element.textContent = "New Content";
  ```

- Change HTML content
  ```javascript
  element.innerHTML = "<p>New Content</p>";
  ```

- Change styles
  ```javascript
  element.style.color = "red";
  ```

## Event Listeners
- Add event listener
  ```javascript
  element.addEventListener("click", () => {
    console.log("Element clicked");
  });
  ```

- Remove event listener
  ```javascript
  function handleClick() {
    console.log("Element clicked");
  }

  element.addEventListener("click", handleClick);
  element.removeEventListener("click", handleClick);
  ```
```

### JavaScript Advanced

#### ES6 Features

```markdown
# JavaScript Advanced - ES6 Features

## Let and Const
- `let` and `const` for block-scoped variables.

## Arrow Functions
- Shorter function syntax.

## Template Literals
- String literals with embedded expressions.
  ```javascript
  let name = "John";
  let greeting = `Hello, ${name}!`;
  ```

## Destructuring
- Extracting values from arrays or properties from objects.
  ```javascript
  let [a, b] = [1, 2];
  let {name, age} = {name: "John", age: 30};
  ```

## Default Parameters
- Setting default values for function parameters.
  ```javascript
  function greet(name = "Guest") {
    console.log(`Hello, ${name}!`);
  }
  ```

## Rest and Spread Operators
- `Rest`: Collects all remaining elements into an array.
  ```javascript
  function sum(...args) {
    return args.reduce((a, b) => a + b, 0);
  }
  ```

- `Spread`: Expands elements of an array.
  ```javascript
  let arr = [1, 2, 3];
  let newArr = [...arr, 4, 5];
  ```

## Classes
- Syntactic sugar for constructor functions and prototypes.
  ```javascript
  class Person {
    constructor(name, age) {
      this.name = name;
      this.age = age;
    }

    greet() {
      console.log(`Hello, my name is ${this.name}`);
    }
  }

  let john = new Person("John", 30);
  john.greet();
  ```
```
