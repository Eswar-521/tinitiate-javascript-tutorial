
## 09-objects.md


## Objects in JavaScript

### Definition:
- An object in JavaScript is a collection of key–value pairs.

- Keys are called properties (or attributes).

- Values can be any data type (string, number, array, function, another object, etc.).

### How to Create an Object

```ts
let user = {
  name: "Bob",
  age: 40,
};

```
Here:

- `user` → object name

- `name` and `age` → keys (properties)

- `"Bob"` and `40` → values



### Accessing Object Properties

- You can access object values in two ways:

1. Dot Notation

```ts
console.log(user.name); // Bob
console.log(user.age);  // 40
```

2. Bracket Notation

```ts
console.log(user["name"]); // Bob
console.log(user["age"]);  // 40
```


### 🔧 Adding & Modifying Properties

```ts
user.email = "bob@example.com";  // add new property
user.age = 41;                   // update existing property

console.log(user);
// { name: "Bob", age: 41, email: "bob@example.com" }
```



### 🗑️ Deleting a Property

```ts
delete user.email;
console.log(user);
// { name: "Bob", age: 41 }

```

### Objects Can Store Different Types


```ts
let student = {
  name: "Alice",
  age: 22,
  isGraduated: false,          // boolean
  subjects: ["Math", "CS"],    // array
  address: {                   // nested object
    city: "Hyderabad",
    pin: 500001
  },
  greet: function() {          // function inside object
    return "Hello, " + this.name;
  }
};

console.log(student.name);         // Alice
console.log(student.subjects[1]);  // CS
console.log(student.address.city); // Hyderabad
console.log(student.greet());      // Hello, Alice

```

### Note : 

- Objects store data as key–value pairs.

- Access properties using dot notation (`obj.key`) or bracket notation (`obj["key"]`).

- Objects can hold any type of data, including arrays, other objects, and functions.

- Properties can be added, updated, or deleted at any time.