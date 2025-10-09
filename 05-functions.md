
## 05-functions.md

## JavaScript Functions 

- A function in JavaScript is a reusable block of code that performs a specific task.
Instead of writing the same code again and again, we can define it once in a function and then call it whenever needed.


### Functions help in:

- Code reusability

- Better organization

- Easy debugging

- Avoiding repetition


### Function Syntax 

```ts

function functionName(parameters) {
  // code to be executed
  return result; // optional
}

```
- function → keyword to declare a function

- functionName → name of the function

- parameters → input values (optional)

- return → sends back a value (optional)


### Example 1. Simple Function 

```ts

function greet() {
  return "Hello, Welcome to JavaScript!";
}

console.log(greet()); 
// Output: Hello, Welcome to JavaScript!
```

### Example 2. Function with Parameter 


```ts
function greet(name) {
  return "Hello " + name + "!";
}

console.log(greet("Sara")); 
// Output: Hello Sara!
console.log(greet("Eswar")); 
// Output: Hello Eswar!

```

### Example 3. Function with Multiple Parameter 

```ts
function add(a, b) {
  return a + b;
}

console.log(add(5, 3)); // Output: 8
console.log(add(10, 20)); // Output: 30

```

### Example 4. Function without Retrun (Just printing)

```ts
function sayHi(name) {
  console.log("Hi " + name);
}

sayHi("Tom");  // Output: Hi Tom
sayHi("Lisa"); // Output: Hi Lisa

```

### Example 5. Function Expression 

- You can also store a function inside a variable.

```ts

const multiply = function(x, y) {
  return x * y;
};

console.log(multiply(4, 5)); // Output: 20

```

### Example 6. Arrow Function (ES6)

- A shorter way to write functions.

```ts
const square = (n) => n * n;

console.log(square(6)); // Output: 36

```
