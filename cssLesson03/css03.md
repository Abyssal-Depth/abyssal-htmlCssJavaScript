# Lesson 3: Box Model & Layout

## Learning Objectives
By the end of this lesson, you will be able to:
- Understand the CSS box model and its components
- Control element spacing with margins and padding
- Style borders effectively
- Format lists with CSS properties
- Create visual layouts using box model principles
- Debug spacing issues using browser developer tools

---

## The CSS Box Model

Every HTML element is rendered as a rectangular box. The **CSS box model** describes the space an element occupies and how that space is calculated.

### Box Model Components

The box model consists of four areas, from inside to outside:

1. **Content** - The actual content (text, images, etc.)
2. **Padding** - Transparent space between content and border
3. **Border** - A line surrounding the padding
4. **Margin** - Transparent space outside the border

```
┌─────────────────────────────────────┐
│           MARGIN (transparent)       │
│  ┌─────────────────────────────┐    │
│  │     BORDER                   │    │
│  │  ┌─────────────────────┐    │    │
│  │  │  PADDING            │    │    │
│  │  │  ┌─────────────┐    │    │    │
│  │  │  │   CONTENT   │    │    │    │
│  │  │  └─────────────┘    │    │    │
│  │  └─────────────────────┘    │    │
│  └─────────────────────────────┘    │
└─────────────────────────────────────┘
```

### Visualizing the Box Model

```html
<div class="box">Content</div>
```

```css
.box {
  width: 200px;
  height: 100px;
  padding: 20px;
  border: 5px solid black;
  margin: 30px;
}
```

**Total width = margin-left + border-left + padding-left + width + padding-right + border-right + margin-right**

Total width = 30 + 5 + 20 + 200 + 20 + 5 + 30 = **310px**

**Total height = margin-top + border-top + padding-top + height + padding-bottom + border-bottom + margin-bottom**

Total height = 30 + 5 + 20 + 100 + 20 + 5 + 30 = **210px**

### Box-Sizing Property

The `box-sizing` property changes how width and height are calculated:

**Content-box (default):**
```css
.box {
  box-sizing: content-box;  /* default */
  width: 200px;  /* content width only */
}
```

**Border-box:**
```css
.box {
  box-sizing: border-box;
  width: 200px;  /* includes padding and border */
}
```

**Modern best practice:**
```css
* {
  box-sizing: border-box;
}
```

This makes sizing more intuitive!

---

## Padding

**Padding** creates space between an element's content and its border. Padding is transparent and takes the background color of the element.

### Padding Syntax

**Single value (all sides):**
```css
padding: 20px;
```

**Two values (vertical | horizontal):**
```css
padding: 10px 20px;
/* top/bottom: 10px, left/right: 20px */
```

**Three values (top | horizontal | bottom):**
```css
padding: 10px 20px 30px;
/* top: 10px, left/right: 20px, bottom: 30px */
```

**Four values (top | right | bottom | left - clockwise):**
```css
padding: 10px 20px 30px 40px;
```

**Mnemonic:** TRouBLe (Top, Right, Bottom, Left)

### Individual Sides

```css
padding-top: 10px;
padding-right: 20px;
padding-bottom: 30px;
padding-left: 40px;
```

### Padding Examples

```css
.button {
  padding: 12px 24px;  /* Comfortable button */
}

.card {
  padding: 20px;  /* Even spacing */
}

.header {
  padding: 30px 15px;  /* More top/bottom than sides */
}
```

### When to Use Padding

- Creating space inside elements
- Making clickable areas larger
- Preventing content from touching borders
- Creating visual breathing room

---

## Margins

**Margins** create space between elements. Margins are always transparent and do not take background colors.

### Margin Syntax

Same syntax as padding:

```css
margin: 20px;  /* all sides */
margin: 10px 20px;  /* vertical | horizontal */
margin: 10px 20px 30px;  /* top | horizontal | bottom */
margin: 10px 20px 30px 40px;  /* top | right | bottom | left */

margin-top: 10px;
margin-right: 20px;
margin-bottom: 30px;
margin-left: 40px;
```

### Auto Margins

**Centering block elements horizontally:**
```css
.container {
  width: 800px;
  margin: 0 auto;  /* Centers horizontally */
}
```

This only works for block elements with a set width!

### Negative Margins

Margins can be negative to pull elements closer:

```css
.overlap {
  margin-top: -20px;  /* Pulls element up */
}
```

Use carefully - can cause overlapping content!

### Margin Collapsing

**Vertical margins collapse** between adjacent elements:

```html
<p style="margin-bottom: 30px;">First paragraph</p>
<p style="margin-top: 20px;">Second paragraph</p>
```

Gap between paragraphs = **30px** (not 50px)

The larger margin wins.

**Margin collapsing DOES NOT occur:**
- With horizontal margins
- Between parent and child if parent has padding/border
- With flexbox or grid layouts
- With absolutely positioned elements

### When to Use Margins

- Creating space between elements
- Centering elements horizontally
- Creating layout spacing
- Separating sections of content

---

## Borders

**Borders** surround the padding area of an element.

### Border Properties

Three main properties define borders:

**1. Border Width:**
```css
border-width: 1px;
border-width: thin;    /* ~1px */
border-width: medium;  /* ~3px, default */
border-width: thick;   /* ~5px */
border-width: 2px 4px;  /* vertical | horizontal */
```

**2. Border Style:**
```css
border-style: none;     /* default - no border */
border-style: solid;    /* ──── */
border-style: dashed;   /* ---- */
border-style: dotted;   /* ···· */
border-style: double;   /* ═══ */
border-style: groove;   /* 3D grooved */
border-style: ridge;    /* 3D ridged */
border-style: inset;    /* 3D inset */
border-style: outset;   /* 3D outset */
```

**3. Border Color:**
```css
border-color: #333;
border-color: rgb(51, 51, 51);
border-color: currentColor;  /* Uses text color */
```

### Border Shorthand

```css
border: width style color;
```

**Examples:**
```css
border: 1px solid #333;
border: 2px dashed blue;
border: 3px double rgb(200, 0, 0);
```

### Individual Sides

```css
border-top: 1px solid black;
border-right: 2px dashed blue;
border-bottom: 3px dotted red;
border-left: 4px solid green;

/* Or be more specific */
border-top-width: 2px;
border-top-style: solid;
border-top-color: #333;
```

### Border Radius

Create rounded corners:

```css
border-radius: 5px;  /* All corners */
border-radius: 10px 20px;  /* top-left & bottom-right | top-right & bottom-left */
border-radius: 10px 20px 30px 40px;  /* clockwise from top-left */
```

**Individual corners:**
```css
border-top-left-radius: 10px;
border-top-right-radius: 20px;
border-bottom-right-radius: 30px;
border-bottom-left-radius: 40px;
```

**Creating shapes:**
```css
.circle {
  width: 100px;
  height: 100px;
  border-radius: 50%;
}

.pill {
  border-radius: 25px;
}

.tab {
  border-radius: 10px 10px 0 0;  /* Rounded top only */
}
```

### Border Examples

```css
.card {
  border: 1px solid #ddd;
  border-radius: 8px;
}

.error {
  border-left: 4px solid #f44336;
}

.dashed-box {
  border: 2px dashed #999;
}

.outline-button {
  border: 2px solid #2196F3;
  border-radius: 4px;
}
```

---

## Combining Box Model Properties

### Card Component Example

```css
.card {
  /* Content sizing */
  width: 300px;
  
  /* Padding for internal spacing */
  padding: 20px;
  
  /* Border for definition */
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  
  /* Margin for spacing from other elements */
  margin: 20px;
  
  /* Additional styling */
  background-color: white;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
```

### Button Example

```css
.button {
  /* Make clickable area larger */
  padding: 12px 24px;
  
  /* Visual definition */
  border: 2px solid #2196F3;
  border-radius: 4px;
  
  /* Spacing from other elements */
  margin: 5px;
  
  /* Additional styling */
  background-color: #2196F3;
  color: white;
  cursor: pointer;
}

.button:hover {
  background-color: #1976D2;
  border-color: #1976D2;
}
```

---

## List Styling

CSS provides properties specifically for styling ordered and unordered lists.

### List Style Type

Control the marker/bullet style:

**Unordered lists:**
```css
ul {
  list-style-type: disc;      /* • (default) */
  list-style-type: circle;    /* ○ */
  list-style-type: square;    /* ▪ */
  list-style-type: none;      /* No marker */
}
```

**Ordered lists:**
```css
ol {
  list-style-type: decimal;              /* 1, 2, 3 (default) */
  list-style-type: decimal-leading-zero; /* 01, 02, 03 */
  list-style-type: lower-roman;          /* i, ii, iii */
  list-style-type: upper-roman;          /* I, II, III */
  list-style-type: lower-alpha;          /* a, b, c */
  list-style-type: upper-alpha;          /* A, B, C */
  list-style-type: lower-greek;          /* α, β, γ */
}
```

### List Style Position

Control marker position:

```css
ul {
  list-style-position: outside;  /* Marker outside text block (default) */
  list-style-position: inside;   /* Marker inside text block */
}
```

**Visual difference:**

```
Outside:                 Inside:
  • Item text wraps       • Item text wraps
    like this               like this
  • Next item             • Next item
```

### List Style Image

Use custom images as markers:

```css
ul {
  list-style-image: url('bullet-icon.png');
}
```

**Better approach with pseudo-elements:**
```css
ul {
  list-style: none;
  padding-left: 0;
}

ul li::before {
  content: '→ ';
  color: #2196F3;
  font-weight: bold;
  margin-right: 8px;
}
```

### List Style Shorthand

```css
list-style: type position image;
```

**Examples:**
```css
ul {
  list-style: square inside;
}

ol {
  list-style: lower-roman outside;
}
```

### Removing Default List Styling

Common for navigation menus:

```css
nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

nav li {
  display: inline-block;  /* Horizontal list */
  margin-right: 20px;
}
```

### Nested List Styling

```css
ul {
  list-style-type: disc;
}

ul ul {
  list-style-type: circle;
}

ul ul ul {
  list-style-type: square;
}
```

### Custom List Counters

For advanced numbering:

```css
ol {
  counter-reset: my-counter;
  list-style: none;
}

ol li::before {
  counter-increment: my-counter;
  content: counter(my-counter) ". ";
  color: #2196F3;
  font-weight: bold;
}
```

---

## Practical Layout Techniques

### Centering Content

**Horizontal centering:**
```css
.container {
  max-width: 1200px;
  margin: 0 auto;  /* Centers horizontally */
  padding: 0 20px;  /* Prevents touching edges */
}
```

**Text centering:**
```css
.centered-text {
  text-align: center;
}
```

### Creating Consistent Spacing

```css
/* Vertical rhythm */
h1, h2, h3, h4, h5, h6 {
  margin-top: 0;
  margin-bottom: 0.5em;
}

p {
  margin-top: 0;
  margin-bottom: 1.5em;
}

ul, ol {
  margin-top: 0;
  margin-bottom: 1.5em;
  padding-left: 1.5em;
}
```

### Spacing Sections

```css
section {
  padding: 60px 0;  /* Vertical section spacing */
}

section + section {
  border-top: 1px solid #eee;  /* Visual separator */
}
```

### Responsive Padding

```css
.container {
  padding: 20px;
}

@media (min-width: 768px) {
  .container {
    padding: 40px;
  }
}
```

---

## Debugging the Box Model

### Using Browser DevTools

**Chrome/Firefox DevTools:**
1. Right-click element → Inspect
2. View "Computed" or "Box Model" tab
3. See visual representation of margins, borders, padding

**What to look for:**
- Unexpected margin collapsing
- Padding vs margin confusion
- Border adding to width
- Box-sizing issues

### Common Box Model Issues

**Problem: Element wider than expected**
```css
/* Problem */
.box {
  width: 300px;
  padding: 20px;
  border: 5px solid black;
  /* Total width: 350px! */
}

/* Solution */
.box {
  box-sizing: border-box;
  width: 300px;
  padding: 20px;
  border: 5px solid black;
  /* Total width: 300px ✓ */
}
```

**Problem: Margin not working**
```css
/* Margins may collapse or inline elements ignore vertical margins */
span {
  margin-top: 20px;  /* Doesn't work! */
}

/* Solution: Make it block or inline-block */
span {
  display: inline-block;
  margin-top: 20px;  /* Now it works */
}
```

**Problem: Content touching edges**
```css
/* Add padding! */
.card {
  padding: 20px;
}
```

---

## Best Practices

### Consistent Spacing

Use a spacing system:

```css
:root {
  --spacing-xs: 4px;
  --spacing-sm: 8px;
  --spacing-md: 16px;
  --spacing-lg: 24px;
  --spacing-xl: 32px;
}

.card {
  padding: var(--spacing-md);
  margin-bottom: var(--spacing-lg);
}
```

### Reset or Normalize

Start with consistent defaults:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

Or use a CSS reset/normalize library.

### Semantic Spacing

Use margins for layout spacing (between elements) and padding for internal spacing (inside elements).

```css
/* Good: Margin for layout */
section {
  margin-bottom: 40px;
}

/* Good: Padding for internal spacing */
.card {
  padding: 20px;
}

/* Avoid mixing without reason */
```

---

## Summary

In this lesson, you learned:

- The box model consists of content, padding, border, and margin
- `box-sizing: border-box` makes sizing more intuitive
- Padding creates internal spacing; margins create external spacing
- Borders can be styled with width, style, color, and radius
- Margin collapsing affects vertical margins between elements
- Lists can be styled with various marker types and positions
- The box model is fundamental to all CSS layouts
- Browser DevTools visualize the box model for debugging

Next lesson: Advanced Selectors & Pseudo-elements!