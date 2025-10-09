
## 19-fetch-api.md

### JavaScript Fetch API

- The Fetch API in JavaScript is used to make HTTP requests (like GET, POST, PUT, DELETE) to servers.
It returns a Promise, which makes it easier to work with asynchronous operations (instead of old XMLHttpRequest).

✅ Basic Syntax

```ts
fetch(url, options)
  .then(response => response.json()) // convert response to JSON
  .then(data => console.log(data))   // handle the data
  .catch(error => console.error("Error:", error));
```

- `url` → The endpoint you want to request.

- ``options` → (Optional) HTTP method, headers, body, etc.

- Returns a Promise → resolves to a Response object.

### Example 1: GET Request (Fetching Data)

```ts
// Fetch all posts from an API
fetch("https://jsonplaceholder.typicode.com/posts")
  .then(response => response.json()) // Convert response to JSON
  .then(data => {
    console.log("Fetched Posts:", data);
  })
  .catch(error => console.error("Error fetching posts:", error));

```

Explanation:

- `fetch()` calls the API.

- `.then (response => response.json())` converts raw response into JSON.

- `.then(data => {...}) ` gives the actual data.

`.catch(error)` handles errors (like network issues).

### Example 2: POST Request (Sending Data)

```ts
// Send new post data to API
fetch("https://jsonplaceholder.typicode.com/posts", {
  method: "POST",  // HTTP Method
  headers: {
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    title: "My New Post",
    body: "This is the content of the post.",
    userId: 1
  })
})
  .then(response => response.json())
  .then(data => {
    console.log("Post Created:", data);
  })
  .catch(error => console.error("Error creating post:", error));

```

 Explanation:

- `method: "POST"` tells fetch we are sending data.

- `headers` specify we are sending JSON.

- `body: JSON.stringify({...})` sends data in JSON format.

### Example 3: Using async/await (Cleaner Syntax)

```ts
async function fetchUsers() {
  try {
    let response = await fetch("https://jsonplaceholder.typicode.com/users");
    let users = await response.json();
    console.log("Fetched Users:", users);
  } catch (error) {
    console.error("Error fetching users:", error);
  }
}

fetchUsers();

```


 Explanation:


- `await fetch(...)` waits for API response.

- `await response.json()` converts it to JSON.

- Easier to read than `.then()` chaining.



###  When to Use Fetch API?

- Retrieve data from REST APIs.

- Send data to servers (e.g., forms, JSON).

- Communicate with backend in web apps.

- Build features like search, live updates, etc.

- ❌ Not suitable for very old browsers (use Axios or polyfills for IE support).