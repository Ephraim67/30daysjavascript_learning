## What is a Data Type?
* When you create a variable in JavaScript, it holds data. The type of that data (like a number, text, or true/false value) is called its 
  data type.
* Think of a variable like a container, and the data type tells you what kind of thing is inside that container.

* Types of Data in JavaScript: There are two types of data in javascript
1. Primitive data types: These are simple, single values. They are not objects, and they are immutable (cannot be changed).
   There are 7 primitive data types:
   - Number: Used to represent numbers (both integers and decimals).
     ```javascript
     let age = 15; // a whole number
     let price = 19.99; // A decimal number
     ```
   - BigInt: Used for very large numbers (bigger than the safe limit for regular numbers).
     ```javascript
     let bignumber = 1234567890123456789012345678901234567890n;
     ```
   - String: Used for text or a sequence of characters, strings are writting inside of a ```" "``` or ```' '``` or ``` ` ` ```
     ```javascript
     let name = "Alice"; // Double quote
     let greeting = 'Hello!'; // Single quote
     let message = `Welcome, ${name}`; // Backticks allow embedding variables
     ```

   - Boolean: Used for True/False values
     ```javascript
     let isJavaScriptFun = true;
     let isSkyfun = false;
     ```
   - Null: Represents "nothing" or "empty", You can assign null to a variable when you want it to have no value.
     ```javascript
     let job = null; // Job is intentionally set to "nothing"
     ```
   - Undefined: A variable that is declared but has not been given a value is undefined.
     ```javascript
     let color;
     console.log(color); // Output: undefined
     ```
   - Symbol: Represents a unique value. Symbols are often used as unique object keys.
     ```javascript
     let uniqueID = Symbol('id');
     console.log(uniqueID); // Output: Symbol(id)
     ```

2. Non-Primitive Data Types: These are more complex types, and they include Objects.
   - Objects: can store multiple values in key-value pair
     ```javascript
     let person = {
         name: "John";
         age = 30;
         isStudent: false;
     };
     console.log(person.name); // Output: John
     console.log(person.age); // Output: 30
     ```
   - Prototype: Every JavaScript object has a hidden, built-in property called [[Prototype]].
     This is like a blueprint that provides access to methods and properties from another object.
     ```javascript
     let anmal = {
         eats: true;
         walk() {
           console.log("Animal walks");
         }
     };

     let dog = {
         barks() {
           console.log("Dog barks");
         }
     };
     // Set `animal` as the prototype of `dog`
     dog.__proto__ = animal;

     dog.bark(); // Output: Dog barks
     dog.walk(); // Output: Animal walks (inherited from animal)
   ```
- Prototypal Inheritence: Prototypal inheritance is how objects in JavaScript can "inherit"
  properties and methods from another object (their prototype). This makes it possible to reuse the code accrossmultiple objects.
  ```javascript
  let parent = {
      greet() {
        console.log("Hello from the parent!");
      }
  };

  let child = Object.create(parent); // `parent` becomes the prototype of `child`
      child.sayHi = function () {
          console.log("Hi from the child!");
  };

  child.greet(); // Output: Hello from the parent! (inherited)
  child.sayHi(); // Output: Hi from the child!
  ```

The Prototypal Inheritance is a feature in javascript used to add methods and properties in objects. It is a method by which an object can inherit the properties and methods of another object. Traditionally, in order to get and set the Prototype of an object, we use Object.getPrototypeOf and Object.setPrototypeOf.

- Built-in Objects in JavaScript are special objects provided by the language itself. They come "pre-installed" and are always available for you to use without needing to create them yourself or import anything.

These objects are often referred to as global objects because they can be accessed anywhere in your code. They provide useful functionality to help you work with numbers, text, dates, and more.

Here are some common examples of built-in objects:

1. Number
   Represents numbers and provides methods to work with them.
   ```javascript
   let num = 42;
   console.log(num.toFixed(2));// Displays: "42.00" (formats number with 2 decimal places)
   console.log(Number.isInteger(num)); // Displays: true (checks if it's an integer)
   ```
2. Math
   Provides constants and methods for mathematical operations.
   ```javascript
   console.log(Math.PI); // Displays: 3.141592653589793 (value of π)
   console.log(Math.sqrt(16)); // Displays: 4 (square root of 16)
   console.log(Math.random()); // Displays a random number between 0 and 1
   ```
3. Date
   Handles dates and times.
   ```javascript
      let now = new Date();
      console.log(now); // Displays the current date and time (e.g., "2025-01-26T08:45:00.000Z")
      console.log(now.getFullYear()); // Displays the current year (e.g., 2025)
   ```
5. String
   Represents and manipulates text.
   ```javascript
      let greeting = "Hello, world!";
      console.log(greeting.length); // Displays: 13 (length of the string)
      console.log(greeting.toUpperCase()); // Displays: "HELLO, WORLD!"
      console.log(greeting.includes("world")); // Displays: true (checks if "world" is in the string)
   ```
5. Error
   Used to handle errors.
   ```javascript
      try {
         throw new Error("Something went wrong!");
      } catch (error) {
        console.log(error.message); // Displays: "Something went wrong!"
      }
   ```
7. Function
   Represents functions and allows advanced operations.
   ```javascript
      let add = new Function('a', 'b', 'return a + b');
      console.log(add(5, 3)); // Displays: 8
   ```
7. Boolean
   Represents true or false values.
   ```javascript
   let isLoggedIn = true;
   console.log(isLoggedIn); // Displays: true
   console.log(Boolean(0)); // Displays: false (0 is considered "falsey" in JavaScript)
   ```
     
