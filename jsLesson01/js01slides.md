---
marp: true
theme: uncover
class: invert
paginate: true
---

# Lesson 01: 
# Introduction to JavaScript

---

## What is JavaScript?

* JavaScript is a programming language that makes web pages interactive and dynamic

* While **`HTML`** provides structure and **`CSS`** provides style, **`JavaScript`** provides behavior and interactivity

---

### What Can JavaScript Do?

- Respond to user actions (clicks, typing, hovering)  
- Change HTML content dynamically  
- Modify CSS styles on the fly  
- Validate form inputs  
- Create animations and effects  
- Load data without refreshing the page  

---

### JavaScript Runs in the Browser

* Unlike some programming languages that need 
special software...  

* `JavaScript` runs directly in your web browser.  
Every modern browser has a `JavaScript` engine built in.

---

## Adding JavaScript to Your HTML

* There are **three ways** to include JavaScript in your web pages:
### Inline, Internal, External

---

### Method 1: Inline JavaScript

```html
<button onclick="alert('Hello!')">Click Me</button>
````

* `onclick` is an **HTML event attribute**
* `alert` is the **JavaScript function**



---

### Method 2: Internal JavaScript 
Using the Script Tag `<script>`

```html
<!DOCTYPE html>
<html>
<head>
  <title>My First JavaScript</title>
</head>
<body>
  <h1>Hello World</h1>

  <script>
    // JavaScript code goes here
    alert('Welcome to JavaScript!');
  </script>

</body>
</html>
```

**Notes:**

* Place `<script>` near the end of `<body>`
* HTML loads before JavaScript runs
* Use `//` for single-line comments

---

### Method 3: External JavaScript File 
(Best Practice)

**index.html** points to **script.js**

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Page</title>
</head>
<body>
  <h1>Hello World</h1>
  <script src="script.js"></script>
</body>
</html>
```

```javascript
alert('Hello from external file!');
```

✅ External files = organized, reusable, maintainable, faster to load.

---

## Your First JavaScript Program

```html
<!DOCTYPE html>
<html>
<head>
  <title>JavaScript Test</title>
</head>
<body>
  <h1>My First JavaScript</h1>

  <script>
    // This is a comment
    alert('Hello, World!');              // Popup
    console.log('This appears in console'); // Debugging
    document.write('JavaScript is working!'); // On page
  </script>
</body>
</html>
```

---

### Three Ways to Output Information

1. **`alert()`** – Popup box (blocks page)
2. **`console.log()`** – Writes to browser console 
3. **`document.write()`** – Writes to page (only for testing)

---

### Browser Console: Your Best Friend

### How to Open It

* **Windows/Linux:** `F12` or `Ctrl + Shift + I`
* **Mac:** `Cmd + Option + I`
* Click the **Console** tab

---

### What You Can Do in the Console

* See `console.log()` messages
* See errors when code breaks
* Debug your programs
<br>
**We will get into this more in a later lessons but for now we'll at least take a look and try a few things**

---

## Comments in JavaScript

```javascript
// Single-line comment

/*
Multi-line comment
spans multiple lines
*/

// Example:
let age = 25;  // Store the user's age
```

**Why use comments?**

Explain code  |  Leave notes for others
Disable code temporarily  |  Document functions

---

## Summary

✅ JavaScript makes web pages interactive
✅ Three ways to add JS (inline, internal, external)
✅ Outputs we looked at: `alert()`, `console.log()`, `document.write()`
✅ Comments explain and document code

---


## Key Terms

* **JavaScript** – Programming language for interactivity
* **Console** – Browser tool for messages & errors
* **Comment** – Notes in code, ignored by JS
* **alert()** – Popup message
* **console.log()** – Console output function

```
