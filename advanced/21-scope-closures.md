# JavaScript Scope and Closures

---

## 🔹 What is Scope?

**Scope** in JavaScript determines where variables and functions are accessible within your code.

### Types of Scope
 **Global Scope**  
   - Variables declared outside any function or block.  
   - Accessible anywhere in the program.  
   ```javascript
   let globalVar = "I am global";

```js
   function showGlobal() {
     console.log(globalVar); // Accessible
   }
   showGlobal();
```

##  Function Scope

- Variables declared inside a function using var, let, or const.

- Accessible only inside that function.


```js
function testScope() {
  let localVar = "Inside function";
  console.log(localVar); // Works
}
testScope();
// console.log(localVar); // ❌ Error: localVar is not defined


Block Scope

Variables declared with let or const inside {} (if, loop, function)

Accessible only within that block.

if (true) {
  let blockVar = "Block Scope";
  console.log(blockVar); // Works
}
// console.log(blockVar); // ❌ Not accessible outside
```


## Lexical Scope

- Inner functions can access variables defined in their outer functions.

```js
function outer() {
  let outerVar = "Outer variable";
  function inner() {
    console.log(outerVar); // Accesses variable from outer scope
  }
  inner();
}
outer();
```

## 🔹 What is a Closure?

- A Closure is created when a function "remembers" variables from its lexical scope, even after the outer function has finished executing.

✅ Definition:
- A closure gives access to an outer function’s scope from an inner function, even after the outer function has returned.

Example 1: Basic Closure

```js
function outerFunction() {
  let count = 0;
  
  function innerFunction() {
    count++;
    console.log("Count:", count);
  }

  return innerFunction;
}

const counter = outerFunction(); // outerFunction executed
counter(); // Count: 1
counter(); // Count: 2
counter(); // Count: 3
```

Explanation:

- outerFunction() executes and returns innerFunction.

- The variable count remains in memory because innerFunction forms a closure over it.

- Each time counter() is called, it accesses and modifies the preserved count.

Example 2: Closure with Parameters


```js
function multiplier(x) {
  return function(y) {
    return x * y;
  };
}

const double = multiplier(2);
const triple = multiplier(3);

console.log(double(5)); // 10
console.log(triple(5)); // 15
```

🧩 Here:

- The multiplier() creates a closure that remembers the value of x.

- Even after multiplier() finishes, the inner function keeps access to x.


## 🔹 Common Uses of Closures
- Use Case	Description	Example
- Data Privacy	Keep variables private	Counter Example
- Function Factories	Create pre-configured functions	multiplier() Example
- Event Handlers	Maintain state between event triggers	Click counters
- Asynchronous Programming	Retain state in async callbacks	setTimeout() closures


Example 3: Data Privacy with Closures

```js
function createBankAccount() {
  let balance = 1000; // private variable

  return {
    deposit(amount) {
      balance += amount;
      console.log(`Deposited ₹${amount}. New balance: ₹${balance}`);
    },
    withdraw(amount) {
      if (amount <= balance) {
        balance -= amount;
        console.log(`Withdrew ₹${amount}. Remaining balance: ₹${balance}`);
      } else {
        console.log("Insufficient balance!");
      }
    }
  };
}

const account = createBankAccount();
account.deposit(500);
account.withdraw(200);
// console.log(balance); // ❌ Error: balance is private
```


🧠 Here balance is encapsulated inside createBankAccount() and cannot be accessed directly — only via the closure methods.

## 🔹 Important Points

- Closures are created every time a function is created.

- Variables used inside inner functions are not garbage-collected if referenced by closures.

- Overusing closures can lead to memory leaks if not handled properly.


## 🔹 Advantages of Closures

✅ Data encapsulation (privacy)
✅ Maintain state between function calls
✅ Functional programming patterns

## 🔹 Disadvantages of Closures

- ⚠️ May increase memory usage
- ⚠️ Can cause unexpected behaviors if not understood properly


## 🔹 Real-World Example — setTimeout()

```js
function delayedPrinter() {
  for (let i = 1; i <= 3; i++) {
    setTimeout(() => {
      console.log("Value:", i);
    }, i * 1000);
  }
}

delayedPrinter();
```

🕒 Output:

- Value: 1
- Value: 2
- Value: 3


- Because let creates a block scope, each iteration maintains its own i via closure.


## 📘 Conclusion

- Closures and scope are core concepts in JavaScript.
- Understanding them allows developers to write efficient, modular, and secure code.
- Closures enable data privacy, state management, and advanced functional programming.