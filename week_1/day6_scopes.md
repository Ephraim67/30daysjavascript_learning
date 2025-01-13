## Javascript Scopes
**What is Scope?**
Scope determines where a variable can be accessed in your code. Think of it like "visibility rules" for variables. 
There are different types of scope depending on where and how you declare a variable.

## Type of Scope in Javascript

1. Global Scope:
* Variables declared outside of any function or block (curly braces {}) are in the global scope.
* These variables can be accessed and modified from anywhere in your code.
* Example:
  ```javascript
  let globalVar = "I am global!";

  function printGlobal() {
    console.log(globalVar); // Accessible here
  }

  printGlobal();
  console.log(globalVar); // Accessible here too
  ```
2. Function Scope:
* Variables declared inside a function are only accessible within that function.
* They "disappear" once the function is finished.
* Example:
  ```javascript
  function greet() {
    let message = "Hello!";
    console.log(message); // Accessible here
  }

  greet();
  console.log(message); // Error! message is not defined
  ```
3. Block Scope
* A block is any code inside curly braces {} like in loops, conditionals, or functions.
* Variables declared with let or const inside a block can only be used inside that block.
* Example:
  if (true) {
    let blockVar = "I exist inside this block!";
    console.log(blockVar); // Accessible here
  }

  console.log(blockVar); // Error! blockVar is not defined
  ```
* Varable declared with ```var``` do not have block scope as they behave differently

4. Local Scope
* This is just another name for variables that are only accessible within a function (Function Scope).
* Example:
  ```javascript
  function addNumbers() {
    let sum = 5 + 3; // Local variable
    console.log(sum);
  }

  addNumbers();
  console.log(sum); // Error! sum is not defined
  ```
## Key Points About var, let, and const:
**var**:
* Does not respect block scope
* Limited to the function scope or global scope.
* Example:
  ```javascript
  if (true) {
    var x = "I am var";
  }
  console.log(x); // Accessible here!
  ```

**let** and **const**:
* Respect block scope
* Example:
  ```javascript
  if (true) {
    let y = "I am let";
  }
  console.log(y); // Error! y is not defined
  ```
## Summary
* Global Scope: Accessible everywhere.
* Function Scope: Accessible only inside the function.
* Block Scope: Accessible only inside the {} where it's defined (using let or const).





