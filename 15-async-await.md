
## 15-async-await.md

### Async/Await in JavaScript

### Definition:

- async and await are special keywords in JavaScript used to work with Promises in a cleaner and easier way.

- They make asynchronous code look like synchronous (normal step-by-step) code.

1. The async Keyword

- Declares a function as asynchronous.

- An async function always returns a Promise.

```ts
async function fetchData() {
  return "Data received"; // Automatically wrapped in a Promise
}

fetchData().then(console.log); // Data received
```

2. The await Keyword

- Can only be used inside an async function.

- It pauses the function until the Promise resolves.


```ts
function getData() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("Fetched after 2 sec"), 2000);
  });
}

async function fetchData() {
  console.log("Fetching...");
  let result = await getData(); // Wait until the promise resolves
  console.log(result);
}

fetchData();
// Output:
// Fetching...
// (after 2 sec) Fetched after 2 sec
```


3. Handling Errors with try...catch

```ts
function getData(isError) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (isError) reject("Something went wrong!");
      else resolve("Success!");
    }, 1000);
  });
}

async function fetchData() {
  try {
    let result = await getData(false); // change to true to test error
    console.log(result);
  } catch (error) {
    console.log("Error:", error);
  }
}

fetchData();
// Output → Success!
```


### Note 

- async → makes a function return a Promise.

- await → pauses inside an async function until the promise resolves.

- Easier to read & write compared to chaining .then() and .catch().

- Use try...catch for error handling with async/await.