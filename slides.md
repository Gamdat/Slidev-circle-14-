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
# # What is the Fetch API?

The **Fetch API** is a built-in JavaScript interface that allows you to **make network requests** (like getting data from or sending data to a server). It is **promise-based**, making it cleaner and easier to handle asynchronous code 

# **Basic Syntax**
``` js
 fetch(url, options)
  .then(response => {
    // handle the response
  })
  .catch(error => {
    // handle any errors
  })
;
```
## Making a GET Request
```  fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```
 # **Making a POST Request**
```js
fetch('https://api.example.com/data', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({ name: 'Gloria', job: 'VA' })
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error)); 
```

#### Common HTTP Methods with Fetch
* GET: Retrieve data.
* POST: Send data.
* PUT: Update data.
* DELETE: Remove data.

# ### Handling JSON Responses

To read a JSON response, use:

``` response.json() ```

# Other methods:
* response.text()
* response.blob()
* response.formData()

# **Setting Headers**
**Headers** are key-value pairs sent along with HTTP requests to give the server additional information (e.g., content type, authentication tokens).
``` js
headers: {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer token_here'
} 
```
 # ### Error Handling

Fetch only rejects on **network errors**, not on HTTP status codes like 404 or 500.
It only rejects on network failures. To handle HTTP errors, you need to check the response.ok property or the
To check status manually:
```js
 fetch('https://api.example.com/data')
  .then(response => {
    if (!response.ok) {
      throw new Error('Network response was not ok');
    }
    return response.json();
  }) 
```
# **Async/Await Version**
In JavaScript, the async/await syntax provides a modern and cleaner approach to managing asynchronous operations . It simplifies code readability.
```js
 async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    if (!response.ok) throw new Error('Request failed');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('Error:', error);
  }
} 
```

# ### Use Cases
* Fetching data from REST APIs
* Submitting form data
* Making authenticated requests
* Communicating with your own backend
---
# Loop
**LOOP**
                 **What is a Loop?**
A loop repeatedly executes a block of code as long as a condition is true. It’s useful for automating repetitive tasks.
Single execution of the loop body is called an iteration 
                             **Types of Loops**
1. **While loop**
This execute condition before code. Any condition or variable can be a loop condition, if ++ is missing then the loop repeat. This is mostly used when the number of iterations isn’t known beforehand.
```js
 let i = 0;
while (i < 5) {
  console.log(i);
  i++;
} 
```



2. **Do while loop**
This is similar to while loop but code run at least once before the loop start. Meaning it execute code before checking conditions.  Condition check is just moved below the loop body.
```js
 let i = 0;
do {
  console.log(i);
  i++;
} while (i < 5); 
```



3. **For loop**
This is more complex but it’s the most commonly used loop, this is best used when you know how many times to run the loop. Exit can be force anytime. 
```js
 for (let i = 0; i < 5; i++) {
  console.log(i);
} 
```



4. **For of loop**
It’s used to loop over iterable properties of an object, value of an iterable object can be counted e.g array, string.
```js
 let colors = ["red", "blue", "green"];
for (let color of colors) {
  console.log(color);
} 
```


P.S  For..of can’t be  use on objects unless they’re converted (e.g., using Object.values()).
---

# **EVENT**
What is an Event?
An event is any interaction or occurrence that happens in the browser,  like clicking a button, submitting a form, or pressing a key. JavaScript uses events to respond to user actions.
  
     **EXAMPLE OF EVENTS**
	1	Clicking a button
	2	Typing in a field 
	3	Moving the mouse
	4	Submitting a form
	5	Pressing a key

**COMMON EVENT TYPE**
| **Event Type** | **Description** |
|:-:|:-:|
| click | When a user clicks an element. |
| mouseover | When a mouse hovers over. |
| keydown | When a key is pressed. |
| submit | When a form is submitted. |
| load | When the page finishes loading. |

**Event Listener**
An event listener is a function that listens for a specific event and executes code when that event occurs.

```js
 element.addEventListener("eventType", callbackFunction);
 ```



**Event Handler**
An event handler is the function that is executed when an event occurs, it runs in response to an event. 
```js
 function greetUser() {
  console.log("Hello, Gloria!");
} 
```




**Why Use Events?**
* Makes web pages interactive.
* Allows dynamic content changes.
* Connects user input to application logic.

**Ways to Assign Event Handlers**
	1	 Assigning Handlers to DOM Properties (Inline or Direct)
You directly assign a function to an HTML element’s event property like .onclick.
Assign a handler to elem.onclick, not elem.ONCLICK, because DOM properties are case-sensitive.
```js let btn = document.getElementById("myBtn");
btn.onclick = function () {
  alert("Clicked!");
}; 
```


Note: this can only store one function at a time and it get replace when a new function is added by the new function. 
	**2	Using addEventListener()**                             Attaching multiple handlers to the same event, and it gives you more control. This is highly recommended.
```js
 btn.addEventListener("click", function () {
  alert("Hello from listener!");
}); 
```
 

Note:  Handlers can also be remove later with removeEventListener().

          **Event Object**
The event object is passed automatically to every event handler. It holds all the details about what happened.
```js
 btn.addEventListener("click", function (event) {
  console.log(event.type);
     //output
 "click"
  console.log(event.target); 
  //output
 The element that was clicked
}); 
```
 


**Common Properties of event objects :**
	1	event.type : Type  of event (“click”, “keydown”, etc.)
	2	event.target : This  element that triggered the event
	3	event.preventDefault() : This  stops default behavior
	4	event.stopPropagation() : This stops bubbling

**Object Handlers (Using Methods from an Object)**
A method of an object can be assigned as an event handler.
```js
 let handler = {
  message: "Hello!",
  show() {
    alert(this.message);
  }
};
btn.addEventListener("click", handler.show.bind(handler)); 
```
 


**Event Propagation**
Propagation is how events travel through the DOM. It happens in three phases:
	1.	Capturing phase : from the root down to the element.
	2.	Target phase : the event reaches the actual target.
	3.	Bubbling phase : event bubbles up from the target to the root.
``` parent.addEventListener("click", () => console.log("Parent clicked"));
child.addEventListener("click", () => console.log("Child clicked")); 
```
 


**Event Bubbling in JavaScript**
Event bubbling is a phase in where an event starts from the target element and bubbles up to its parent elements.
Almost all events bubble.
```js
 document.getElementById("child").addEventListener("click", () => {
  console.log("Child clicked");
}); 
document.getElementById("parent").addEventListener("click", () => {
  console.log("Parent clicked");
});
```





**UI Events**
These are events related to the user interface, they are related to user interaction with the web page or the browser window.
Example 
Resize
Load
Error
Focus/blur
Scroll

```js
 window.addEventListener("resize", function () {
  console.log("Window resized!");
}); 
```
 


**Event Capturing** 
Event capturing is the first phase of event propagation. The event starts from document and travels down the DOM tree to the target element before bubbling back up.
**How to use it:**
By default, addEventListener() listens during the bubbling phase. To catch it during the capturing phase, pass a third argument true.
```js
 document.getElementById("outer").addEventListener(
  "click",
  () => console.log("Outer - Capturing"),
  true // enable capturing
); 
```




  **FORM**
A form is an HTML element that collects user input. It usually contains inputs like text fields, checkboxes, radio buttons, and submit buttons.
**Form events**: This  respond to user interactions within form fields like inputs, checkboxes, or submission buttons. This allows you track user actions in a form.
```js
 form.addEventListener("submit", function (e) {
  e.preventDefault();
  console.log("Form submitted!");
}); 
```



**Form Submission**
By default, when a form is submitted:
* The browser reloads the page
* The form data is sent to the server via action/method.
To prevent this and handle it with JavaScript
```js
 form.addEventListener("submit", function (e) {
  e.preventDefault(); // Stops page reload
  console.log("Data captured with JS!");
}); 
```
 


**Form Attributes**
	**1	Action:** URl where form data should be sent
	2	Method: Get or Post
	3	Name: Name of the form or input 
	4	Required: Makes a field compulsory 
	5	Autocomplete: Helps a browser remember user input 

      **JavaScript Form Handling Flow**
	1.	Select the form with document.getElementById or similar.
	2.	Add submit event listener.
	3.	Use preventDefault() to stop real submission.
	4.	Access form fields using form.elements or input names.
	5.	Validate or send data with fetch() 







<PoweredBySlidev mt-10 />
