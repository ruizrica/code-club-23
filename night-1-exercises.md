**Exercises**

1. **Variable Declaration and Usage**
```javascript
let studentName = "John Doe";
console.log(studentName); // prints "John Doe" to the console
```

2. **Using a Conditional Statement (If-Else)**
```javascript
let age = 18;
if (age >= 18) {
    console.log("You are an adult.");
} else {
    console.log("You are a minor.");
}
```

3. **Creating and Using a Function**
```javascript
function calculateSquare(number) {
    return number * number;
}
console.log(calculateSquare(5)); // prints 25
```

4. **Using Loops (For Loop)**
```javascript
for (let i = 0; i < 5; i++) {
    console.log(i); // prints numbers from 0 to 4
}
```

5. **Creating and Manipulating an Array**
```javascript
let fruits = ["Apple", "Banana", "Mango"];
console.log(fruits.length); // prints 3
fruits.push("Orange"); // adds Orange to the array
console.log(fruits); // prints ["Apple", "Banana", "Mango", "Orange"]
```

6. **Creating and Using Objects**
```javascript
let student = {
    firstName: "John",
    lastName: "Doe",
    age: 18,
    greet: function() {
        return `Hello, my name is ${this.firstName} ${this.lastName}`;
    }
};
console.log(student.greet()); // prints "Hello, my name is John Doe"
```

7. **Using a Switch Case Statement**
```javascript
let day = 3; // Wednesday
switch(day) {
    case 0:
        console.log("Sunday");
        break;
    case 1:
        console.log("Monday");
        break;
    case 2:
        console.log("Tuesday");
        break;
    case 3:
        console.log("Wednesday");
        break;
    case 4:
        console.log("Thursday");
        break;
    case 5:
        console.log("Friday");
        break;
    case 6:
        console.log("Saturday");
        break;
    default:
        console.log("Invalid day!");
}
```

8. **Using a While Loop**
```javascript
let count = 0;
while (count < 5) {
    console.log(count); // prints numbers from 0 to 4
    count++;
}
```

9. **Displaying the Current Time of Day**
```javascript
let now = new Date();
let hours = now.getHours();
let minutes = now.getMinutes();
let seconds = now.getSeconds();
console.log(`Current time is: ${hours}:${minutes}:${seconds}`);
```
