
## 10-events.md

## Events in JavaScript

### Definition:

- Events in JavaScript are actions or occurrences that happen in the browser, often triggered by the user or the browser itself.

👉 Examples:

- A user clicks a button

- A user presses a key

- A web page loads completely

- A mouse moves over an element

* JavaScript can react to these events using event handlers.

### Example : Button Click Event

```ts

<!DOCTYPE html>
<html>
<head>
  <title>Event Example</title>
</head>
<body>

<button onclick="myFunction()">Click Me</button>

<script>
  function myFunction() {
    alert("Button clicked!");
  }
</script>

</body>
</html>
```

### Explanation : 

- `<button onclick="myFunction()">` → The event is onclick (triggered when button is clicked).

- `myFunction()` → The function that runs when the event occurs.

- `alert("Button clicked!")` → Action that happens when button is clicked.


### Here the Common Javascript Events 

### Event Name	   ==>    Triggered When…
- onclick	User   ==>    clicks an element
- onmouseover	   ==>    Mouse hovers over an element
- onmouseout	   ==>    Mouse leaves an element
- onkeydown	     ==>    A key is pressed down
- onkeyup	       ==>    A key is released
- onchange	     ==>    Value of input/select changes
- onload	       ==>    Page finishes loading
- onsubmit	     ==>    A form is submitted