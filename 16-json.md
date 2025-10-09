
## 16-json.md

### SON in JavaScript

### Definition:

- JSON stands for JavaScript Object Notation.

- It is a lightweight data format used to store and exchange data between systems (for example: client ↔ server).

- JSON looks like JavaScript objects but is stored as strings.

### ✨ Example: JSON String

```ts
let jsonString = '{"name":"Sara","age":25}';
```

- This is a JSON string (notice the quotes around keys and values).

- Keys and string values must be inside double quotes (" ").



1. Converting JSON String → JavaScript Object

We use ` JSON.parse()`

```ts
let jsonString = '{"name":"Sara","age":25}';
let obj = JSON.parse(jsonString);

console.log(obj.name); // Sara
console.log(obj.age);  // 25
```

Explanation:

- JSON.parse(jsonString) → Converts JSON string into a JavaScript object.

- Now we can access values using obj.name or obj.age.

2. Converting JavaScript Object → JSON String

- We use `JSON.stringify()`

```ts
let person = {
  name: "John",
  age: 30,
  isStudent: false
};

let jsonString = JSON.stringify(person);
console.log(jsonString);
// {"name":"John","age":30,"isStudent":false}
```


Explanation:

- JSON.stringify(person) → Converts object into a JSON string (useful for sending data to servers).



3. Example: JSON with Arrays

```ts
let jsonString = '{"students":["Alice","Bob","Charlie"]}';
let obj = JSON.parse(jsonString);

console.log(obj.students[0]); // Alice
console.log(obj.students[1]); // Bob


```

 ### Note :


- JSON = JavaScript Object Notation (text-based format for data exchange).

- `JSON.parse()` → Converts JSON string → Object.

- `JSON.stringify()` → Converts Object → JSON string.

- Commonly used in APIs to send and receive data.