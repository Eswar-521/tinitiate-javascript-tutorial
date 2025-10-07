
## 17-error-handling.md


### Error Handling in JavaScript

- In JavaScript, error handling is done using the try...catch block.
- It allows you to catch errors and handle them gracefully without crashing the program.

Syntax 

```ts
try {
  // Code that might throw an error
} catch (error) {
  // Handle the error here
}
```

- try block → Contains code that may throw an error.

- catch block → Handles the error if one occurs.

- finally block (optional) → Always runs, whether an error occurs or not.

### Example: Basic Error Handling

```ts
try {
  throw new Error("Something went wrong!"); // Manually throwing an error
} catch (err) {
  console.log("Error caught: " + err.message);
} finally {
  console.log("This will always run, error or not.");
}
```


### Output
- Error caught: Something went wrong!
- This will always run, error or not.

### Example: Handling Undefined Variable Error

```ts
try {
  console.log(user); // 'user' is not defined → ReferenceError
} catch (error) {
  console.log("An error occurred: " + error.message);
}
```

### Output
- An error occurred: user is not defined

### Example: Preventing Program Crash

```ts
function divide(a, b) {
  try {
    if (b === 0) {
      throw new Error("Cannot divide by zero");
    }
    return a / b;
  } catch (err) {
    console.log("Error: " + err.message);
  }
}

console.log(divide(10, 2)); // 5
console.log(divide(10, 0)); // Error: Cannot divide by zero

```

### 👉 Note:

- Use try for risky code.

- Use catch to handle errors.

- Use finally for cleanup (always runs).


