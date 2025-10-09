
## 03-data-types.md

### JavaScript Data Types

- In JavaScript, `data types` define the kind of values we can store in variables.

JavaScript is `dynamically typed` → you don’t need to declare the type, it is decided automatically at runtime. 


1. String 

- Represents text inside quotes (`""` or `''` or `).

- Can contain letters, numbers, and symbols.

```ts

let str1 = "Hello";
let str2 = 'World';
let str3 = `Hello ${str2}`; // Template literal

console.log(str1);  // Hello
console.log(str2);  // World
console.log(str3);  // Hello World
```

2. Number 

- Represents both `integers` and `floating-point` numbers.

```ts

let num1 = 42;      // Integer
let num2 = 3.14;    // Decimal
let num3 = -100;    // Negative number

console.log(num1, num2, num3); // 42 3.14 -100
```

3. Boolean 

- Represents true or false values.

- Often used in conditions.

```ts

let isOk = true;
let isLoggedIn = false;

console.log(isOk);       // true
console.log(isLoggedIn); // false
```

4. Object

- Stores data in key-value pairs.

- Used for structured data.

```ts
let person = {
  name: "Tom",
  age: 30,
  isStudent: false
};

console.log(person.name); // Tom
console.log(person.age);  // 30
```

5. Array

- A collection of values stored in a single variable.

- Values can be of any type.

```ts
let items = ["apple", "orange", "banana"];
let mixed = [1, "text", true];

console.log(items[0]);  // apple
console.log(items[1]);  // orange
console.log(mixed[2]);  // true
```

6. Null

- Represents intentional empty value.

- Think of it as “nothing here.”

```ts
let data = null;
console.log(data); // null
```

7. Undefined

- A variable declared but not assigned any value.

```ts
let value;
console.log(value); // undefined
```