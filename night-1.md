# JavaScript Cheat Sheet for Beginners

## Variables and Data Types
- Declaring a variable
```javascript
let name = "John";
```
- Declare a constant
```javascript
const pi = 3.14159;
```
- Types of data
```javascript
let string = "Hello"; // String
let number = 10; // Number
let boolean = true; // Boolean
let obj = {}; // Object
let array = []; // Array
let n = null; // Null
let notDefined; // Undefined
```

## Operators
- Arithmetic Operators
```javascript
let a = 10;
let b = 3;
console.log(a + b); // Addition
console.log(a - b); // Subtraction
console.log(a * b); // Multiplication
console.log(a / b); // Division
console.log(a % b); // Modulus
console.log(a ** b); // Exponentiation
```
- Assignment Operators
```javascript
let a = 10;
a += 3; // a = a + 3
a -= 3; // a = a - 3
a *= 3; // a = a * 3
a /= 3; // a = a / 3
a %= 3; // a = a % 3
```
- Comparison Operators
```javascript
let a = 10, b = 3;
console.log(a == b); // Equal to
console.log(a != b); // Not equal to
console.log(a === b); // Equal to in value and type
console.log(a !== b); // Not equal to in value or type
console.log(a < b); // Less than
console.log(a > b); // Greater than
console.log(a <= b); // Less than or equal to
console.log(a >= b); // Greater than or equal to
```
- Logical Operators
```javascript
let a = true, b = false;
console.log(a && b); // Logical AND
console.log(a || b); // Logical OR
console.log(!a); // Logical NOT
```

## Control Structures
- If-Else Statement
```javascript
if (condition) {
    // code to execute if condition is true
} else {
    // code to execute if condition is false
}
```
- Switch Statement
```javascript
switch(expression) {
    case x:
        // code block
        break;
    case y:
        // code block
        break;
    default:
        // code block
}
```
- For Loop
```javascript
for (let i = 0; i < 10; i++) {
    // code block to be executed
}
```
- While Loop
```javascript
while (condition) {
    // code block to be executed
}
```
- Do-While Loop
```javascript
do {
    // code block to be executed
} while (condition);
```
## Functions
- Declare a Function
```javascript
function functionName(parameters) {
    // code to be executed
}
```
- Call a Function
```javascript
functionName(arguments);
```
- Arrow Function
```javascript
let functionName = (parameters) => {
    // code to be executed
}
```
## Object
- Creating an Object
```javascript
let person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```
- Accessing Object Properties
```javascript
console.log(person.firstName);
console.log(person["lastName"]);
```
- Adding New Properties
```javascript
person.nationality = "English";
```
- Deleting Properties
```javascript
delete person.age;
```
-

 Checking for Property
```javascript
console.log('age' in person);
```
## Arrays
- Declare an Array
```javascript
let fruits = ["Apple", "Banana", "Mango"];
```
- Accessing Array Elements
```javascript
console.log(fruits[0]); // logs "Apple"
```
- Array Length
```javascript
console.log(fruits.length); // logs 3
```
- Array Methods
```javascript
fruits.push("Orange"); // adds a new element ("Orange") to fruits
fruits.pop(); // removes the last element from fruits
fruits.shift(); // removes the first element from fruits
fruits.unshift("Strawberry"); // adds a new element ("Strawberry") to the beginning of fruits
```
## Error Handling
- Try-Catch
```javascript
try {
    // code to try
} catch(err) {
    // code to handle errors
}
```
- Throw
```javascript
throw "Error2";   // String type
throw 42;         // Number type
throw true;       // Boolean type
throw {toString: function() { return "I'm an object!"; } };
```

These are the very basics. JavaScript is a powerful language and there are many more concepts and features to explore as you progress, such as promises, async/await, classes, modules, and much more!
