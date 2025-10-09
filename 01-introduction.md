
## 01-introduction.md

## JavaScript Introduction


- JavaScript is a programming language that runs inside the browser and makes websites interactive.
Without JavaScript, a webpage is just plain HTML + CSS (static).
With JavaScript, we can add logic, handle events, and update content dynamically.


### Why Use Javascript..?

- Validate forms (check if user entered correct data before submitting).

- Handle user interactions (clicks, typing, mouse movement, etc.).

- Build dynamic websites (change text, images, or styles without reloading).

- Communicate with servers (fetch API data, load content).

- Create games, animations, and single-page apps.



## Example : 

```ts
<!DOCTYPE html>
<html>
<head>
  <title>JavaScript Example</title>
</head>
<body>
  <h2>JavaScript Demo</h2>

  <!-- A button that shows a message when clicked -->
  <button onclick="alert('Hello!')">Click me</button>
</body>
</html>
```

- When you click the button, an `alert popup` appears with the message `"Hello!"`.



## Example : Chnaging Text 

```ts

<!DOCTYPE html>
<html>
<body>
  <h2 id="demo">Old Text</h2>

  <button onclick="changeText()">Click to Change</button>

  <script>
    function changeText() {
      document.getElementById("demo").innerHTML = "New Text!";
    }
  </script>
</body>
</html>
```

- Here:

- document.getElementById("demo") → finds the <h2> element.

- innerHTML = "New Text!" → replaces its content when button is clicked.



## Example : From Validation 


```ts
<!DOCTYPE html>
<html>
<body>
  <form onsubmit="return validateForm()">
    Name: <input type="text" id="name">
    <input type="submit" value="Submit">
  </form>

  <script>
    function validateForm() {
      let x = document.getElementById("name").value;
      if (x === "") {
        alert("Name must be filled out");
        return false; // Prevent form submission
      }
      return true;
    }
  </script>
</body>
</html>
```

- If the user tries to submit without entering a name → an alert shows up.

- return false stops the form from submitting.







