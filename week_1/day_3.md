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
