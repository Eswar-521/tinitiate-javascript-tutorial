
## 07-loops.md

### Loops in JavaScript

- Definition: Loops in JavaScript are used to execute a block of code repeatedly as long as a specified condition is true.

1. `for` Loop 

- The `for` loop is used when you know how many times you want to run the loop.

```ts
Syntax:

for (initialization; condition; increment/decrement) {
  // code to be executed
}


Example:

for (let i = 0; i < 5; i++) {
  console.log("Number is:", i);
}
```

- Explanation:

- let i = 0 → Start value (i is initialized to 0).

- i < 5 → Condition (loop runs while i is less than 5).

- i++ → Increment (adds 1 after each loop).

- Runs 5 times → outputs 0, 1, 2, 3, 4.

2. `while Loop`

- The while loop is used when you don’t know in advance how many times to run the loop — it keeps running as long as the condition is true.


```ts
Syntax:

while (condition) {
  // code to be executed
}


Example:

let i = 0;
while (i < 5) {
  console.log("Number is:", i);
  i++;
}

```

- Explanation:

- Loop starts with i = 0.

- Runs while i < 5.

- Increases i each time.

- Prints 0, 1, 2, 3, 4.



3. `do...while Loop`

- The do...while loop is similar to while, but it always runs at least once (because the condition is checked after running the block).


```ts
Syntax:

do {
  // code to be executed
} while (condition);


Example:

let i = 0;
do {
  console.log("Number is:", i);
  i++;
} while (i < 5);

```

- Explanation:

- Executes the block first.

- Then checks i < 5.

- Runs until condition becomes false.

- Prints 0, 1, 2, 3, 4.


