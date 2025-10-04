I'll create comprehensive lesson and task files for Advanced Selectors & Pseudo-elements based on the PDF material.

# Lesson 4: Advanced Selectors & Pseudo-elements

## Learning Objectives
By the end of this lesson, you will be able to:
- Use contextual selectors to target elements based on document structure
- Apply attribute selectors to style elements by their attributes
- Work with pseudo-classes for dynamic styling
- Use structural pseudo-classes to select elements by position
- Apply pseudo-elements to style specific parts of elements
- Generate content dynamically with CSS

---

## Contextual Selectors

**Contextual selectors** allow you to target elements based on their relationship to other elements in the document hierarchy.

### Document Hierarchy

HTML documents have a tree-like structure with parent, child, and sibling relationships:

```html
<article>           <!-- parent -->
  <h2>Title</h2>    <!-- child of article, sibling of p -->
  <p>Text</p>       <!-- child of article, sibling of h2 -->
</article>
```

### Descendant Selector

Select elements nested anywhere within another element:

```css
article p {
  color: gray;
}
```

This selects all `<p>` elements inside `<article>`, no matter how deeply nested.

### Child Selector (>)

Select only direct children:

```css
article > p {
  color: blue;
}
```

This selects only `<p>` elements that are immediate children of `<article>`.

**Example:**
```html
<article>
  <p>This will be blue</p>
  <div>
    <p>This will NOT be blue (not a direct child)</p>
  </div>
</article>
```

### Adjacent Sibling Selector (+)

Select an element immediately following another:

```css
h2 + p {
  font-weight: bold;
}
```

This selects the first `<p>` that comes immediately after an `<h2>`.

### General Sibling Selector (~)

Select all siblings that follow an element:

```css
h2 ~ p {
  margin-left: 20px;
}
```

This selects all `<p>` elements that follow an `<h2>` (as siblings).

### Combining Selectors

You can combine contextual selectors for precise targeting:

```css
nav > ul > li:first-child {
  font-weight: bold;
}

article h2 + p {
  font-size: 1.2em;
}
```

---

## Attribute Selectors

**Attribute selectors** target elements based on their attributes and attribute values.

### Basic Attribute Selector

Select elements that have a specific attribute:

```css
a[href] {
  color: blue;
}

img[alt] {
  border: 2px solid green;
}
```

### Exact Value Match

Select elements with an exact attribute value:

```css
a[href="https://example.com"] {
  color: red;
}

input[type="text"] {
  border: 1px solid #ccc;
}
```

### Contains Value

Select elements whose attribute contains a specific value:

```css
/* Contains the word "button" */
a[class~="button"] {
  padding: 10px;
}

/* Contains "external" anywhere in href */
a[href*="external"] {
  color: orange;
}
```

### Starts With

Select elements whose attribute starts with a specific value:

```css
/* href starts with "https" */
a[href^="https"] {
  padding-left: 20px;
}

/* class starts with "btn" */
[class^="btn"] {
  display: inline-block;
}
```

### Ends With

Select elements whose attribute ends with a specific value:

```css
/* href ends with ".pdf" */
a[href$=".pdf"]::after {
  content: " (PDF)";
}

/* src ends with ".png" */
img[src$=".png"] {
  border: 1px solid gray;
}
```

### Common Use Cases

```css
/* Style external links */
a[href^="http"]::after {
  content: " ↗";
}

/* Style email links */
a[href^="mailto:"] {
  color: #0066cc;
}

/* Style required form fields */
input[required] {
  border-left: 3px solid red;
}
```

---

## Pseudo-Classes

**Pseudo-classes** select elements based on their state or position in the document.

### Dynamic Pseudo-Classes

These change based on user interaction:

```css
/* Unvisited link */
a:link {
  color: blue;
}

/* Visited link */
a:visited {
  color: purple;
}

/* Mouse hover */
a:hover {
  color: red;
  text-decoration: underline;
}

/* Active (being clicked) */
a:active {
  color: orange;
}

/* Keyboard focus */
input:focus {
  outline: 2px solid blue;
  background: #f0f0f0;
}
```

**Best Practice:** Define link styles in this order (LoVe HAte):
1. :link
2. :visited
3. :hover
4. :active

### Structural Pseudo-Classes

Target elements based on their position:

#### :first-child and :last-child

```css
li:first-child {
  font-weight: bold;
}

li:last-child {
  border-bottom: none;
}
```

#### :nth-child()

Select elements by position number:

```css
/* Select the 3rd child */
li:nth-child(3) {
  color: red;
}

/* Select even children (2, 4, 6...) */
li:nth-child(even) {
  background: #f0f0f0;
}

/* Select odd children (1, 3, 5...) */
li:nth-child(odd) {
  background: white;
}

/* Select every 3rd child starting from the first */
li:nth-child(3n+1) {
  font-weight: bold;
}
```

#### :first-of-type and :last-of-type

Target the first or last element of a specific type:

```css
p:first-of-type {
  font-size: 1.2em;
}

article img:last-of-type {
  margin-bottom: 0;
}
```

#### :nth-of-type()

Similar to :nth-child() but only counts elements of the same type:

```css
/* Every other paragraph */
p:nth-of-type(even) {
  background: #f9f9f9;
}
```

#### :only-child

Select elements that are the only child:

```css
p:only-child {
  text-align: center;
}
```

#### :empty

Select elements with no children:

```css
div:empty {
  display: none;
}
```

### :not() Pseudo-Class

Select elements that DON'T match a selector:

```css
/* All paragraphs except those with class "intro" */
p:not(.intro) {
  font-size: 14px;
}

/* All inputs except submit buttons */
input:not([type="submit"]) {
  border: 1px solid #ccc;
}

/* All list items except the first */
li:not(:first-child) {
  margin-top: 10px;
}
```

---

## Pseudo-Elements

**Pseudo-elements** let you style specific parts of elements or insert generated content.

**Note:** Pseudo-elements use double colons (::) while pseudo-classes use single colons (:).

### ::first-letter

Style the first letter of an element:

```css
p::first-letter {
  font-size: 2em;
  font-weight: bold;
  color: #c00;
  float: left;
  margin-right: 5px;
}
```

Creates a drop cap effect.

### ::first-line

Style the first line of text:

```css
p::first-line {
  font-weight: bold;
  color: #333;
  text-transform: uppercase;
}
```

### ::before and ::after

Insert generated content before or after an element:

```css
.note::before {
  content: "Note: ";
  font-weight: bold;
  color: blue;
}

.required::after {
  content: " *";
  color: red;
}
```

### Practical Examples with ::before and ::after

**Adding icons:**
```css
.external-link::after {
  content: " ↗";
  font-size: 0.8em;
}

.download::before {
  content: "⬇ ";
}
```

**Creating shapes:**
```css
.arrow::after {
  content: "";
  display: inline-block;
  width: 0;
  height: 0;
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: 5px solid black;
  margin-left: 5px;
}
```

**Decorative elements:**
```css
blockquote::before {
  content: open-quote;
  font-size: 3em;
  color: #ccc;
  vertical-align: -0.4em;
}

blockquote::after {
  content: close-quote;
  font-size: 3em;
  color: #ccc;
  vertical-align: -0.4em;
}
```

---

## Generating Content with CSS

The `content` property works with ::before and ::after to insert content.

### Content Values

```css
/* Text string */
.label::before {
  content: "New: ";
}

/* Attribute value */
a::after {
  content: " (" attr(href) ")";
}

/* Counter */
h2::before {
  content: counter(section) ". ";
}

/* No content (for decorative elements) */
.icon::before {
  content: "";
  display: block;
  width: 20px;
  height: 20px;
  background: url(icon.png);
}
```

### Displaying Attribute Values

Show attribute values in the rendered page:

```css
/* Show href in parentheses after links */
a::after {
  content: " (" attr(href) ")";
  font-size: 0.8em;
  color: #666;
}

/* Show alt text below images */
img::after {
  content: attr(alt);
  display: block;
  text-align: center;
  font-style: italic;
}
```

### Working with Quotation Marks

```css
/* Define custom quote marks */
blockquote {
  quotes: """ """ "'" "'";
}

blockquote::before {
  content: open-quote;
  font-size: 2em;
  color: #999;
}

blockquote::after {
  content: close-quote;
  font-size: 2em;
  color: #999;
}
```

### CSS Counters

Create automatic numbering:

```css
body {
  counter-reset: section;
}

h2::before {
  counter-increment: section;
  content: "Section " counter(section) ": ";
}
```

**Nested counters:**
```css
body {
  counter-reset: chapter;
}

h2 {
  counter-reset: section;
}

h2::before {
  counter-increment: chapter;
  content: counter(chapter) ". ";
}

h3::before {
  counter-increment: section;
  content: counter(chapter) "." counter(section) " ";
}
```

---

## Practical Combinations

### Clearfix with ::after

Clear floats without extra HTML:

```css
.clearfix::after {
  content: "";
  display: table;
  clear: both;
}
```

### Custom List Markers

```css
ul {
  list-style: none;
  padding-left: 0;
}

ul li::before {
  content: "▶ ";
  color: #2196F3;
  font-weight: bold;
  margin-right: 8px;
}
```

### Breadcrumb Navigation

```css
.breadcrumb li {
  display: inline;
}

.breadcrumb li:not(:last-child)::after {
  content: " / ";
  color: #999;
  padding: 0 8px;
}
```

### Required Form Fields

```css
label.required::after {
  content: " *";
  color: red;
}

input:required {
  border-left: 3px solid red;
}

input:valid {
  border-left: 3px solid green;
}
```

---

## Best Practices

### Selector Specificity

More specific selectors override less specific ones:

```css
/* Specificity: 1 (one element) */
p {
  color: black;
}

/* Specificity: 11 (one class + one element) */
p.intro {
  color: blue;
}

/* Specificity: 100 (one ID) */
#main {
  color: red;
}
```

### Performance Considerations

- Avoid overly complex selectors
- Right-to-left matching means browsers read selectors from right to left
- More efficient: `nav .menu-item`
- Less efficient: `body div nav ul li a`

### Maintainability

```css
/* Good: Clear and specific */
.article-header h1 {
  font-size: 2em;
}

/* Avoid: Too generic */
div div div h1 {
  font-size: 2em;
}
```

### Generated Content Guidelines

- Only use ::before and ::after for decorative content
- Never put important information in generated content (accessibility)
- Images inserted via content don't appear in print by default

---

## Browser Support

### Well-Supported

- Basic pseudo-classes (:hover, :focus, :first-child)
- ::before and ::after
- Attribute selectors
- :not()

### Good Support (IE9+)

- Structural pseudo-classes (:nth-child, :last-child)
- ::first-letter, ::first-line
- Advanced attribute selectors

### Check Before Using

Always test in target browsers or use feature detection.

---

## Summary

In this lesson, you learned:

- **Contextual selectors** target elements based on document structure (descendant, child, sibling)
- **Attribute selectors** select elements by their attributes and values
- **Pseudo-classes** select elements by state (:hover, :focus) or position (:first-child, :nth-child)
- **Pseudo-elements** style parts of elements (::first-letter) or generate content (::before, ::after)
- The `content` property creates generated content with ::before and ::after
- How to combine selectors for powerful, specific styling
- Best practices for selector efficiency and maintainability

Next lesson: Responsive Design & Media Queries!