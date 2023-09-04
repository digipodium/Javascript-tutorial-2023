`Team digipodium presents`
# JavaScript Basics
---
# Basic Syntax and Data Types of JavaScript

JavaScript is a scripting language that can run in web browsers and other environments. It can be used to create dynamic and interactive web pages, as well as other applications. In this tutorial, we will learn some of the basic syntax and data types of JavaScript, such as variables, operators, expressions, statements, functions, objects, arrays, etc.

## Variables

Variables are containers that can store values of different types. To declare a variable in JavaScript, we can use the `var`, `let`, or `const` keywords. For example:

```javascript
var x = 10; // declare a variable named x and assign it the value 10
let y = "Hello"; // declare a variable named y and assign it the value "Hello"
const z = true; // declare a constant variable named z and assign it the value true
```

The difference between `var`, `let`, and `const` is that `var` has a function scope, `let` has a block scope, and `const` has a block scope and cannot be reassigned. For example:

```javascript
function foo() {
  var a = 1; // a is only accessible within this function
  let b = 2; // b is only accessible within this block
  if (true) {
    var c = 3; // c is also accessible within this function
    let d = 4; // d is only accessible within this block
    const e = 5; // e is only accessible within this block and cannot be changed
    // e = 6; // this will cause an error
  }
  console.log(a); // prints 1
  console.log(b); // prints 2
  console.log(c); // prints 3
  // console.log(d); // this will cause an error
  // console.log(e); // this will also cause an error
}
```

## Operators

Operators are symbols that perform operations on one or more values. There are different types of operators in JavaScript, such as arithmetic, assignment, comparison, logical, bitwise, etc. For example:

```javascript
// arithmetic operators
console.log(1 + 2); // prints 3 (addition)
console.log(3 - 4); // prints -1 (subtraction)
console.log(5 * 6); // prints 30 (multiplication)
console.log(7 / 8); // prints 0.875 (division)
console.log(9 % 10); // prints 9 (remainder)
console.log(11 ** 12); // prints 3138428376721 (exponentiation)

// assignment operators
var x = 1; // assign the value 1 to x
x += 2; // equivalent to x = x + 2 (add and assign)
x -= 3; // equivalent to x = x - 3 (subtract and assign)
x *= 4; // equivalent to x = x * 4 (multiply and assign)
x /= 5; // equivalent to x = x / 5 (divide and assign)
x %= 6; // equivalent to x = x % 6 (remainder and assign)
x **= 7; // equivalent to x = x ** 7 (exponentiate and assign)

// comparison operators
console.log(1 == "1"); // prints true (equal value)
console.log(1 === "1"); // prints false (equal value and type)
console.log(2 != "2"); // prints false (not equal value)
console.log(2 !== "2"); // prints true (not equal value or type)
console.log(3 < 4); // prints true (less than)
console.log(3 > 4); // prints false (greater than)
console.log(3 <= 4); // prints true (less than or equal to)
console.log(3 >= 4); // prints false (greater than or equal to)

// logical operators
console.log(true && false); // prints false (logical AND)
console.log(true || false); // prints true (logical OR)
console.log(!true); // prints false (logical NOT)

// bitwise operators
console.log(1 & 2); // prints 0 (bitwise AND)
console.log(1 | 2); // prints 3 (bitwise OR)
console.log(1 ^ 2); // prints 3 (bitwise XOR)
console.log(~1); // prints -2 (bitwise NOT)
console.log(1 << 2); // prints 4 (left shift)
console.log(1 >> 2); // prints 0 (right shift)
```

## Expressions

Expressions are combinations of values, variables, operators, and functions that produce a result. For example:

```javascript
var x = 1 + 2; // an expression that assigns the result of 1 + 2 to x
console.log(x * 3); // an expression that prints the result of x * 3
var y = Math.sqrt(x); // an expression that assigns the result of Math.sqrt(x) to y
```

## Statements

Statements are instructions that tell the JavaScript engine what to do. Statements are usually terminated by a semicolon (;). For example:

```javascript
var x = 1; // a statement that declares a variable named x and assigns it the value 1
console.log(x); // a statement that prints the value of x
x++; // a statement that increments the value of x by 1
```

## Functions

Functions are blocks of code that can be defined and invoked to perform a specific task. To define a function in JavaScript, we can use the `function` keyword, followed by the function name, parentheses, and curly braces. For example:

```javascript
function add(a, b) {
  // a function named add that takes two parameters a and b
  return a + b; // return the sum of a and b
}
```

To invoke a function in JavaScript, we can use the function name, followed by parentheses and arguments. For example:

```javascript
var x = add(1, 2); // invoke the add function with arguments 1 and 2 and assign the result to x
console.log(x); // prints 3
```

## Objects

Objects are collections of properties and methods that can be used to represent real-world entities or data structures. To create an object in JavaScript, we can use the object literal syntax, which is a pair of curly braces with key-value pairs inside. For example:

```javascript
var person = {
  // an object named person
  name: "Alice", // a property named name with value "Alice"
  age: 25, // a property named age with value 25
  greet: function () {
    // a method named greet
    console.log("Hello, I am " + this.name); // print a greeting using this keyword to refer to the object itself
  },
};
```

To access or modify the properties or methods of an object in JavaScript, we can use the dot notation or the bracket notation. For example:

```javascript
console.log(person.name); // prints "Alice" (dot notation)
console.log(person["age"]); // prints 25 (bracket notation)
person.greet(); // invokes the greet method (dot notation)
person["name"] = "Bob"; // changes the name property to "Bob" (bracket notation)
```

## Arrays

Arrays are ordered collections of values that can be accessed by index. To create an array in JavaScript, we can use the array literal syntax, which is a pair of square brackets with values inside. For example:

```javascript
var fruits = ["apple", "banana", "cherry"]; // an array named fruits with three values
```

To access or modify the values of an array in JavaScript, we can use the index notation, which is a pair of square brackets with a numeric index inside. The index starts from zero. For example:

```javascript
console.log(fruits[0]); // prints "apple" (index 0)
console.log(fruits[1]); // prints "banana" (index 1)
console.log(fruits[2]); // prints "cherry" (index 2)
fruits[0] = "orange"; // changes the value at index 0 to "orange"
```

Arrays also have some built-in methods that can be used to manipulate or iterate over them. For example:

```javascript
console.log(fruits.length); // prints 3 (the length property returns the number of elements in the array)
fruits.push("durian"); // adds a new element to the end of the array (the push method)
console.log(fruits); // prints ["orange", "banana", "cherry", "durian"]
fruits.pop(); // removes and returns the last element of the array (the pop method)
console.log(fruits); // prints ["orange", "banana", "cherry"]
fruits.forEach(function (fruit) {
  // executes a function for each element of the array (the forEach method)
  console.log(fruit.toUpperCase()); // prints the element in uppercase
});
```
---
# How to Use JavaScript in HTML Documents

JavaScript is a scripting language that can run in web browsers and other environments. It can be used to create dynamic and interactive web pages, as well as other applications. In this tutorial, we will learn how to use JavaScript in HTML documents, such as using the `<script>` tag, linking external JavaScript files, using the `document` object, etc.

## The `<script>` Tag

The `<script>` tag is used to embed JavaScript code in an HTML document. The `<script>` tag can be placed anywhere in the HTML document, but it is usually placed in the `<head>` or the `<body>` section. The `<script>` tag has two attributes: `src` and `type`. The `src` attribute is used to specify the URL of an external JavaScript file. The `type` attribute is used to specify the MIME type of the script. The default value is `text/javascript`. For example:

```html
<head>
  <script src="script.js" type="text/javascript"></script>
</head>
<body>
  <script type="text/javascript">
    // write your JavaScript code here
  </script>
</body>
```

The `<script>` tag can also have a `defer` or an `async` attribute. The `defer` attribute tells the browser to execute the script after the HTML document has been parsed. The `async` attribute tells the browser to execute the script asynchronously as soon as it is available. These attributes are useful for improving the performance and user experience of the web page. For example:

```html
<head>
  <script src="script1.js" type="text/javascript" defer></script>
  <script src="script2.js" type="text/javascript" async></script>
</head>
```

## Linking External JavaScript Files

Linking external JavaScript files is a good practice for organizing and maintaining your code. It also allows you to reuse your code across multiple web pages. To link an external JavaScript file, you need to use the `<script>` tag with the `src` attribute. The value of the `src` attribute should be the URL of the JavaScript file. For example:

```html
<head>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
</head>
```

This example links to the jQuery library from a CDN (Content Delivery Network). A CDN is a network of servers that deliver content to users based on their geographic location. Using a CDN can improve the speed and reliability of your web page.

You can also link to local JavaScript files that are stored in your own server or computer. For example:

```html
<head>
  <script src="js/script.js"></script>
</head>
```

This example links to a JavaScript file named `script.js` that is located in a folder named `js` in the same directory as the HTML document.

## Using the `document` Object

The `document` object is a built-in object that represents the current HTML document. It provides various properties and methods that can be used to access and manipulate the elements and content of the document. For example:

```javascript
console.log(document.title); // prints the title of the document
console.log(document.URL); // prints the URL of the document
console.log(document.body); // prints the body element of the document
document.write("Hello, world!"); // writes "Hello, world!" to the document
document.getElementById("demo"); // returns the element with id="demo"
document.getElementsByTagName("p"); // returns a collection of all <p> elements
document.getElementsByClassName("example"); // returns a collection of all elements with class="example"
document.querySelector("#demo"); // returns the first element that matches the CSS selector "#demo"
document.querySelectorAll(".example"); // returns a collection of all elements that match the CSS selector ".example"
```

The `document` object also has some events that can be used to trigger functions when certain actions occur in the document. For example:

```javascript
document.onload = function () {
  // this function will run when the document is fully loaded
  console.log("The document is ready!");
};
document.onclick = function () {
  // this function will run when the document is clicked
  console.log("The document is clicked!");
};

# How to Use JavaScript to Manipulate the DOM

The DOM (Document Object Model) is a representation of the HTML document as a tree of nodes. Each node corresponds to an element, attribute, text, comment, or other type of content in the document. JavaScript can access and manipulate the DOM using various methods and properties of the `document` object and the nodes themselves. In this tutorial, we will learn how to use JavaScript to manipulate the DOM, such as selecting elements, modifying attributes and styles, creating and removing elements, etc.

## Selecting Elements

To manipulate the DOM, we first need to select the elements that we want to work with. There are several ways to select elements in JavaScript, such as using the `getElementById`, `getElementsByClassName`, `getElementsByTagName`, `querySelector`, and `querySelectorAll` methods of the `document` object. For example:

```javascript
var element = document.getElementById("demo"); // returns the element with id="demo"
var elements = document.getElementsByClassName("example"); // returns a collection of all elements with class="example"
var elements = document.getElementsByTagName("p"); // returns a collection of all <p> elements
var element = document.querySelector("#demo"); // returns the first element that matches the CSS selector "#demo"
var elements = document.querySelectorAll(".example"); // returns a collection of all elements that match the CSS selector ".example"
```

These methods return either a single element or a collection of elements. To access the individual elements in a collection, we can use the index notation or loop through them. For example:

```javascript
var elements = document.getElementsByClassName("example");
console.log(elements[0]); // prints the first element in the collection
console.log(elements[1]); // prints the second element in the collection
for (var i = 0; i < elements.length; i++) {
  // loop through all elements in the collection
  console.log(elements[i]); // prints each element in the collection
}
```

## Modifying Attributes and Styles

Once we have selected an element, we can modify its attributes and styles using various methods and properties of the element object. For example:

```javascript
var element = document.getElementById("demo");
element.setAttribute("title", "This is a demo"); // sets the title attribute of the element to "This is a demo"
element.removeAttribute("title"); // removes the title attribute of the element
element.className = "example"; // sets the class name of the element to "example"
element.style.color = "red"; // sets the color style of the element to "red"
element.style.fontSize = "24px"; // sets the font size style of the element to "24px"
```

## Creating and Removing Elements

We can also create and remove elements from the DOM using various methods of the `document` object and the element object. For example:

```javascript
var newElement = document.createElement("div"); // creates a new <div> element
newElement.innerHTML = "This is a new element"; // sets the inner HTML content of the new element
newElement.id = "new"; // sets the id of the new element to "new"
document.body.appendChild(newElement); // appends the new element as a child of the body element

var oldElement = document.getElementById("demo"); // selects an existing element
oldElement.parentNode.removeChild(oldElement); // removes the existing element from its parent node
```
---
# How to Use JavaScript to Handle User Events and Use the querySelector Method

User events are actions that occur when a user interacts with a web page, such as clicking a button, moving the mouse, typing on the keyboard, submitting a form, etc. JavaScript can handle user events using various methods and properties of the `document` object and the element object. In this tutorial, we will learn how to use JavaScript to handle user events, such as clicks, mouse movements, keyboard inputs, form submissions, etc. and use the querySelector method to select elements that match a given CSS selector.

## The `addEventListener` Method

The `addEventListener` method is used to attach an event listener to an element. An event listener is a function that runs when a specific event occurs on the element. The `addEventListener` method takes two or three parameters: the event type, the event handler function, and an optional boolean value that indicates whether to use the capturing or bubbling phase of the event. For example:

```javascript
var button = document.querySelector("#button"); // select an element using querySelector
button.addEventListener("click", function () {
  // attach an event listener for the click event
  alert("You clicked the button!"); // run this function when the click event occurs
});
```

This example attaches an event listener for the click event to a button element that has an id of "button". When the user clicks the button, an alert message will pop up.

The event type is a string that specifies the name of the event, such as "click", "mouseover", "keydown", "submit", etc. The event handler function is a function that defines what to do when the event occurs. The function can take an optional parameter that represents the event object. The event object contains various properties and methods that provide information and control over the event. For example:

```javascript
var input = document.querySelector("#input"); // select an element using querySelector
input.addEventListener("keydown", function (event) {
  // attach an event listener for the keydown event
  console.log(event.keyCode); // print the code of the pressed key
  if (event.keyCode === 13) {
    // check if the pressed key is Enter
    alert("You pressed Enter!"); // run this function if the pressed key is Enter
    event.preventDefault(); // prevent the default action of the keydown event
  }
});
```

This example attaches an event listener for the keydown event to an input element that has an id of "input". When the user presses a key on the keyboard, the code of the pressed key will be printed in the console. If the pressed key is Enter, an alert message will pop up and the default action of the keydown event will be prevented.

The capturing or bubbling phase is a concept that describes how events propagate through the DOM tree. When an event occurs on an element, it can trigger other events on its parent elements or its child elements. The capturing phase is when the event travels from the root element to the target element. The bubbling phase is when the event travels from the target element to the root element. By default, the `addEventListener` method uses the bubbling phase. To use the capturing phase, we can pass `true` as the third parameter of the `addEventListener` method. For example:

```javascript
var parent = document.querySelector("#parent"); // select an element using querySelector
var child = document.querySelector("#child"); // select another element using querySelector
parent.addEventListener(
  "click",
  function () {
    // attach an event listener for the click event on parent using capturing phase
    console.log("Parent clicked!");
  },
  true
);
child.addEventListener("click", function () {
  // attach an event listener for the click event on child using bubbling phase
  console.log("Child clicked!");
});
```

This example attaches two event listeners for the click event on two elements: parent and child. The parent element has an id of "parent" and uses the capturing phase. The child element has an id of "child" and uses the bubbling phase. When we click on the child element, both events will be triggered in this order: parent clicked, child clicked.

## The `removeEventListener` Method

The `removeEventListener` method is used to remove an event listener from an element. The `removeEventListener` method takes two or three parameters: the same event type, event handler function, and capturing or bubbling phase as used in the `addEventListener` method. For example:

```javascript
var button = document.querySelector("#button"); // select an element using querySelector
function handleClick() {
  // define a function as an event handler
  alert("You clicked the button!");
}
button.addEventListener("click", handleClick); // attach an event listener for the click event using handleClick function
button.removeEventListener("click", handleClick); // remove an event listener for the click event using handleClick function
```

This example removes an event listener for the click event from a button element that has an id of "button" using a named function as an event handler.

## The `onclick`, `onmouseover`, `onkeydown`, `onsubmit`, etc. Properties

Another way to handle user events in JavaScript is to use the `onclick`, `onmouseover`, `onkeydown`, `onsubmit`, etc. properties of the element object. These properties can be assigned a function that runs when the corresponding event occurs on the element. For example:

```javascript
var button = document.querySelector("#button"); // select an element using querySelector
button.onclick = function () {
  // assign a function to the onclick property
  alert("You clicked the button!"); // run this function when the click event occurs
};
```

This example assigns a function to the onclick property of a button element that has an id of "button". When the user clicks the button, an alert message will pop up.

The advantage of using these properties is that they are simpler and shorter than using the `addEventListener` method. The disadvantage is that they can only handle one event handler function per event type per element. If we assign another function to the same property, it will overwrite the previous one. For example:

```javascript
var button = document.querySelector("#button"); // select an element using querySelector
button.onclick = function () {
  // assign a function to the onclick property
  alert("You clicked the button!");
};
button.onclick = function () {
  // assign another function to the onclick property
  console.log("You clicked the button!");
};
```

This example assigns two functions to the onclick property of a button element that has an id of "button". Only the second function will run when the user clicks the button.
---
# How to Use JavaScript to Communicate with the Server

JavaScript is a scripting language that can run in web browsers and other environments. It can be used to create dynamic and interactive web pages, as well as other applications. One of the most common uses of JavaScript is to communicate with the server, which is a computer that hosts and delivers data and resources over the internet. By communicating with the server, JavaScript can send requests, receive responses, and update the web page without reloading it. This makes the web page more responsive and user-friendly.

In this tutorial from digipodium, we will learn how to use JavaScript to communicate with the server, such as using the XMLHttpRequest object, using the fetch API, using the axios library, etc.

## The XMLHttpRequest Object

The XMLHttpRequest object is a built-in object that allows JavaScript to make HTTP requests to the server. HTTP (Hypertext Transfer Protocol) is a protocol that defines how messages are formatted and transmitted over the internet. HTTP requests are messages that contain information about what data or resource is requested from the server. HTTP responses are messages that contain information about what data or resource is returned from the server.

To use the XMLHttpRequest object, we need to follow these steps:

- Create a new XMLHttpRequest object using the `new` keyword and the `XMLHttpRequest` constructor. For example:

```javascript
var xhr = new XMLHttpRequest(); // create a new XMLHttpRequest object
```

- Open the request using the `open` method of the XMLHttpRequest object. The `open` method takes three or four parameters: the HTTP method, the URL, an optional boolean value that indicates whether to make an asynchronous or synchronous request, and an optional username and password for authentication. The HTTP method is a string that specifies what action to perform on the server, such as "GET", "POST", "PUT", "DELETE", etc. The URL is a string that specifies the location of the data or resource on the server. The asynchronous or synchronous request determines whether to wait for the response before executing the next line of code or not. By default, it is `true`, which means asynchronous. For example:

```javascript
xhr.open("GET", "https://jsonplaceholder.typicode.com/users"); // open a GET request to get users data from a fake API
```

- Send the request using the `send` method of the XMLHttpRequest object. The `send` method can take an optional parameter that contains the data to send to the server. For example:

```javascript
xhr.send(); // send the request without any data
```

- Handle the response using the `onreadystatechange` property and the `readyState` and `status` properties of the XMLHttpRequest object. The `onreadystatechange` property is an event handler that runs when the state of the request changes. The `readyState` property is a number that indicates the current state of the request, from 0 (uninitialized) to 4 (done). The `status` property is a number that indicates the status code of the response, such as 200 (OK), 404 (Not Found), 500 (Internal Server Error), etc. For example:

```javascript
xhr.onreadystatechange = function () {
  // assign a function to handle state changes
  if (xhr.readyState === 4) {
    // check if the request is done
    if (xhr.status === 200) {
      // check if the response is OK
      console.log(xhr.responseText); // print the response text
      var users = JSON.parse(xhr.responseText); // parse the response text as JSON
      console.log(users); // print the users array
    } else {
      // handle other status codes
      console.log("Error: " + xhr.status); // print the error status
    }
  }
};
```

This example handles the response by checking if the request is done and if the response is OK. If so, it prints and parses the response text as JSON. If not, it prints an error message.

## The fetch API

The fetch API is a modern and simpler way to make HTTP requests in JavaScript. It uses promises and async/await syntax to handle asynchronous operations. Promises are objects that represent future values or outcomes of asynchronous operations. Async/await syntax is a way to write asynchronous code in a synchronous manner.

To use the fetch API, we need to follow these steps:

- Call the `fetch` function with one or two parameters: the URL and an optional options object that contains information about the request, such as method, headers, body, etc. The `fetch` function returns a promise that resolves to a response object. For example:

```javascript
fetch("https://jsonplaceholder.typicode.com/users") // call fetch with URL
  .then(function (response) {
    // handle the response object
    console.log(response); // print the response object
    return response.json(); // return a promise that resolves to the response data as JSON
  })
  .then(function (users) {
    // handle the response data
    console.log(users); // print the users array
  })
  .catch(function (error) {
    // handle any errors
    console.log(error); // print the error
  });
```

This example calls fetch with a URL and handles the response object and the response data using the `then` method of the promise. The `then` method takes a function that runs when the promise is fulfilled and returns another promise. The `catch` method takes a function that runs when the promise is rejected and handles any errors.

- Alternatively, we can use the async/await syntax to write the same code in a simpler way. To use async/await syntax, we need to declare an async function using the `async` keyword and use the `await` keyword to wait for a promise to resolve. For example:

```javascript
async function fetchData() {
  // declare an async function
  try {
    // try to execute this block of code
    var response = await fetch("https://jsonplaceholder.typicode.com/users"); // wait for fetch to resolve and assign the response object to a variable
    console.log(response); // print the response object
    var users = await response.json(); // wait for response.json to resolve and assign the response data to a variable
    console.log(users); // print the users array
  } catch (error) {
    // catch any errors
    console.log(error); // print the error
  }
}

fetchData(); // call the async function
```

This example declares an async function and uses await to wait for fetch and response.json to resolve. It also uses a try/catch block to handle any errors.

## The axios Library

The axios library is a third-party library that provides a simple and elegant way to make HTTP requests in JavaScript. It supports both the XMLHttpRequest object and the fetch API, as well as other features such as interceptors, transformers, cancel requests, etc.

To use the axios library, we need to follow these steps:

- Install and import the axios library using npm or CDN. For example:

```javascript
// install axios using npm
npm install axios

// import axios in your JavaScript file
var axios = require("axios");

// or use CDN in your HTML file
<script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>
```

- Call the `axios` function or one of its aliases (`get`, `post`, `put`, `delete`, etc.) with one or two parameters: the URL or a config object that contains information about the request, and an optional data object that contains the data to send to the server. The `axios` function returns a promise that resolves to a response object. For example:

```javascript
axios("https://jsonplaceholder.typicode.com/users") // call axios with URL
  .then(function (response) {
    // handle the response object
    console.log(response); // print the response object
    console.log(response.data); // print the response data
  })
  .catch(function (error) {
    // handle any errors
    console.log(error); // print the error
  });

// or use an alias method with a config object
axios.get("https://jsonplaceholder.typicode.com/users", {
  // call axios.get with URL and config object
  params: {
    id: 1, // add query parameters to the URL
  },
})
  .then(function (response) {
    // handle the response object
    console.log(response); // print the response object
    console.log(response.data); // print the response data
  })
  .catch(function (error) {
    // handle any errors
    console.log(error); // print the error
  });
```

This example calls axios with a URL and handles the response object and the response data using the `then` method of the promise. It also uses an alias method with a config object to add query parameters to the URL.

- Alternatively, we can use the async/await syntax to write the same code in a simpler way. For example:

```javascript
async function fetchData() {
  // declare an async function
  try {
    // try to execute this block of code
    var response = await axios("https://jsonplaceholder.typicode.com/users"); // wait for axios to resolve and assign the response object to a variable
    console.log(response); // print the response object
    console.log(response.data); // print the response data

    // or use an alias method with a config object
    var response = await axios.get("https://jsonplaceholder.typicode.com/users", {
      // wait for axios.get to resolve and assign the response object to a variable
      params: {
        id:
---
Sure, I can create a markdown file for a tutorial from digipodium on how to use JavaScript to communicate with the server, such as using the XMLHttpRequest object, using the fetch API and axios. Here is the file content:

# How to Use JavaScript to Communicate with the Server

JavaScript is a scripting language that can run in web browsers and other environments. It can be used to create dynamic and interactive web pages, as well as other applications. One of the most common uses of JavaScript is to communicate with the server, which is a computer that hosts and delivers data and resources over the internet. By communicating with the server, JavaScript can send requests, receive responses, and update the web page without reloading it. This makes the web page more responsive and user-friendly.

In this tutorial from digipodium, we will learn how to use JavaScript to communicate with the server, such as using the XMLHttpRequest object, using the fetch API and axios.

## The XMLHttpRequest Object

The XMLHttpRequest object is a built-in object that allows JavaScript to make HTTP requests to the server. HTTP (Hypertext Transfer Protocol) is a protocol that defines how messages are formatted and transmitted over the internet. HTTP requests are messages that contain information about what data or resource is requested from the server. HTTP responses are messages that contain information about what data or resource is returned from the server.

To use the XMLHttpRequest object, we need to follow these steps:

- Create a new XMLHttpRequest object using the `new` keyword and the `XMLHttpRequest` constructor. For example:

```javascript
var xhr = new XMLHttpRequest(); // create a new XMLHttpRequest object
```

- Open the request using the `open` method of the XMLHttpRequest object. The `open` method takes three or four parameters: the HTTP method, the URL, an optional boolean value that indicates whether to make an asynchronous or synchronous request, and an optional username and password for authentication. The HTTP method is a string that specifies what action to perform on the server, such as "GET", "POST", "PUT", "DELETE", etc. The URL is a string that specifies the location of the data or resource on the server. The asynchronous or synchronous request determines whether to wait for the response before executing the next line of code or not. By default, it is `true`, which means asynchronous. For example:

```javascript
xhr.open("GET", "https://jsonplaceholder.typicode.com/users"); // open a GET request to get users data from a fake API
```

- Send the request using the `send` method of the XMLHttpRequest object. The `send` method can take an optional parameter that contains the data to send to the server. For example:

```javascript
xhr.send(); // send the request without any data
```

- Handle the response using the `onreadystatechange` property and the `readyState` and `status` properties of the XMLHttpRequest object. The `onreadystatechange` property is an event handler that runs when the state of the request changes. The `readyState` property is a number that indicates the current state of the request, from 0 (uninitialized) to 4 (done). The `status` property is a number that indicates the status code of the response, such as 200 (OK), 404 (Not Found), 500 (Internal Server Error), etc. For example:

```javascript
xhr.onreadystatechange = function () {
  // assign a function to handle state changes
  if (xhr.readyState === 4) {
    // check if the request is done
    if (xhr.status === 200) {
      // check if the response is OK
      console.log(xhr.responseText); // print the response text
      var users = JSON.parse(xhr.responseText); // parse the response text as JSON
      console.log(users); // print the users array
    } else {
      // handle other status codes
      console.log("Error: " + xhr.status); // print the error status
    }
  }
};
```

This example handles the response by checking if the request is done and if the response is OK. If so, it prints and parses the response text as JSON. If not, it prints an error message.

## The fetch API

The fetch API is a modern and simpler way to make HTTP requests in JavaScript. It uses promises and async/await syntax to handle asynchronous operations. Promises are objects that represent future values or outcomes of asynchronous operations. Async/await syntax is a way to write asynchronous code in a synchronous manner.

To use the fetch API, we need to follow these steps:

- Call the `fetch` function with one or two parameters: the URL and an optional options object that contains information about the request, such as method, headers, body, etc. The `fetch` function returns a promise that resolves to a response object. For example:

```javascript
fetch("https://jsonplaceholder.typicode.com/users") // call fetch with URL
  .then(function (response) {
    // handle the response object
    console.log(response); // print the response object
    return response.json(); // return a promise that resolves to the response data as JSON
  })
  .then(function (users) {
    // handle the response data
    console.log(users); // print the users array
  })
  .catch(function (error) {
    // handle any errors
    console.log(error); // print the error
  });
```

This example calls fetch with a URL and handles the response object and the response data using the `then` method of the promise. The `then` method takes a function that runs when the promise is fulfilled and returns another promise. The `catch` method takes a function that runs when the promise is rejected and handles any errors.

- Alternatively, we can use the async/await syntax to write the same code in a simpler way. To use async/await syntax, we need to declare an async function using the `async` keyword and use the `await` keyword to wait for a promise to resolve. For example:

```javascript
async function fetchData() {
  // declare an async function
  try {
    // try to execute this block of code
    var response = await fetch("https://jsonplaceholder.typicode.com/users"); // wait for fetch to resolve and assign the response object to a variable
    console.log(response); // print the response object
    var users = await response.json(); // wait for response.json to resolve and assign the response data to a variable
    console.log(users); // print the users array
  } catch (error) {
    // catch any errors
    console.log(error); // print the error
  }
}

fetchData(); // call the async function
```

This example declares an async function and uses await to wait for fetch and response.json to resolve. It also uses a try/catch block to handle any errors.

## The axios Library

The axios library is a third-party library that provides a simple and elegant way to make HTTP requests in JavaScript. It supports both the XMLHttpRequest object and the fetch API, as well as other features such as interceptors, transformers, cancel requests, etc.

To use the axios library, we need to follow these steps:

- Install and import the axios library using npm or CDN. For example:

```javascript
// install axios using npm
npm install axios

// import axios in your JavaScript file
var axios = require("axios");

// or use CDN in your HTML file
<script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>
```

- Call the `axios` function or one of its aliases (`get`, `post`, `put`, `delete`, etc.) with one or two parameters: the URL or a config object that contains information about the request, and an optional data object that contains the data to send to the server. The `axios` function returns a promise that resolves to a response object. For example:

```javascript
axios("https://jsonplaceholder.typicode.com/users") // call axios with URL
  .then(function (response) {
    // handle the response object
    console.log(response); // print the response object
    console.log(response.data); // print the response data
  })
  .catch(function (error) {
    // handle any errors
    console.log(error); // print the error
  });

// or use an alias method with a config object
axios.get("https://jsonplaceholder.typicode.com/users", {
  // call axios.get with URL and config object
  params: {
    id: 1, // add query parameters to the URL
  },
})
  .then(function (response) {
    // handle the response object
    console.log(response); // print the response object
    console.log(response.data); // print the response data
  })
  .catch(function (error) {
    // handle any errors
    console.log(error); // print the error
  });
```

This example calls axios with a URL and handles the response object and the response data using the `then` method of the promise. It also uses an alias method with a config object to add query parameters to the URL.

This is the end of the tutorial. We hope you learned something useful from it. 😊
