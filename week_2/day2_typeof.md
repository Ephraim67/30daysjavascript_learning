The **`typeof` operator** in JavaScript is used to determine the **data type** of a variable or value. It evaluates and returns a string describing the type of the operand (the value or variable being tested).

### How it works:
- The syntax is:  
  ```javascript
  typeof operand
  ```

- The result is a **string** indicating the type of the operand.

### Examples:

1. **Numbers**  
   ```javascript
   let age = 25;
   console.log(typeof age); // Displays: "number"
   ```

2. **Strings**  
   ```javascript
   let name = "Alice";
   console.log(typeof name); // Displays: "string"
   ```

3. **Booleans**  
   ```javascript
   let isLoggedIn = true;
   console.log(typeof isLoggedIn); // Displays: "boolean"
   ```

4. **Undefined**  
   ```javascript
   let x;
   console.log(typeof x); // Displays: "undefined" (no value assigned)
   ```

5. **Objects**  
   ```javascript
   let person = { name: "John", age: 30 };
   console.log(typeof person); // Displays: "object"
   ```

6. **Functions**  
   ```javascript
   let greet = function() { return "Hello!"; };
   console.log(typeof greet); // Displays: "function"
   ```

7. **Arrays**  
   ```javascript
   let fruits = ["apple", "banana"];
   console.log(typeof fruits); // Displays: "object" (arrays are a type of object)
   ```

8. **Null**  
   ```javascript
   let value = null;
   console.log(typeof value); // Displays: "object" (this is a known quirk in JavaScript)
   ```

9. **Symbols** (introduced in ES6)  
   ```javascript
   let symbol = Symbol("id");
   console.log(typeof symbol); // Displays: "symbol"
   ```

10. **BigInt** (introduced in ES2020 for very large integers)  
    ```javascript
    let bigNumber = 123456789012345678901234567890n;
    console.log(typeof bigNumber); // Displays: "bigint"
    ```

### Notes:
- `typeof` works well for most data types but has a **quirk** with `null`, which returns `"object"` instead of `"null"`. This is a historical issue in JavaScript.  
- Use `Array.isArray()` to specifically check if a value is an array.

This operator is very handy for debugging or writing code that needs to adapt based on the type of a variable!
