---
layout: cover
title: Circle 14
class: center middle
background: https://raw.githubusercontent.com/mdn/content/main/files/en-us/web/api/document_object_model/dom_tree.png

/* Global Style for Dark Background */.theme {background: linear-gradient(135deg, #1a1a1a, #333333); /* Dark gradient background */ color: #fff; /* White text for contrast */
transition: background 0.5s ease, color 0.5s ease; /* Smooth transition for background and text color */}

/* Slide Transition Effects */.slide { transition: transform 0.5s ease-in-out, opacity 0.5s ease-in-out; /* Smooth transition when changing slides */}
---

# Circle 14 Presentation 
---
class: text-center
---

# **JavaScript Class Summary**
---
transition: fade-out
---

# Table of Contents

1. [Introduction to JavaScript](#/intro)
2. [Data Types](#/data-types)
   - [Number](#/number)
   - [String](#/string)
   - [Object](#/object)
3. [Function](#/function)
4. [Array](#/array)
5. [Loops] (#Loops)
6. [DOM & Event Handling](#/dom-event)
7. [Modules](#/modules)

---
## id: intro
---
## Introduction to JavaScript

- JavaScript is a versatile programming language for web development.
- It runs in the browser and enables interactive features.
- Created by Brendan Eich in 1995.
- Evolved into modern frameworks like React, Vue, and Angular.

---
## id: data-types
---
## Data Types

JavaScript has several core data types, including:
---
transition: fade-out
---
- **Primitive Types**: Number, String, Boolean, Null, Undefined, Symbol
- **Reference Types**: Objects, Arrays, Functions

---
## id: number
---
# Number

They can be used in calculations and can include both integers (whole numbers) and floating-point numbers (decimals).
---
transition: fade-out
---
**Number Types**

- **Integers**: Whole numbers without decimals
- **Floating-point numbers**: Numbers with decimals

```js
let integer = 35;
let float = 4.57;
```

**Special numeric values:** e.g. NaN and Infinity

- NaN (Not a number): Represents an invalid or unreliable numeric result.

```js
let result = "hello" * 2;
console.log(result); // NaN
```

---
transition: fade-out
---
- Infinity: we have the positive infinity that represents a value that is greater than any other number and negative infinity that represents a value that is less than any other number.

```js
let a = 1
let b = 0
console.log (a/b); // Infinity

let a = -1
let b = 0
console.log (a/b); // -Infinity
```

---
transition: fade-out
---
# Number operations

Refers to ways you can manipulate and work with numbers. Below are the most common number operations in JavaScript using arithmetic operators like +, -, \*, /, %

Note an **operator** is a received syntax consisting of punctuation or alphanumeric characters that carries out built in functionalities while **operands** are the values the operator works on

       operator
           |
       20  +  7
       |      |
       operands

```js
let a = 20;
let b = 7;

console.log(a + b); // 27
console.log(a - b); // 13
console.log(a * b); // 140
console.log(a / b); // 2.857142857142857
console.log(a % b); // 6
```

---

- Numeric separator (\_) : They are used to improve readability of large numbers in JavaScript.

```js
let largeNumber = 1_000_000_000; // equivalent to 1000000000
console.log (largeNumber); // Output: 1000000000
```

They don't affect the value of the number but are just there to make the number easier to read.

```js
let float = 3.141_59; // No impact on the value
console.log(float); // 3.14159
```

- Number.parseInt(): Converts a string into an integer by removing any decimal point. It reads from left to right until it hits something that isn’t a number and then stops.

```js
let x = Number.parseInt("100px"); // 100
let y = Number.parseInt("3.14"); // 3
let z = Number.parseInt("Hello 12"); // NaN (can't convert text/can’t read if it starts with text)
```

- Number.parseFloat (): reads the string and keeps the decimal part if it exists.

```js
let x = Number.parseFloat("100.50px"); // 100.5 (reads until it sees non-numeric)
let y = Number.parseFloat("3.14"); // 3.14
let z = Number.parseFloat("Hello 12"); // NaN (no valid number to start with)
```


---
transition: fade-out
---
- .toString(): This is a method you can use to turn a number into text (a string).

```js

let age = 25;
let ageText = age.toString();
console.log(ageText); // "25"
console.log(typeof ageText); // string
```
You use .toString() when you need to:

- Display numbers as text (like in a sentence or on a webpage).
- Format output, like showing "You have 5 new messages"

---
transition: fade-out
---

# Introduction to Strings
---

JavaScript Strings

A string is a sequence of characters used to represent text.

```javascript
let greeting = "Hello, world!";
```

Strings are primitive data types in JavaScript.  
They can be defined using:

- "double quotes"  
- 'single quotes'  
- `backticks` (template literals)
---
transition: fade-out
---

# Creating Strings

Creating Strings

```javascript
let single = 'Hello';
let double = "World";
let backtick = `Hey there!`;
```

Use backticks for template literals.  
Mixing quotes inside each other:

```javascript
let mix = "It's a nice day";
```

---
transition: flip
---

# Escape Characters

Escape Characters

Use backslashes (\) for special characters inside strings.

```javascript
let quote = "He said, \"Hello!\"";
let newline = "First line\nSecond line";
```

- \n – new line  
- \t – tab  
- \\ – backslash

---
transition: cube
---

#  Common String Methods

Useful String Methods

```javascript
let text = "  JavaScript is fun!  ";
```

| Method                   | Description                |
| ------------------------ | -------------------------- |
| `text.length`            | Total characters           |
| `text.trim()`            | Removes whitespace         |
| `text.toLowerCase()`     | Converts to lowercase      |
| `text.toUpperCase()`     | Converts to uppercase      |
| `text.includes("fun")`   | Checks if "fun" exists     |
| `text.indexOf("Script")` | Finds position of "Script" |

---

# More String Methods

More String Methods

```javascript
let str = "JavaScript";
```

| Method                        | Example                     | Result                   |
| ----------------------------- | --------------------------- | ------------------------ |
| `str.slice(0, 4)`             | Returns "Java"              | "Java"                   |
| `str.substring(4)`            | From position 4 onward      | "Script"                 |
| `str.replace("Java", "Type")` | Replaces "Java" with "Type" | "TypeScript"             |
| `str.repeat(2)`               | Repeats the string twice    | "JavaScriptJavaScript"   |

---

# Template Literals

Template Literals

Template literals (`) allow:

- Variable interpolation  
- Multi-line strings

```javascript
let name = "Sam";
let mood = "excited";
let message = `Hi ${name}, you're looking ${mood} today!`;
```

Cleaner and more readable than string concatenation.

---

# String Immutability

String Immutability

Strings in JavaScript are immutable

```javascript
let word = "hello";
word[0] = "H";  // This won't work
```

To "change" a string, create a new one:

```javascript
word = "H" + word.slice(1);  // "Hello"
```

---

# String Conversion

String Conversion

Convert other data types to strings using:

```javascript
String(123);      // "123"
(456).toString(); // "456"
```

Useful for:

- Concatenating numbers with strings  
- Preparing data for display
---

# ARRAYS 
An array is a data structure that stores a collection of elements of the same data type in contiguous memory locations, meaning they are stored next to each other. Each element in the array can be accessed using its index, which is a numerical identifier starting from 0.

```js
 let fruits = ["apple", "banana", "cherry"];
console.log(fruits[0]); // prints "apple"
console.log(fruits[1]); // prints "banana"
console.log(fruits[2]); // prints "cherry"

let fruits = ["apple", "banana", "orange"];

``` 

## Here

```js
  •	fruits[0] is "apple"
	•	fruits[1] is "banana"
	•	fruits[2] is "orange"
```
---

## Key features

Can store multiple values (numbers, strings, objects, etc.)
You can add, remove, update, or loop through values

**reduce()** <br>
Reduces an array to a single value by applying a function accumulatively.

Example 

```js

let numbers = [1, 2, 3, 4];
let sum = numbers.reduce((accumulator, current) => accumulator + current, 0);
console.log(sum); // 10

```

**includes()** <br>

	Returns true if the array contains a certain value; otherwise false.

Example 

```js 

let fruits = ["apple", "banana", "orange"];
console.log(fruits.includes("banana")); // true
console.log(fruits.includes("grape")); // false

```

---

**push()** <br>

Adds one or more elements to the end of an array and returns the new length.

For example 

```js
let colors = ["red", "green"];
colors.push("blue");
console.log(colors); // ["red", "green", "blue"]

```


**map()** <br>

It changes every item in an array and gives you a new array with the changed items.
Example:
Imagine you have numbers and you want to add 1 to each:

Example: 
```js 

let numbers = [1, 2, 3];
let newNumbers = numbers.map(num => num + 1);
console.log(newNumbers); // [2, 3, 4]

```

---


**filter()**  <br>

It keeps only the items you want from an array.
E.G
Example

```js

let numbers = [3, 6, 8, 2];
let bigNumbers = numbers.filter(num => num > 5);
console.log(bigNumbers); // [6, 8]

```

***find()*** <br>
It finds the first item that matches what is being searched   for.

Example:
Let’s find the first number bigger than 4:

```js

let numbers = [1, 3, 5, 7];
let firstBig = numbers.find(num => num > 4);
console.log(firstBig); // 5

```

---

***every()*** <br>

Checks if all items in the array pass a test (all must be true).
Eg
Are all numbers on the greater than 0 

```js

let numbers = [1, 2, 3];
let allPositive = numbers.every(num => num > 0);
console.log(allPositive); // true

let numbers = [1, 2, 3];
let allPositive = numbers.every(num => num > 5);
console.log(allPositive); // false

```


***some()***  <br>
Checks if at least one item passes the test (only one needs to be true).

Example:
Is there any number bigger than 5?

```js

let numbers = [2, 4, 7];
let hasBig = numbers.some(num => num > 5);
console.log(hasBig); // true

```

---

***splice()***  <br>
Lets you remove or add items in the middle of the array.

Example 

```js 
let fruits = ["apple", "banana", "orange"];
fruits.splice(1, 1); // remove 1 item at index 1
console.log(fruits); // ["apple", "orange"]

let fruits = ["apple", "banana",”mango”, "orange"];
fruits.splice(1, 1); // remove 2 item at index 1
console.log(fruits); // ["apple", "orange"]

```

---


***forEach()***
 is an array method in JavaScript that executes a provided function once for each array element. It does not return a new array (unlike map() or filter()); it simply runs a function for every item in the array.

Example 

```js

et numbers = [10, 20, 30];
numbers.forEach(function(num) {
   console.log(num);
});
Output:
10
20
30

```
---
# OBJECT

Objects are data types used to store data in key value pair. Each key also called a property maps to a value, which can be of any type including a primitive, object or function.

Examples :
```js
 let person = {
  name: “Tayo”,
age: 18,
isFemale: true

}:
```
---
# There are two ways to create an object 

1. Using the object () constructor: This is rarely used

Example 
```js
let user = new Object();
 user.name = "Theo";
```
2. Using object literal syntax: This is commonly used

Example 
```js
 let person = {};
 ```
---

# Accessing the object properties 

In order to access the property of an object, we can use two methods 

1. Dot notation: it’s commonly used to access object property

Examples 
```js
console.log(person.name);
 //Output
“Tayo”
```
2. Bracket notation: This is required if the key is dynamic or not a valid identifier.

Example 
```js
Console.log(person[“age”]);

//Output:

“18”
```
---

# Adding a property 

This is giving an existing object a brand new key and value.

Example 
```js
obj.newKey = newValue;
obj[“newKey”] = newValue;

//dot notation
person.school = "AltSchool";      

//bracket notation
 person["takesStudent"] = false;
```
---

#  Modifying a property

This is used in changing the value stored under an existing key. 

Example 
```js
  const user = { name: "Maxwell" };

  user.name = "Maxwell Emma";
```
---
# Deleting a property  

This is used in removing a key value pair entirely from the object. 

Example 
```js
delete person.takesStudent;
```
---

# Nested object

Objects can contain other objects or arrays

Example 
```js
 let student = {

  name: "Albert",

scores: {
 physics: 80,
 english: 90

  }

};

console.log(student.scores.english);

   //Output

    90
    ```
---
# Object with methods

A method is a function defined inside an object. 

Example 
```js
     let person = {

     name: “David”,

  greet: function() {

    return "Hello, " + this.name;

    }

   };

console.log(person.greet()); 
 //output 
 Hello, David
```

# this keyword in object 

This refers to the object that is calling the method. It’s common used inside methods to refer to the current object properties.

Example 
```js
       let profile = {

     username: "Ozeni",

     show() {

    console.log(`Hi, I'm ${this.username}`);

    }

    };

    profile.show(); 

   //output 

   Hi, I'm Ozeni
```
---

# Functions in JavaScript

Functions are blocks of code designed to perform a particular task.  
They help organize and reuse code in a program.  
A function can accept input (parameters), perform operations, and return an output.

---

## Function Declaration

Functions are declared using the `function` keyword. They can take parameters and return values.

```js
function greet(name) {
  return `Hello, ${name}!`;
}
console.log(greet('Alice'));
```

**Output:**  
Hello, Alice!

---

## Basic Functions

Functions allow for reusable logic, like this simple addition example.

```js
function add(a, b) {
  return a + b;
}
console.log(add(2, 3));
```

**Output:**  
5

---

## Arrow Functions

Arrow functions are a concise way to write functions, introduced in ES6.

```js
const multiply = (a, b) => a * b;
console.log(multiply(4, 5));
```

**Output:**  
20

---

## Default Parameters

You can define default values for parameters, which are used if no argument is provided.

```js
function bookRoom(roomType = 'Standard') {
  return `Room booked: ${roomType}`;
}
console.log(bookRoom());
```

**Output:**  
Room booked: Standard

---

## Optional Chaining

Optional chaining allows safe access to nested object properties without causing errors.

```js
const user = { profile: { name: 'Bob' } };
console.log(user?.profile?.name);
console.log(user?.contact?.email);
```

**Output:**  
Bob  
undefined

---

## Asynchronous Functions

`async` and `await` simplify asynchronous operations and make them easier to read.

```js
async function fetchData() {
  const response = await fetch('https://api.example.com/data');
  const data = await response.json();
  console.log(data);
}
fetchData();
```

---

## Callback Pattern

Before async/await, callbacks were used to handle asynchronous code.

```js
function getUserData(callback) {
  setTimeout(() => {
    callback({ name: 'Jane' });
  }, 1000);
}
getUserData(user => console.log(user.name));
```

**Output:**  
Jane (after 1 second)

---

## Closures

Closures allow functions to retain access to their lexical scope even after the outer function has executed.

```js
function makeCounter() {
  let count = 0;
  return function() {
    count++;
    return count;
  };
}
const counter = makeCounter();
console.log(counter());
```

**Output:**  
1

---

## Lexical Scope

Lexical scope defines how variable names are resolved in nested functions.

```js
function outer() {
  let outerVar = 'I am outer';
  function inner() {
    console.log(outerVar);
  }
  return inner;
}
const innerFunc = outer();
innerFunc();
```

**Output:**  
I am outer

---

## Hoisting

Hoisting allows function declarations to be used before they are defined in the code.

```js
console.log(square(3));
function square(x) {
  return x * x;
}
```

**Output:**  
9

---

## Passing Functions as Arguments

Functions can be passed as arguments, enabling high-order functions.

```js
function logGreeting(fn) {
  console.log(fn('Charlie'));
}
logGreeting(name => `Hello, ${name}!`);
```

**Output:**  
Hello, Charlie!

---

## Implicit Return (Arrow Functions)

Arrow functions can return values implicitly if they consist of a single expression.

```js
const isEven = num => num % 2 === 0;
console.log(isEven(4));
```

**Output:**  
true

---

## Generator Functions

Generator functions use `yield` to pause and resume execution, producing a series of values.

```js
function* idGenerator() {
  let id = 1;
  while (true) {
    yield id++;
  }
}
const gen = idGenerator();
console.log(gen.next().value);
console.log(gen.next().value);
```

**Output:**  
1  
2

---

## Yield Keyword

The `yield` keyword pauses a generator function and returns a value to the caller.

```js
function* fruitList() {
  yield 'Apple';
  yield 'Banana';
  yield 'Cherry';
}
const fruits = fruitList();
console.log(fruits.next().value);
console.log(fruits.next().value);
```

**Output:**  
Apple  
Banana

---

## yield* Delegation

`yield*` allows a generator to delegate part of its iteration process to another generator.

```js
function* numbers() {
  yield 1;
  yield 2;
}

function* moreNumbers() {
  yield* numbers();
  yield 3;
}
const genNums = moreNumbers();
console.log(genNums.next().value);
console.log(genNums.next().value);
console.log(genNums.next().value);
```

**Output:**  
1  
2  
3

<PoweredBySlidev mt-10 />
