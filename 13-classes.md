
## 13-classes.md


### Classes in JavaScript

### Definition:
- A class in JavaScript is a blueprint for creating objects.
It lets you define properties (data) and methods (functions) that objects created from the class can use.


### Example: Basic Class

```ts
class Car {
  constructor(name) {
    this.name = name; // property
  }

  // method
  drive() {
    console.log(this.name + " is driving");
  }
}

// Create an object (instance) from the class
let myCar = new Car("Toyota");
myCar.drive(); // Toyota is driving

```


Explanation:

- class Car { ... } → Defines a class named Car.

- constructor(name) → Special method that runs when a new object is created.

- this.name = name; → Assigns the passed value to the object’s property.

drive() → A method of the class.

- new Car("Toyota") → Creates a new object (called an instance) of the class.

### 🔑 Key Features of Classes
1. Constructor Method

```ts
Used to initialize object properties.

class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}

let p1 = new Person("Alice", 22);
console.log(p1.name); // Alice
console.log(p1.age);  // 22


```
2. Methods in Classes

```ts
Functions inside classes.

class Animal {
  constructor(type) {
    this.type = type;
  }
  speak() {
    console.log(this.type + " makes a sound");
  }
}

let dog = new Animal("Dog");
dog.speak(); // Dog makes a sound
```



3. Inheritance (Extending Classes)

- One class can inherit properties and methods from another using extends.
```ts
class Vehicle {
  start() {
    console.log("Vehicle started");
  }
}

class Car extends Vehicle {
  drive() {
    console.log("Car is driving");
  }
}

let myCar = new Car();
myCar.start(); // Vehicle started (inherited)
myCar.drive(); // Car is driving
```



4. Super Keyword

- Used to call the parent class’s constructor or methods.
```ts
class Vehicle {
  constructor(brand) {
    this.brand = brand;
  }
}

class Bike extends Vehicle {
  constructor(brand, model) {
    super(brand); // call parent constructor
    this.model = model;
  }
  showDetails() {
    console.log(this.brand + " " + this.model);
  }
}

let bike1 = new Bike("Honda", "Shine");
bike1.showDetails(); // Honda Shine
```

### Note :

- Class → Blueprint for objects.

- Constructor → Initializes object properties.

- Methods → Functions inside classes.

- Inheritance → One class can extend another (extends).

- Super → Used to call parent class constructor/methods.
