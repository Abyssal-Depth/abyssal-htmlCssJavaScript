# Task 1: CSS Basics & Selectors

## Objective
Practice applying CSS using different methods and master various selector types including element, class, ID, contextual, and attribute selectors.

## Setup
Create the following files in a new folder:
- `index.html`
- `styles.css`

**Total Points: 100**

---

## Part A: Creating Your First Stylesheet (20 points)

### Instructions

1. Create an HTML file named `index.html` with the following structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My CSS Practice Page</title>
  <!-- Link your external stylesheet here -->
</head>
<body>
  <header>
    <h1>Welcome to My Website</h1>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
  
  <main>
    <article id="intro">
      <h2>Introduction</h2>
      <p class="highlight">This is an important paragraph that should stand out from the rest.</p>
      <p>This is a regular paragraph with some text to demonstrate normal styling.</p>
      <p>Another paragraph here with additional content to show consistency.</p>
    </article>
    
    <article id="content">
      <h2>Main Content</h2>
      <p>Some content goes here with interesting information about the topic.</p>
      <p class="highlight">Another highlighted paragraph that needs emphasis.</p>
      <p>More regular paragraph content for variety.</p>
    </article>
  </main>
  
  <footer>
    <p>&copy; 2025 My Website. All rights reserved.</p>
  </footer>
</body>
</html>
```

2. Create a file named `styles.css` and link it properly in your HTML `<head>` section.

3. In `styles.css`, write CSS rules to:
   - Set the `body` background color to `#f5f5f5` (light gray)
   - Set the `body` text color to `#333` (dark gray)
   - Set the `body` font family to `Arial, Helvetica, sans-serif`
   - Make all `h1` elements use the color `#2c3e50` (dark blue)
   - Make all `h2` elements use the color `#34495e` (slightly lighter blue)
   - Add a bottom margin of `20px` to all `h1` and `h2` elements

**Grading Criteria:**
- External CSS file is properly linked (5 points)
- All specified styles are correctly applied (10 points)
- CSS is properly formatted with correct syntax (5 points)

---

## Part B: Class and ID Selectors (15 points)

### Instructions

4. Add CSS rules to:
   - Give the element with id `intro` a background color of `#fffacd` (light yellow)
   - Give the `intro` element padding of `20px` on all sides
   - Give all elements with class `highlight` a font weight of `bold`
   - Give all elements with class `highlight` an orange text color (`#ff6347`)
   - Give the `footer` element a dark gray background (`#2c3e50`)
   - Give the `footer` element white text color
   - Give the `footer` element padding of `15px` on all sides
   - Center-align the text in the `footer`

**Grading Criteria:**
- ID selector used correctly (5 points)
- Class selectors used correctly (5 points)
- All visual requirements met (5 points)

---

## Part C: Contextual Selectors (25 points)

### Instructions

5. Write CSS rules using contextual selectors (you must use descendant, child, or sibling selectors):

   a. **Navigation styling** (10 points):
   - Remove bullets from list items in the navigation (use `nav ul`)
   - Remove default padding from the `ul` inside `nav`
   - Make list items in the navigation display `inline-block`
   - Add `15px` of right margin to each navigation list item
   - Add `10px` of padding to all links inside the navigation
   - Give navigation links a background color of `#3498db` (blue)
   - Make navigation link text white
   - Remove underlines from navigation links
   
   b. **Article styling** (10 points):
   - Make paragraphs inside articles have a line-height of `1.6`
   - Add a bottom margin of `15px` to paragraphs inside articles
   - Make the first paragraph in each article have a font size of `1.1em`
   - Add `30px` of padding to all articles
   - Give articles a white background color
   - Add a bottom margin of `20px` to articles
   
   c. **Heading relationships** (5 points):
   - Make any paragraph that immediately follows an `h2` have italic font style
   - Add extra top margin (`25px`) to `h2` elements that are not the first child

**Grading Criteria:**
- Proper use of descendant selectors (8 points)
- Proper use of adjacent sibling selector (5 points)
- All visual requirements correctly implemented (12 points)

---

## Part D: Attribute Selectors (20 points)

### Instructions

6. Add a new section to your HTML (inside `<main>`, after the articles):

```html
<section id="links">
  <h2>Useful Links</h2>
  <ul>
    <li><a href="https://www.google.com">Google Search</a></li>
    <li><a href="https://developer.mozilla.org">MDN Web Docs</a></li>
    <li><a href="http://www.example.com">Example Site (HTTP)</a></li>
    <li><a href="resources/document.pdf">Download PDF Guide</a></li>
    <li><a href="resources/spreadsheet.xlsx">Download Excel File</a></li>
    <li><a href="mailto:info@example.com">Email Us</a></li>
    <li><a href="tel:+1234567890">Call Us</a></li>
  </ul>
</section>
```

7. Write CSS rules using attribute selectors:
   - Make all links that start with `https://` appear in blue (`#0066cc`)
   - Make all links that start with `http://` (not https) appear in orange (`#ff6600`) and add the text "⚠️" after them using `::after`
   - Make links ending with `.pdf` appear in red (`#cc0000`) and add " (PDF)" after them
   - Make links ending with `.xlsx` appear in green (`#00cc00`) and add " (Excel)" after them
   - Make `mailto:` links appear in purple (`#9900cc`)
   - Make `tel:` links appear in teal (`#008080`)
   - Remove underlines from all links in this section
   - Add a hover effect that underlines links when you hover over them

**Grading Criteria:**
- Correct use of `^=` (starts with) selector (5 points)
- Correct use of `$=` (ends with) selector (5 points)
- Proper use of `::after` pseudo-element (5 points)
- All styles correctly applied (5 points)

---

## Part E: Specificity Challenge (20 points)

### Instructions

8. Add this div to your HTML (inside `<main>`, after the links section):

```html
<section id="specificity-test">
  <h2>Understanding Specificity</h2>
  <div id="special" class="box">
    <p class="text" style="color: green;">Test your understanding of specificity!</p>
    <p class="text">This paragraph should be affected by your CSS.</p>
  </div>
</section>
```

9. Write THREE different CSS rules that try to set the color of paragraphs with class `text`:

```css
/* Rule 1: Using just the class */
.text {
  color: blue;
}

/* Rule 2: Using descendant selector with class */
.box .text {
  color: red;
}

/* Rule 3: Using ID in the selector */
#special .text {
  color: purple;
}
```

10. Answer these questions in CSS comments right after your rules:
   - Which rule will win for the FIRST paragraph? Why?
   - Which rule will win for the SECOND paragraph? Why?
   - Calculate the specificity score for each rule
   - How could you make Rule 1 win without using `!important`?

**Grading Criteria:**
- All three rules written correctly (6 points)
- Correct explanation of which rules win (8 points)
- Correct specificity calculations (4 points)
- Correct suggestion for making Rule 1 win (2 points)

---

## Bonus Challenges (20 extra points)

### Bonus 1: Advanced Navigation (10 points)

Enhance your navigation with these features:
- Add a hover effect that changes background color to a darker blue
- Add a smooth transition effect (0.3s) to all color changes
- Make the currently active page's link have a different background color
- Add rounded corners to navigation links (5px border-radius)

### Bonus 2: Visual Enhancement (10 points)

Improve the overall design:
- Add a subtle box shadow to articles
- Create a "container" class that limits max-width to 1200px and centers content
- Add a gradient background to the header
- Style the links section as cards with borders and padding

---

## Submission Checklist

Before submitting, verify:

- [ ] HTML file has proper structure and all required elements
- [ ] CSS file is externally linked and loads correctly
- [ ] All element selectors work correctly
- [ ] All class selectors work correctly
- [ ] All ID selectors work correctly  
- [ ] Contextual selectors (descendant, child, sibling) are used properly
- [ ] Attribute selectors are implemented correctly
- [ ] Specificity challenge is completed with explanations
- [ ] Code is properly indented and formatted
- [ ] CSS file includes helpful comments explaining sections
- [ ] Page displays correctly in a web browser
- [ ] All colors match the specifications exactly

---

## Testing Your Work

1. Open `index.html` in a web browser
2. Verify all styles are applied correctly
3. Test hover effects on links
4. Use browser developer tools (F12) to inspect elements
5. Check that your specificity challenge produces the expected results

---

## Common Mistakes to Avoid

- Forgetting to link the CSS file
- Typos in class or ID names (remember: case-sensitive!)
- Missing semicolons at the end of CSS declarations
- Forgetting closing braces `}` in CSS rules
- Using spaces in class or ID names
- Mixing up `#` (ID) and `.` (class) in selectors

---

## Helpful Resources

- MDN CSS Selectors Reference
- CSS Specificity Calculator
- Can I Use (for browser compatibility)

---

## Submission Format

Submit a folder containing:
1. `index.html` - Your HTML file
2. `styles.css` - Your CSS file
3. Screenshots of your final page showing:
   - The full page
   - The navigation with hover effect
   - The links section
   - Browser dev tools showing your CSS


**Good luck! Remember, CSS is about practice. Experiment and have fun with it!**