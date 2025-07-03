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
function add(a, b) {
    return a + b;
}

let x = 5;
let y = 10;
console.log(add(x, y));

```
```python
#  Python output
def add(a, b):
    return a + b

x = 5
y = 10
print(add(x, y))
```
