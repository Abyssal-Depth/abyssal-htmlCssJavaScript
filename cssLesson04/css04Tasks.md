# Task 4: Advanced Selectors & Pseudo-elements

## Objective
Master advanced CSS selectors including contextual selectors, attribute selectors, pseudo-classes, and pseudo-elements to create sophisticated styling without extra HTML markup.

## Setup
Create:
- `advanced.html`
- `advanced.css`

**Total Points: 100**

---

## Part A: Blog Post with Contextual Selectors (25 points)

1. Create `advanced.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Advanced Selectors Practice</title>
  <link rel="stylesheet" href="advanced.css">
</head>
<body>
  <article class="blog-post">
    <header>
      <h1>Understanding CSS Selectors</h1>
      <p class="meta">Published on <time>October 4, 2025</time> by Jane Doe</p>
    </header>
    
    <p>CSS selectors are the foundation of styling web pages. In this article, we'll explore advanced techniques.</p>
    
    <h2>Getting Started</h2>
    <p>First, let's understand the basics. Selectors allow you to target specific elements.</p>
    <p>There are many types of selectors available in modern CSS.</p>
    
    <h2>Advanced Techniques</h2>
    <p>Now we'll dive into more complex selection methods.</p>
    <p>These techniques will help you write cleaner, more maintainable code.</p>
    
    <blockquote>
      <p>CSS is not just about making things pretty; it's about creating maintainable, semantic designs.</p>
    </blockquote>
    
    <h2>Conclusion</h2>
    <p>With these techniques, you can style complex layouts efficiently.</p>
  </article>
</body>
</html>
```

2. In `advanced.css`, use contextual selectors:

**Requirements:**
- First paragraph after the header should be larger (1.2em) and bold
- All paragraphs immediately following h2 headings should be indented 20px
- Blockquote paragraphs should be italic with gray color (#666)
- The meta paragraph should be smaller (0.9em) and gray (#888)
- All h2 elements except the first should have 40px top margin

**Grading:**
- First paragraph styling (5 points)
- Paragraphs after h2 headings (5 points)
- Blockquote styling (5 points)
- Meta paragraph styling (5 points)
- All h2 except first (5 points)

---

## Part B: Attribute Selectors for Links (20 points)

3. Add this navigation and links section to your HTML (inside body, before article):

```html
<nav class="main-nav">
  <ul>
    <li><a href="#home">Home</a></li>
    <li><a href="https://example.com">External Site</a></li>
    <li><a href="mailto:contact@example.com">Email Us</a></li>
    <li><a href="docs/guide.pdf">Download Guide</a></li>
    <li><a href="https://github.com/username">GitHub</a></li>
  </ul>
</nav>
```

4. Style links using attribute selectors:

**Requirements:**
- All links starting with "https" should have a small arrow icon after them (use "↗" character)
- Links to PDF files should have "(PDF)" after them in smaller, gray text
- Email links should have a different color (#0066cc) and mail icon before them (use "✉ ")
- Internal links (href starting with #) should be bold
- External links should underline on hover only

**Grading:**
- HTTPS links with arrow (5 points)
- PDF links indicator (5 points)
- Email link styling (5 points)
- Internal link styling (3 points)
- Hover effects (2 points)

---

## Part C: Dynamic Pseudo-Classes (15 points)

5. Add a contact form to your HTML (after the article):

```html
<section class="contact-form">
  <h2>Contact Us</h2>
  <form>
    <div class="form-group">
      <label for="name">Name</label>
      <input type="text" id="name" required>
    </div>
    
    <div class="form-group">
      <label for="email">Email</label>
      <input type="email" id="email" required>
    </div>
    
    <div class="form-group">
      <label for="message">Message</label>
      <textarea id="message" rows="5" required></textarea>
    </div>
    
    <button type="submit">Send Message</button>
  </form>
</section>
```

6. Style using dynamic pseudo-classes:

**Requirements:**
- Focused inputs should have a blue border (2px solid #2196F3) and light blue background (#f0f8ff)
- Button should change background color on hover (#1976D2) with smooth transition (0.3s)
- Button should have a pressed effect on :active (scale down slightly or darker color)
- Visited links should be purple (#800080)
- Unvisited links should be blue (#0000FF)

**Grading:**
- Input focus styles (5 points)
- Button hover effect with transition (5 points)
- Button active state (3 points)
- Link visited/unvisited states (2 points)

---

## Part D: Structural Pseudo-Classes (20 points)

7. Add a features section to your HTML:

```html
<section class="features">
  <h2>Key Features</h2>
  <div class="feature-grid">
    <div class="feature">
      <h3>Fast Performance</h3>
      <p>Optimized for speed and efficiency.</p>
    </div>
    <div class="feature">
      <h3>Responsive Design</h3>
      <p>Works on all devices and screen sizes.</p>
    </div>
    <div class="feature">
      <h3>Easy to Use</h3>
      <p>Intuitive interface for all users.</p>
    </div>
    <div class="feature">
      <h3>Secure</h3>
      <p>Built with security in mind.</p>
    </div>
    <div class="feature">
      <h3>Customizable</h3>
      <p>Tailor it to your needs.</p>
    </div>
    <div class="feature">
      <h3>Great Support</h3>
      <p>We're here to help you succeed.</p>
    </div>
  </div>
</section>
```

8. Style using structural pseudo-classes:

**Requirements:**
- First feature should have a gold/yellow background (#fff9c4)
- Last feature should have a blue background (#e3f2fd)
- Odd-numbered features should have a light gray background (#f5f5f5)
- Even-numbered features should have white background
- Every third feature should have a thicker border (3px instead of 1px)
- All features should have border and padding (your choice)

**Grading:**
- First feature styling (4 points)
- Last feature styling (4 points)
- Odd/even alternating backgrounds (6 points)
- Every third feature styling (4 points)
- Base feature styling (2 points)

---

## Part E: Pseudo-Elements and Generated Content (20 points)

9. Apply pseudo-elements throughout your page:

**Requirements for blog post:**
- First letter of the first paragraph in .blog-post should be a drop cap (3em, bold, different color, floated left)
- First line of blockquote should be uppercase and bold
- Add quotation marks before and after blockquote using ::before and ::after (use open-quote and close-quote)

**Requirements for features:**
- Add a checkmark (✓) before each feature h3 using ::before
- Add a decorative line after the "Key Features" h2 using ::after (hint: use a colored border or background)

**Requirements for required fields:**
- Add a red asterisk (*) after labels for required fields using attribute selector and ::after

**Grading:**
- Drop cap on first letter (5 points)
- First line styling (3 points)
- Quotation marks (4 points)
- Feature checkmarks (4 points)
- Decorative line (2 points)
- Required field asterisks (2 points)

---

## Bonus Challenges (20 extra points)

### Bonus 1: Custom Numbered Headings (10 points)
Use CSS counters to automatically number all h2 headings in the blog post (e.g., "1. Getting Started", "2. Advanced Techniques", etc.)

```css
/* Your solution here using counter-reset and counter-increment */
```

### Bonus 2: Advanced :not() Selector Usage (10 points)
Create these styles using the :not() pseudo-class:
- Style all paragraphs EXCEPT those inside blockquote or with class "meta"
- Style all links EXCEPT those in navigation
- Style all feature divs EXCEPT the first and last

Demonstrate at least 3 different uses of :not()

---

## Part F: Polish and Refinement (Additional styling to make page look good)

Add these finishing touches (included in base points):

**Global Styles:**
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.6;
  color: #333;
  max-width: 900px;
  margin: 0 auto;
  padding: 20px;
}

/* Add more as needed */
```

---

## Submission Checklist

- [ ] Contextual selectors used correctly for blog post
- [ ] Attribute selectors target different link types
- [ ] Dynamic pseudo-classes applied to form elements
- [ ] Structural pseudo-classes create alternating patterns
- [ ] Pseudo-elements add visual enhancements
- [ ] Generated content appears correctly
- [ ] First letter drop cap works
- [ ] Quotation marks appear on blockquote
- [ ] Required field indicators show
- [ ] All hover effects work smoothly
- [ ] Code is well-organized and commented
- [ ] Page displays correctly in browser
- [ ] No inline styles used (all CSS in external file)

**Submit your folder with both HTML and CSS files plus screenshots!**

---

## Expected Output Examples

Your page should demonstrate:
- Clear visual hierarchy with contextual styling
- Different link styles based on attributes
- Interactive form with focus states
- Alternating feature card colors
- Decorative elements from pseudo-elements
- Professional, polished appearance

**Key Learning Outcomes:**
- Understanding selector specificity
- Using relationships between elements
- Creating dynamic, interactive styles
- Adding visual elements without extra HTML
- Writing maintainable, semantic CSS