---
marp: true
theme: uncover
class: invert
paginate: true
---

# 💻 Lesson B1: Intro to Bootstrap  
### & Basic Components

**Goal:** Build beautiful, responsive websites quickly using Bootstrap — a CSS framework trusted by millions.

---

## 🎨 Why Learn Bootstrap?

Bootstrap = **Professional design toolkit**  
Instead of writing hundreds of CSS lines...

✅ Prebuilt buttons, alerts, forms  
✅ Works on all devices  
✅ Looks great out of the box  

> “Like a LEGO set for websites — you snap together polished components.”

---

## 🧱 What Is Bootstrap?

A **CSS framework** that gives you:
- Ready-made styles (buttons, alerts, navbars, etc.)
- Responsive layout grid
- Consistent, modern look

Created by **Twitter**, used by **Spotify, Walmart**, and many others.

---

## 🌐 How to Add Bootstrap

We use a **CDN** — we discuss what this is, next.  
A CDN hosts Bootstrap’s files online, so you can link to them directly.

```html
<!-- In the <head> -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">

<!-- Before </body> -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
````
---

## 🌐 What Is a CDN?

**CDN = Content Delivery Network**

Think of it like a *global library* of files.

Instead of you hosting Bootstrap on your own computer...  
you borrow it from the **nearest online server** that already has it!

---
Let's watch this video on Content Delivery Networks!
https://www.youtube.com/watch?v=Bsq5cKkS33I


---
### 🗺️ How Bootstrap Works

1️⃣ You add a hyperlink to a CDN version of Bootstrap  
2️⃣ The browser fetches it from the **closest** server  
3️⃣ It loads **faster** because it’s cached around the world ()  
4️⃣ You don’t have to download anything!

---

### ⚡ Benefits

✅ Faster load times  
✅ No setup or downloads  
✅ Works on any computer with internet  
✅ Already cached by other websites  

> 💡 Example: Google Fonts, Bootstrap, and jQuery all use CDNs.

---

## ⚙️ What’s Happening Here

1️⃣ `<link>` loads **Bootstrap CSS**
2️⃣ `<script>` loads **Bootstrap JS** (for dropdowns, modals, etc.)
3️⃣ Your browser downloads these files from the CDN
4️⃣ You can now use all Bootstrap classes!

🧠 *The script goes at the end of `<body>`.*

---
Let's watch this video on Bootstrap from Harvard's CS50: 
https://cs50.harvard.edu/web/weeks/0/
From 1:38:20 to 1:47:45


--- 

## Open associated file 
## to visually follow along with html: 
bootstrap01ExampleHmtl.html

---

## 🔵 Bootstrap Buttons

Without Bootstrap:

```html
<button>Click Me</button>
```

With Bootstrap:

```html
<button class="btn btn-primary">Click Me</button>
```
✨ Professional look instantly!

---

## 🎨 Button Colors

```html
<button class="btn btn-primary">Primary</button>
<button class="btn btn-success">Success</button>
<button class="btn btn-danger">Danger</button>
<button class="btn btn-warning">Warning</button>
<button class="btn btn-dark">Dark</button>
```

🧩 Every button = `btn` + color class
(Ex: `btn-primary`, `btn-success`, `btn-warning`)

---

## 🔠 Button Sizes & Styles

```html
<button class="btn btn-primary btn-lg">Large</button>
<button class="btn btn-primary btn-sm">Small</button>

<button class="btn btn-outline-danger">Outline</button>
```

> 🪄 Outline versions use a border only — perfect for light themes.

---

## ⚠️ Bootstrap Alerts

```html
<div class="alert alert-success">Success! Task completed.</div>
<div class="alert alert-danger">Error: Something went wrong.</div>
<div class="alert alert-warning">Warning! Check your input.</div>
```

Use for messages, warnings, or notifications.

---

## 🪪 Bootstrap Badges

Tiny labels for counts or tags.

```html
<h1>Messages <span class="badge bg-primary">4</span></h1>
<h3>User <span class="badge bg-success">Online</span></h3>
<button class="btn btn-primary">
  Cart <span class="badge bg-light text-dark">3</span>
</button>
```

---

## 📏 Spacing Utilities

No CSS needed — use quick margin (`m`) and padding (`p`) classes.

```html
<div class="mt-3">Margin Top</div>
<div class="mb-4">Margin Bottom</div>
<div class="p-3">Padding All Around</div>
```

🧮 Sizes go from `0` → `5` (small → large)

---

## ✍️ Text Utilities

Quick formatting helpers:

```html
<p class="text-center">Centered text</p>
<p class="text-success">Green text</p>
<p class="fw-bold">Bold text</p>
<p class="text-uppercase">Uppercase</p>
```

---

## Yes, you can combine classes: 

```html
<p class="text-center text-success fw-bold text-uppercase">
  Centered, Green, Bold, and Uppercase Text
</p>
```

---


## ⚖️ Bootstrap vs. Custom CSS

| Use Bootstrap When...   | Use Custom CSS When...     |
| ----------------------- | -------------------------- |
| You want speed          | You need unique design     |
| You want responsiveness | You need precise control   |
| You want consistency    | You want smaller file size |

💡 Best Practice: **Use both!**
Link Bootstrap first, then your own CSS after it.

---

## 🧩 Summary

✅ Bootstrap = CSS framework for quick, responsive design
✅ Add via **CDN** links in HTML
✅ Use classes like `btn`, `alert`, `badge`
✅ Utility classes for spacing & text
✅ Combine Bootstrap + your CSS for best results

---

🧠 Key Terms

| **Term** | **Meaning** |
|-----------|-------------|
| **Framework**| Pre-written toolkit for structure and styling (e.g. Bootstrap).|
| **CDN**| Network of servers that host files globally for faster loading. |
| **Component**| Reusable UI piece (e.g. alert, navbar). |
| **Utility Class**| One-purpose style helper (e.g. `text-center`, `mt-3`). |
| **Bootstrap Class**| Predefined multi-style class for full elements (e.g. `btn`, `alert`). |
