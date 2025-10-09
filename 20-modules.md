
## 20-modules.md


### JavaScript Modules are a way to split your code into multiple files.
- This helps in keeping the code organized, reusable, and maintainable.

- Each module is a separate file.

- We can export values (functions, objects, or variables) from one module.

- We can import those values in another module.




### Example: Exporting and Importing
👉 `math.js` (Export file)


```ts
// math.js

// Named export
export const PI = 3.14;

// Exporting a function
export function add(a, b) {
  return a + b;
}

// Exporting multiple things at once
export const subtract = (a, b) => a - b;
```




👉 `app.js` (Import file)

```ts

// Import specific values
import { PI, add, subtract } from "./math.js";

console.log("PI value:", PI); // 3.14
console.log("Add:", add(10, 5)); // 15
console.log("Subtract:", subtract(10, 5)); // 5
```


### Default Export

- Sometimes we want to export just one main value from a module.

👉 `greet.js`

```ts
export default function greet(name) {
  return `Hello, ${name}!`;
}
```
👉 `main.js`

```ts
// Default export can be imported with any name
import greet from "./greet.js";

console.log(greet("Eswar")); // Hello, Eswar!
```



### Key Points

- Named exports must be imported using the exact same name.

- Default export can be imported with any name.

- Modules work in browsers only if you add type="module" in <script>:


```ts
<script type="module" src="app.js"></script>

```