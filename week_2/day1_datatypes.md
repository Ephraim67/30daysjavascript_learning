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

     
