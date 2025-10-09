# Prototypes and Classes  


## Contents
- [Prototype Chain](#prototype-chain)
- [Object.create()](#objectcreate)
- [Class vs Prototype](#class-vs-prototype)



## Prototype Chain

In JavaScript, every object has an internal link to another object called its **prototype**. This is called the **prototype chain**. It allows objects to inherit properties and methods from other objects.

### Example:

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}

Person.prototype.greet = function() {
  console.log(`Hello, my name is ${this.name}`);
};

const person1 = new Person("Eswar", 25);
person1.greet(); // Hello, my name is Eswar

// Checking the prototype chain
console.log(person1.__proto__ === Person.prototype); // true
console.log(Person.prototype.__proto__ === Object.prototype); // true
console.log(Object.prototype.__proto__); // null
```

Explanation:

- person1 inherits from Person.prototype.

- Person.prototype inherits from Object.prototype.

- Object.prototype is the end of the chain (null).


## Object.create()

- Object.create() creates a new object with the specified prototype.

Example:

```js
const animal = {
  eats: true
};

const rabbit = Object.create(animal);
rabbit.jumps = true;

console.log(rabbit.eats); // true (inherited from animal)
console.log(rabbit.jumps); // true
console.log(Object.getPrototypeOf(rabbit) === animal); // true

```

Explanation:

- rabbit inherits from animal.

- You can create objects without using constructors or classes.

##  Class vs Prototype

JavaScript classes are syntactic sugar over the existing prototype-based inheritance. Classes make it easier to write and read code, but under the hood, JavaScript still uses prototypes.

Example:

```js
// Using Class
class PersonClass {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hi, my name is ${this.name}`);
  }
}

const eswar = new PersonClass("Eswar", 25);
eswar.greet(); // Hi, my name is Eswar

// Equivalent using prototype
function PersonProto(name, age) {
  this.name = name;
  this.age = age;
}

PersonProto.prototype.greet = function() {
  console.log(`Hi, my name is ${this.name}`);
};

const eswar2 = new PersonProto("Eswar", 25);
eswar2.greet(); // Hi, my name is Eswar
```


Key Points:

- Feature	Class	Prototype Function
- Syntax	Cleaner & modern	Function constructor
- Inheritance	extends keyword	Manual prototype chaining
- Methods	Inside class block	Added to prototype
- Usage	Preferred in ES6+	Older or more flexible approach


## Summary

- The prototype chain enables inheritance.

- Object.create() is a simple way to set prototypes.

- Classes are syntactic sugar over prototypes but make the code cleaner and more structured.