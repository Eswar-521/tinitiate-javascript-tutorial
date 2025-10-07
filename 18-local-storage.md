
## 18-local-storage.md

### Local Storage in JavaScript
### 📌 What is Local Storage?

- Local Storage is a web storage API in JavaScript that allows you to store key-value pairs in the browser.

- Data stored in local storage does not expire — it remains even after closing the browser or restarting the computer (until manually cleared).

- Stored data is always in string format, so objects/arrays must be converted using JSON.stringify() and JSON.parse().


```ts
📌 Basic Example
// Store data
localStorage.setItem("username", "John");

// Retrieve data
let user = localStorage.getItem("username");
console.log(user); // John

// Remove data
localStorage.removeItem("username");

// Clear all data
localStorage.clear();

```



### 📌 Storing Objects in Local Storage

- Since Local Storage only stores strings, you need to convert objects/arrays using JSON.

```ts
// Object to store
let user = { name: "Sara", age: 25 };

// Convert object to string before saving
localStorage.setItem("user", JSON.stringify(user));

// Retrieve the object
let storedUser = JSON.parse(localStorage.getItem("user"));
console.log(storedUser.name); // Sara
console.log(storedUser.age);  // 25
```


### 📌 When to Use Local Storage?

- Save user preferences (theme, language, etc.)
- Store small amounts of data for offline access
-  Remember form input between refreshes

❌ Not suitable for sensitive data (like passwords) because it’s accessible from developer tools.

### ⚡ Note:
- Local Storage = Browser’s permane