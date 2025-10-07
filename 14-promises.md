
## 14-promises.md


## Promises in JavaScript

### Definition:
- A Promise in JavaScript represents a value that may be available now, in the future, or never.
It is mainly used to handle asynchronous operations (like API calls, file reading, setTimeout, etc.).

### ✨ States of a Promise

* A promise can be in one of three states:

* Pending → Initial state (not resolved or rejected yet).

* Fulfilled → Operation completed successfully → resolve() is called.

* Rejected → Operation failed → reject() is called.


###  Example: Basic Promise

```ts
let promise = new Promise((resolve, reject) => {
  // Task is successful
  resolve("Done!");
  // If there was an error: reject("Error!");
});

// Handling the promise
promise.then((result) => console.log(result))   // Done!
       .catch((error) => console.log(error));

```


Explanation:

- new Promise((resolve, reject) => {...}) → Creates a promise.

- resolve("Done!") → Marks the promise as successful.

- reject("Error!") → Marks the promise as failed.

- .then() → Runs when the promise is resolved.

- .catch() → Runs when the promise is rejected.

### Example: Using setTimeout (Async Operation)

```ts
let promise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve("Data received after 2 seconds");
  }, 2000);
});

promise.then((result) => console.log(result));
// Output after 2 sec → Data received after 2 seconds

```


### 🔁 Promise Chaining

- You can chain multiple `.then()` calls.

```ts
let promise = new Promise((resolve) => {
  resolve(10);
});

promise
  .then((num) => num * 2)      // 20
  .then((num) => num + 5)      // 25
  .then((num) => console.log(num)); // 25

⚡ Promise Error Handling
let promise = new Promise((resolve, reject) => {
  reject("Something went wrong!");
});

promise
  .then((result) => console.log(result))
  .catch((error) => console.log("Error:", error));
// Output → Error: Something went wrong!


```

### Note 

- Promise handles asynchronous code.

- States: Pending → Fulfilled (resolve) → Rejected (reject).

Methods:

- .then() → when resolved.

- .catch() → when rejected.

- .finally() → runs always (success or failure).
- Useful for API calls, delays, and async tasks.