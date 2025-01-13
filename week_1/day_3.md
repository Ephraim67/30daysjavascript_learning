## All About javascript

**var** Statement
* What it does: The var keyword declares a variable. A variable is like a container that holds data (e.g., a number, text, etc.).
  You can name the container and change its contents later.

**Scope (Where it works):**
* If you declare it inside a function, it can only be used in that function (this is called "function-scoped").
* If you declare it outside a function, it becomes globally available and can be used anywhere in your script.

**Example**
```javascript
var name = "john"; //Declare a variable and assign a value to it
console.log(name); //Prints: john

if (true) {
    var age = 30; // this variable is accessible even outside of this block

}

console.log(age);
```

**Key points**:
var doesn't care about blocks like if or for—the variable is still accessible outside those blocks (which can cause bugs).

**let** Declaration
* What it does: The let keyword is a more modern way to declare variables. It also lets you store data in a container, but it is better at controlling where the variable can be used.
* Scope (Where it works): ```let``` is block-scoped, which means it only works within the block where it is declared (like inside ```{}```). Blocks are defined by ```{}``` in code.
* Example:
  ```javascript
  let name = "Alice"; // Declare a variable with 'let'
  console.log(name); // Prints: Alice

  if (true) {
      let age = 25; // This variable exists only inside this block
      console.log(age); // Prints: 25
  }
  console.log(age);  // Error! 'age' is not accessible here
  ```

**Key points** ```let``` avoids the problem of accidentally using variables outside their intended block. It's safer than ```var```.

**const** Declaration
* What it does: The ```const``` keyword is used to declare variables whose value cannot be changed. Once you assign a value, you can't reassign it with a new value.
* Scope (Where it works): Like ```let```, const is block-scoped. It works only in the block where you declare it.
* Rules for const:
  - You must assign a value when you declare it.
  - You cannot reassign the variable later.
* Example:
  ```javascript
  const PI = 3.14; // Declare a constant
  console.log(PI); // Prints: 3.14
  ```

// Trying to change its value will throw an error
// PI = 3.1415; // Error! You can't reassign a constant
* Special Case for Objects and Arrays: If you use const for an object or an array, you can't replace the entire object or array, but you can modify its contents.
* Example:
```javascript
const person = { name: "John", age: 30 };
person.name = "Alice"; // You can update a property
console.log(person); // Prints: { name: "Alice", age: 30 }
```

// But you can't reassign the entire object
// person = { name: "Bob" }; // Error!

**Key Takeaways**
**var:**
* Use it only if you need a function-scoped variable.
* Avoid it in modern code because it can cause unexpected issues due to its behavior.

**let:**
* Use for variables that you plan to reassign later.
* Safer than var because it's block-scoped.

**const:**
* Use for values that won't change.
* Great for constants like PI, or objects/arrays you don't want to replace.

```javascript
var x = 50; // Global or function-scoped
let y = 20; // Block-scoped
const z = 30; // Block-scoped and immutable

if (true) {
  var x = 50; // Updates the global 'x
  let y = 60; // Only in this block
  // z = 100; // Error! You can't reassign 'z'
}
console.log(x) // Prints: 50
console.log(y); // Prints: 20
```

