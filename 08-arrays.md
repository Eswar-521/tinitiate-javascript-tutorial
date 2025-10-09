
## 08-arrays.md

### Arrays in JavaScript

* Definition:
- An array in JavaScript is a special variable that can store multiple values in a single variable.
- Instead of creating separate variables for each value, you can store them inside an array.

### How to Create an Array

```ts
let fruits = ["apple", "banana", "mango"];
```

Here:

- `fruits` → array variable name

- `["apple", "banana", "mango"]` → array values (called elements)

- Indexing starts from 0

`fruits[0]` → `"apple"`

`fruits[1]` → `"banana"`

`fruits[2]` → `"mango"`

### Example

```ts
let fruits = ["apple", "banana", "mango"];

console.log(fruits[0]); // apple
console.log(fruits[1]); // banana
console.log(fruits[2]); // mango
```


### 🔧 Array Properties & Methods

1. Length of an Array
let fruits = ["apple", "banana", "mango"];
console.log(fruits.length); // 3

2. Add an Element (push)
fruits.push("orange");
console.log(fruits); // ["apple", "banana", "mango", "orange"]

3. Remove Last Element (pop)
fruits.pop();
console.log(fruits); // ["apple", "banana", "mango"]

4. Add at the Beginning (unshift)
fruits.unshift("grape");
console.log(fruits); // ["grape", "apple", "banana", "mango"]

5. Remove First Element (shift)
fruits.shift();
console.log(fruits); // ["apple", "banana", "mango"]


### Note : 
- Arrays store multiple values in one variable.

- Elements are accessed using indexes (0-based).

### Common methods:

- push() → add at end

- pop() → remove from end

- unshift() → add at beginning

- shift() → remove from beginning

- length → count elements