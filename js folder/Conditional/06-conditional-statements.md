
## 06-conditional-statements.md


## JavaScript Conditional Statements

- Conditional statements are used to make decisions in your code. They allow your program to execute different blocks of code based on certain conditions.

1. `if` Statement

- Executes a block of code only if the condition is true.

```ts
let age = 20;

if (age >= 18) {
  console.log("You are an adult."); 
}


Output:

You are an adult.

```

2. `if...else` Statement

- Executes one block if the condition is true, and another block if it’s false.


```ts
let age = 15;

if (age >= 18) {
  console.log("You are an adult.");
} else {
  console.log("You are a minor.");
}


Output:

You are a minor.
```


3. `if...else if...else` Statement

- Used when you have multiple conditions.


```ts
let marks = 85;

if (marks >= 90) {
  console.log("Grade: A");
} else if (marks >= 75) {
  console.log("Grade: B");
} else if (marks >= 50) {
  console.log("Grade: C");
} else {
  console.log("Grade: F");
}


Output:

Grade: B
```


4. `switch Statement`

- A cleaner way to handle multiple possible values of a variable.


```ts
let day = 3;

switch (day) {
  case 1:
    console.log("Monday");
    break;
  case 2:
    console.log("Tuesday");
    break;
  case 3:
    console.log("Wednesday");
    break;
  default:
    console.log("Invalid day");
}


Output:

Wednesday

```



### ES6 Tip: Ternary Operator (? :)

- A short way to write simple if...else conditions.

```ts
let age = 18;
let result = (age >= 18) ? "Adult" : "Minor";
console.log(result);


Output:

Adult

```

