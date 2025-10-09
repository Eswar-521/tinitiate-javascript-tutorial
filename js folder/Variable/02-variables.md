

## 02-variables.md

### JavaScript Variables

- A variable is a container used to store data in memory so we can use it later.


### Way to Declare Variables 

1. `var` (Old, avoid using)

- Introduced in old JavaScript.

- Function-scoped (not block-scoped).

- Can be redeclared and updated.

- May cause bugs → not recommended.


2. let (Modern, Preferred)

- Block-scoped (only available inside {} block).

- Can be updated, but not redeclared in the same scope.

- Best for variables that change values.


3. const (Constant)

- Block-scoped.

- Cannot be reassigned after initialization.

- Must be initialized when declared.

- Use for fixed values (e.g., PI, API keys).


### Example :

```ts

// let → block-scoped, can change
let name = "Alice";
name = "Bob"; 
console.log(name); // Bob

// const → block-scoped, cannot change
const age = 30;
// age = 31; ❌ Error: Assignment to constant variable
console.log(age); // 30

// var → old way (avoid)
var city = "Delhi";
city = "Mumbai"; 
console.log(city); // Mumbai
```

### Block Scope Example 


```ts

{
  let x = 10;
  const y = 20;
  var z = 30;
}

// console.log(x); // ❌ Error (block-scoped)
// console.log(y); // ❌ Error (block-scoped)
console.log(z);   // ✅ 30 (var is function-scoped, not block-scoped)
```


