# JavaScript Async Programming 

## Contents
- [Event Loop](#event-loop)
- [Call Stack](#call-stack)
- [Task Queue and Microtasks](#task-queue-and-microtasks)

---

## Event Loop

JavaScript is **single-threaded**, which means it can execute one task at a time. The **event loop** allows JavaScript to perform **non-blocking asynchronous operations** like I/O without freezing the program.

**How it works:**  
- Checks the **call stack** to see if it's empty.  
- If empty, takes the first task from the **task queue** and pushes it to the stack.  
- Repeats this process continuously.

### Example:

```javascript
console.log("Start");

setTimeout(() => {
  console.log("Timeout");
}, 0);

console.log("End");
```
Output:
- Start
- End
- Timeout

- Even with setTimeout(…, 0), the callback runs after the synchronous code because it goes to the task queue.


## Call Stack

The call stack is a LIFO (Last In, First Out) data structure that keeps track of function calls.

Example:

```js 
function first() {
  console.log("First");
  second();
}

function second() {
  console.log("Second");
}

first();
```
Output:
- First
- Second


Explanation:

- first() is pushed to the stack.

- Inside first(), second() is called and pushed on top.

- second() completes, popped off.

- first() completes, popped off.


## Task Queue and Microtasks
- Task Queue (Macrotasks)

- Tasks like setTimeout, setInterval, and I/O callbacks go here.

- Event loop picks the first task from the task queue when the call stack is empty.

- Microtasks

- Tasks like Promises (.then) and MutationObserver.

- Microtasks have higher priority than macrotasks: they are executed before moving to the next macrotask.

Example:

```js
console.log("Start");

setTimeout(() => {
  console.log("Timeout"); // Macrotask
}, 0);

Promise.resolve().then(() => {
  console.log("Promise"); // Microtask
});

console.log("End");

Output:
- Start
- End
- Promise
- Timeout

```


Explanation:

- Promise callback runs before setTimeout because microtasks are processed immediately after the current stack clears, before the next macrotask.

## Summary:

- Call Stack: Executes code (synchronous).

- Task Queue (Macrotask Queue): Holds asynchronous tasks.

- Microtasks Queue: Holds higher-priority async tasks (Promises, MutationObservers).

- Event Loop: Continuously checks the stack and queues, ensuring non-blocking execution.


