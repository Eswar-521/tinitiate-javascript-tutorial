
## 11-dom-manipulation.md

## DOM Manipulation in JavaScript

## Definition
- The DOM (Document Object Model) represents the structure of a web page.
JavaScript can manipulate (change, add, remove, or style) HTML elements dynamically using the DOM.

- Example: Change Text Dynamically

```ts
<!DOCTYPE html>
<html>
<head>
  <title>DOM Manipulation Example</title>
</head>
<body>

<p id="demo">Hello</p>
<button onclick="changeText()">Change</button>

<script>
  function changeText() {
    // Find the element with id="demo" and change its content
    document.getElementById("demo").innerHTML = "Goodbye";
  }
</script>

</body>
</html>

```

### Explanation:

- document.getElementById("demo") → Finds the element with id="demo".

- .innerHTML = "Goodbye"; → Changes the text inside that element.

### 🔑 Common DOM Manipulation Methods

1. Change Content
```ts
document.getElementById("demo").innerHTML = "New Content";
```

2. Change Style

```ts
document.getElementById("demo").style.color = "red";
document.getElementById("demo").style.fontSize = "24px";
```


3. Change Attributes
```ts
document.getElementById("myImage").src = "newImage.jpg";
```


4. Create & Add Elements
```ts
let newPara = document.createElement("p");   // create element
newPara.innerHTML = "I am a new paragraph";  // set text
document.body.appendChild(newPara);          // add to page
```


5. Remove Elements

```ts
let element = document.getElementById("demo");
element.remove(); // removes the element from page
```


### Full Example: Multiple DOM Manipulations

```ts
<!DOCTYPE html>
<html>
<head>
  <title>DOM Demo</title>
</head>
<body>

<p id="demo">Original Text</p>
<img id="myImage" src="old.jpg" width="100">
<button onclick="manipulate()">Manipulate DOM</button>

<script>
  function manipulate() {
    // Change text
    document.getElementById("demo").innerHTML = "Text Changed!";

    // Change style
    document.getElementById("demo").style.color = "blue";

    // Change attribute
    document.getElementById("myImage").src = "new.jpg";

    // Add new element
    let newElement = document.createElement("h2");
    newElement.innerHTML = "I was added dynamically!";
    document.body.appendChild(newElement);
  }
</script>

</body>
</html>
```

### Note : 

- DOM allows JavaScript to interact with HTML elements.

- Common manipulations:

- Change content → `.innerHTML`

- Change style → `.style`

- Change attributes → `.setAttribute()` or `direct assignment`

- Add/Remove elements → `createElement()`, `appendChild()`, `remove()`


