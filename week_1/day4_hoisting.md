## What is Hoisting?
In JavaScript, hoisting is a behavior where declarations (for variables, functions, or classes) are "moved" to the top of their scope before
the code runs. This means you can use a variable or function before it's declared, without getting an error for the declaration itself.

## How Hoisting works:
1. Only Declarations Are Hoisted:
   - For variables: Only the declaration (var x;) is hoisted, not the assignment (x = 10;).
   - For functions: The entire function declaration is hoisted.
   - For classes: Declarations are hoisted but are not initialized.
2. Execution Order Matters
Even though the declarations are moved to the top of the scope, assignments or initializations stay where they are in the code.

3. Examples of Hoisting
Variable Hoisting with ```var```
```javascript
console.log(x); // Prints: undefined
var x = 10;     // Declaration is hoisted, but the value assignment stays here
console.log(x); // Prints: 10
```

**What happens here?**
 - During hoisting, JavaScript treats the code as if it were written like this
```javascript
var x;        // Declaration is hoisted
console.log(x); // Prints: undefined (x is declared but not assigned yet)
x = 10;       // Assignment happens here
console.log(x); // Prints: 10
```

**Function Hoisting**
Functions declared with the function keyword are hoisted entirely, meaning you can call them before they are defined.
```javascript
greet(); // Prints: "Hello!"
function greet() {
    console.log("Hello!");
}
```

**What happens here?**
The function declaration is hoisted to the top, so JavaScript acts as if the code was written like this:
```javascript
function greet() {
  console.log("Hello");
}
greet(); // Prints: "Hello!"

**```let``` and ```const``` Hoisting**
Variables declared with ```let``` or ```const``` are also hoisted, but they are not initialized. This means you cannot use them before their declaration.

```javascript
console.log(a); // Error! Cannot access 'a' before initialization
let a = 5;
```

**Why does this happen?**
Variables declared with ```let``` or ```const``` are in a "temporal dead zone" from the start of the block until their declaration is encountered. 
They are hoisted but not usable until the code reaches the declaration.

**Class Hoisting**
Classes behave like ```let``` and ```const```. They are hoisted but are not initialized, so you cannot use them before their declaration.

```javascript
const obj = new Person(); // Error! Cannot access 'Person' before initialization
class Person {
    constructor() {
        this.name = "John";
    }
}
```

**Key Points to Remember**
1. Only declarations are hoisted, not initializations.
   - With var, the variable is hoisted but is initialized to undefined.
   - With let and const, the variable is hoisted but not initialized (so it throws an error if used before declaration).
   - With functions, the entire function body is hoisted.
2. Avoid relying on hoisting
Hoisting can make code confusing. It's better to always declare variables and functions before you use them.

**Best Practices**
1. Use let and const instead of var to avoid unexpected behaviors caused by hoisting.
2. Declare all variables and functions at the top of their scope to make your code easier to read and understand.
3. Don’t call functions or use variables before their declarations.

**Visualization of Hoisting**
```javascript
console.log(a); // undefined (var is hoisted)
var a = 10;

console.log(b); // Error! Cannot access 'b' before initialization
let b = 20;

greet(); // Works fine because function declarations are hoisted
function greet() {
    console.log("Hello!");
}

const obj = new Person(); // Error! Cannot access 'Person' before initialization
class Person {
    constructor() {
        this.name = "John";
    }
}
```
