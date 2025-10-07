
## 04-operators.md

## Operators in Javascript are symbols that perform operations on values or variables.


1. Arithmetic Operators

- Used for mathematical calculations.

```ts
let x = 5;
let y = 3;

console.log(x + y); // 8  (Addition)
console.log(x - y); // 2  (Subtraction)
console.log(x * y); // 15 (Multiplication)
console.log(x / y); // 1.666... (Division)
console.log(x % y); // 2  (Modulus: remainder)
```


2. Assignment Operators

- Used to assign values to variables.

```ts
let a = 10;
a += 5; // a = a + 5
console.log(a); // 15

a -= 3; // a = a - 3
console.log(a); // 12

a *= 2; // a = a * 2
console.log(a); // 24

a /= 4; // a = a / 4
console.log(a); // 6
```

3. Comparison Operators

- Used to compare values and return true or false.

```ts
let x = 5;
let y = "5";

console.log(x == y);  // true  (equality, only checks value)
console.log(x === y); // false (strict equality, checks value + type)
console.log(x != y);  // false (not equal by value)
console.log(x !== y); // true  (strict not equal)
console.log(x > 3);   // true
console.log(x < 3);   // false
console.log(x >= 5);  // true
console.log(x <= 4);  // false

```

4. Logical Operators

- Used to combine conditions.

```ts
let a = true;
let b = false;

console.log(a && b); // false (AND → both must be true)
console.log(a || b); // true  (OR → at least one true)
console.log(!a);     // false (NOT → opposite)
```


5. String Operators

- `+` can also join strings (concatenation).

```ts
let first = "Hello";
let last = "World";

console.log(first + " " + last); // Hello World

```


6. `➕` Addition (+)

- Used to add two numbers or join strings.

```ts
let x = 5;
let y = 3;

console.log(x + y); // 8 (number addition)

let firstName = "Alice";
let lastName = " Smith";
console.log(firstName + lastName); // "Alice Smith" (string concatenation)
```


7. `➖` Subtraction (-)

- Subtracts the right-hand operand from the left-hand operand.


```ts
let x = 10;
let y = 4;

console.log(x - y); // 6
```

8. `✖️` Multiplication (*)

- Multiplies two numbers.

```ts
let x = 6;
let y = 2;

console.log(x * y); // 12
```


9. `➗` Division (/)

- Divides the left-hand operand by the right-hand operand.

```ts
let x = 15;
let y = 3;

console.log(x / y); // 5
```

9. `🔢` Modulus (%)

- Returns the remainder after division.

```ts
let x = 10;
let y = 3;

console.log(x % y); // 1 (because 10 ÷ 3 = 3 remainder 1)
```
10. `⚖️` Equality (==)

- Compares values after type conversion.
```ts
console.log(5 == "5");  // true (values are equal after conversion)
console.log(5 == 5);    // true
console.log(5 == 6);    // false
```


11. `🔒` Strict Equality (===)

- Compares both value and type (no type conversion).

```ts
console.log(5 === "5"); // false (number vs string)
console.log(5 === 5);   // true (same type and value)
```
