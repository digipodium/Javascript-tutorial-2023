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

This is the end of the tutorial on basic syntax and data types of JavaScript. I hope you learned something useful from it. 😊
