
## 12-es6-features.md


### ES6 Features in JavaScript

### Definition:
- ES6 (ECMAScript 2015) introduced many new features that make JavaScript code more powerful, readable, and easier to write.

1. let and const

- `let` → Used for block-scoped variables (can be updated, but not re-declared in the same scope).

- `const` → Used for block-scoped constants (cannot be reassigned).


```ts 
let name = "Alice";
name = "Bob";   // ✅ allowed
console.log(name); // Bob

const age = 25;
// age = 30; ❌ Error: Cannot reassign
console.log(age);
```


2. Arrow Functions

- Shorter syntax for writing functions.

- Automatically bind this from their surrounding scope.


```ts
// Normal function
function addOld(a, b) {
  return a + b;
}

// Arrow function
const add = (a, b) => a + b;

console.log(add(2, 3)); // 5

```

3. Template Literals

- Use backticks (`) instead of quotes.

- Allow string interpolation using ${}.

- Support multi-line strings easily.

```ts
let name = "Alice";
let age = 25;

// Normal string concatenation
console.log("My name is " + name + " and I am " + age + " years old.");

// Template literal
console.log(`My name is ${name} and I am ${age} years old.`);

// Multi-line string
let message = `Hello,
This is a multi-line
string.`;
console.log(message);

```


4.  Spread & Rest Operator (...)

- Spread `(...)` → Expands elements (useful for arrays/objects).

- Rest `(...)` → Collects arguments into an array.

```ts
// Spread Example
let arr1 = [1, 2, 3];
let arr2 = [4, 5];
let combined = [...arr1, ...arr2];
console.log(combined); // [1, 2, 3, 4, 5]

// Rest Example
function sum(...numbers) {
  return numbers.reduce((total, num) => total + num, 0);
}
console.log(sum(1, 2, 3, 4)); // 10
```

### Note : 
- let & const → Block-scoped variables.

- Arrow functions → Shorter function syntax.

- Template literals → String interpolation & multi-line strings.

- Spread/Rest operator → Expands or collects values.