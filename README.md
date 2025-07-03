# TransPyler

🐍✨ **TransPyler** is a Pure Python, powerful and customizable JavaScript-to-Python transpiler.

It converts modern JavaScript (including arrow functions, template strings, object methods, `map().join()` chains, and more) into clean, idiomatic Python code — preserving structure, logic, and intent.

---

## ✨ Features


✅ **Supports modern ES6+ features**  
 • Arrow functions  
 • Object methods & spread/rest  
 • Destructuring (object & array)  

✅ **Object-oriented mapping**  
 • Converts JavaScript objects into `DotDict`-style Python classes  
 • Preserves `this`

✅ **Smart method transformations**  
 • `.map().join()` → list comprehensions  
 • `.includes()` → `in`  

✅ **IIFE support**  
 • Detects and hoists immediately-invoked function expressions (IIFE)  

✅ **Helper-aware**  
 • Optionally injects helpers for `typeof`, `.length`, or `.hasOwnProperty`

✅ **Handler-based transformation system**  
 • Easily extend with your own rules  
 • Add handlers for custom JS APIs or library patterns



---

## 🚀 Quick Example(s)

```js
// JavaScript input
const PI = 3.14159;

function areaCircle(radius) {
    if (radius <= 0) {
        return 0;
    } else if (radius > 10) {
        return PI * radius * radius * 0.9; // rduction pour gros cercles
    } else {
        return PI * radius * radius;
    }
}

function checkNumber(num) {
    if (num === 0) {
        return "zero";
    } else if (num > 0) {
        return "positive";
    } else {
        return "negative";
    }
}

let x = 5;
let y = 10;

let result;

if (x > y) {
    result = areaCircle(x);
} else if (x === y) {
    result = areaCircle(y);
} else {
    result = areaCircle(x + y);
}

console.log("Result is:", result);
console.log("Check x:", checkNumber(x));
console.log("Check y:", checkNumber(y));

```
```python
#  Python output
PI = 3.14159

def areaCircle(radius):
    if radius <= 0:
        return 0
    elif radius > 10:
        return PI * radius * radius * 0.9
    else:
        return PI * radius * radius

def checkNumber(num):
    if num == 0:
        return 'zero'
    elif num > 0:
        return 'positive'
    else:
        return 'negative'

x = 5
y = 10

result = None

if x > y:
    result = areaCircle(x)
elif x == y:
    result = areaCircle(y)
else:
    result = areaCircle(x + y)

print('Result is:', result)
print('Check x:', checkNumber(x))
print('Check y:', checkNumber(y))
```
