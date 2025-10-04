# Task 2: Colors & Typography

## Objective
Master color formats (RGB, hex, HSL, RGBA, HSLA) and create professional, readable typography using font properties, web fonts, and text styling techniques.

## Setup
Create a new folder with these files:
- `typography.html`
- `typography.css`

**Total Points: 100**

---

## Part A: Color Exploration (25 points)

### Instructions

1. Create `typography.html` with this structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Color & Typography Showcase</title>
  <link rel="stylesheet" href="typography.css">
</head>
<body>
  <header class="hero">
    <h1>Color & Typography Showcase</h1>
    <p class="subtitle">Mastering CSS Colors and Fonts</p>
  </header>
  
  <section class="color-demo">
    <h2>Color Format Examples</h2>
    <div class="color-grid">
      <div class="color-box box-rgb">
        <h3>RGB Color</h3>
        <p>rgb(41, 128, 185)</p>
      </div>
      <div class="color-box box-hex">
        <h3>Hexadecimal</h3>
        <p>#E74C3C</p>
      </div>
      <div class="color-box box-hsl">
        <h3>HSL Color</h3>
        <p>hsl(142, 71%, 45%)</p>
      </div>
      <div class="color-box box-rgba">
        <h3>RGBA (Transparent)</h3>
        <p>rgba(155, 89, 182, 0.5)</p>
      </div>
    </div>
  </section>
  
  <section class="content">
    <article>
      <h2>Understanding Typography</h2>
      <p class="intro">Typography is the art and technique of arranging type to make written language legible, readable, and visually appealing when displayed.</p>
      <p>Good typography enhances the reading experience and helps establish visual hierarchy on a webpage. It's one of the most important aspects of web design.</p>
      <p>Through careful selection of typefaces, sizes, spacing, and colors, designers can create interfaces that are both beautiful and functional.</p>
    </article>
  </section>
</body>
</html>
```

2. In `typography.css`, create styles for the color boxes with these requirements:

**For `.color-box` (all boxes):**
- Width: `200px`
- Height: `200px`
- Padding: `20px`
- Margin: `10px`
- Border-radius: `8px`
- Center the text inside
- Add a subtle box shadow: `0 2px 8px rgba(0, 0, 0, 0.1)`

**For `.box-rgb`:**
- Background: Use RGB format to create a medium blue (`rgb(41, 128, 185)`)
- Text color: White

**For `.box-hex`:**
- Background: Use hexadecimal to create a coral/red color (`#E74C3C`)
- Text color: White

**For `.box-hsl`:**
- Background: Use HSL to create a green (`hsl(142, 71%, 45%)`)
- Text color: White

**For `.box-rgba`:**
- Background: Use RGBA to create a semi-transparent purple (`rgba(155, 89, 182, 0.6)`)
- Text color: Dark gray (`#333`)

**For `.color-grid`:**
- Display the boxes in a row (use `display: flex`)
- Wrap them if they don't fit (`flex-wrap: wrap`)
- Center them (`justify-content: center`)

**Grading Criteria:**
- All four color formats used correctly (12 points)
- Boxes are properly sized and styled (8 points)
- Grid layout works correctly (5 points)

---

## Part B: Web Font Integration (20 points)

### Instructions

3. Visit [Google Fonts](https://fonts.google.com) and select TWO fonts:
   - One for headings (serif or display font)
   - One for body text (sans-serif for readability)

   Suggested combinations:
   - Playfair Display + Lato
   - Merriweather + Open Sans
   - Montserrat + Roboto

4. Add the Google Fonts to your CSS using `@import` at the very top of your file:

```css
@import url('https://fonts.googleapis.com/css2?family=YourHeadingFont:wght@400;700&family=YourBodyFont:wght@300;400;600&display=swap');
```

5. Apply the fonts:
   - Body font to the `body` element
   - Heading font to all headings (`h1, h2, h3, h4, h5, h6`)

**Grading Criteria:**
- Correct `@import` syntax (5 points)
- Fonts are properly applied (10 points)
- Font choices are readable and complementary (5 points)

---

## Part C: Typography System (25 points)

### Instructions

6. Create a complete typography system with these specifications:

**Base typography:**
```css
body {
  font-family: [your chosen sans-serif], sans-serif;
  font-size: 16px;
  line-height: 1.6;
  color: #333;
}
```

**Headings:**
```css
h1, h2, h3, h4, h5, h6 {
  font-family: [your chosen heading font], serif;
  line-height: 1.2;
  margin-top: 0;
}

h1 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

h2 {
  font-size: 2rem;
  margin-bottom: 0.875rem;
}

h3 {
  font-size: 1.5rem;
  margin-bottom: 0.75rem;
}
```

**Paragraphs:**
```css
p {
  margin-bottom: 1.25rem;
}

.intro {
  font-size: 1.125rem;  /* Slightly larger */
  font-style: italic;
  color: #555;
  margin-bottom: 1.5rem;
}
```

**Grading Criteria:**
- Base typography is properly set (8 points)
- Heading sizes use rem units (7 points)
- Line heights are appropriate for readability (5 points)
- Intro paragraph has distinct styling (5 points)

---

## Part D: Advanced Text Styling (20 points)

### Instructions

7. Style the hero section:

```css
.hero {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  min-height: 300px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 40px 20px;
  text-align: center;
  color: white;
}

.hero h1 {
  font-size: 3rem;
  text-transform: uppercase;
  letter-spacing: 3px;
  margin-bottom: 0.5rem;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}

.subtitle {
  font-size: 1.5rem;
  font-weight: 300;
  letter-spacing: 1px;
  opacity: 0.9;
}
```

8. Add these text effects to your stylesheet:

**Letter spacing:**
- Add `letter-spacing: 2px` to the `.subtitle`

**Word spacing:**
- Add `word-spacing: 0.1em` to regular paragraphs

**Text transform:**
- Make all `h2` elements uppercase

**Text decoration:**
- Remove underlines from any links you might add
- Add underlines on hover

**Grading Criteria:**
- Hero section is properly styled (8 points)
- Text transform, spacing, and decoration are applied (8 points)
- Visual hierarchy is clear (4 points)

---

## Part E: Color Accessibility (10 points)

### Instructions

9. Add a new section to test contrast:

```html
<section class="accessibility-test">
  <h2>Color Contrast Examples</h2>
  <div class="good-contrast">
    <p>This text has good contrast and is easy to read (WCAG AA compliant).</p>
  </div>
  <div class="poor-contrast">
    <p>This text has poor contrast and is hard to read (Not WCAG compliant).</p>
  </div>
  <div class="excellent-contrast">
    <p>This text has excellent contrast and is very easy to read (WCAG AAA compliant).</p>
  </div>
</section>
```

10. Style these contrast examples:

```css
.good-contrast {
  background-color: #f0f0f0;
  color: #333333;
  padding: 20px;
  margin: 10px 0;
  border-left: 4px solid #4CAF50;
}

.poor-contrast {
  background-color: #cccccc;
  color: #aaaaaa;
  padding: 20px;
  margin: 10px 0;
  border-left: 4px solid #f44336;
}

.excellent-contrast {
  background-color: #ffffff;
  color: #000000;
  padding: 20px;
  margin: 10px 0;
  border-left: 4px solid #2196F3;
}
```

11. In a CSS comment, answer these questions:
   - Which example meets WCAG AA standards (4.5:1 contrast)?
   - Why is good contrast important for web accessibility?
   - What tools can you use to check contrast ratios?

**Grading Criteria:**
- Contrast examples are styled correctly (5 points)
- Questions answered correctly in comments (5 points)

---

## Bonus Challenges (20 extra points)

### Bonus 1: Custom Quote Styling (10 points)

Add a blockquote to your HTML and style it beautifully:

```html
<blockquote class="fancy-quote">
  <p>"Good typography is invisible; great typography is unforgettable."</p>
  <cite>— Typography Wisdom</cite>
</blockquote>
```

Style it with:
- Large quotation marks using `::before` and `::after`
- Italic text
- Larger font size for first letter
- Border on the left side
- Distinctive cite styling

### Bonus 2: Responsive Font Sizing (10 points)

Implement responsive typography using `clamp()`:

```css
h1 {
  font-size: clamp(2rem, 5vw, 4rem);
}

p {
  font-size: clamp(1rem, 2vw, 1.25rem);
}
```

Test by resizing your browser window.

---

## Submission Checklist

Before submitting, verify:

- [ ] All four color formats (RGB, hex, HSL, RGBA) are used correctly
- [ ] Two Google Fonts are imported and applied
- [ ] Typography system has consistent sizing using rem units
- [ ] Line heights are set for readability (1.5-1.8 for body text)
- [ ] Hero section has gradient background and text effects
- [ ] Letter spacing, word spacing, and text transforms are applied
- [ ] Contrast examples demonstrate WCAG compliance concepts
- [ ] All questions are answered in CSS comments
- [ ] Code is well-organized with helpful comments
- [ ] Page displays correctly in browser

---

## Testing Your Work

1. Open `typography.html` in multiple browsers
2. Test readability at different screen sizes
3. Verify Google Fonts load correctly
4. Check color contrast using WebAIM Contrast Checker
5. Use browser dev tools to inspect computed styles
6. Take screenshots showing:
   - Full page view
   - Color boxes clearly visible
   - Typography examples
   - Hero section

---

## Common Mistakes to Avoid

- Forgetting to import Google Fonts before using them
- Using too many different fonts (stick to 2-3 maximum)
- Setting line-height too low (makes text cramped)
- Using pure black (#000) on pure white (harsh contrast)
- Forgetting fallback fonts in font-family
- Not testing on different screen sizes
- Mixing up rgba() and rgb() syntax
- Using # with rgb() or hsl() values

---

## Helpful Resources

- Google Fonts: fonts.google.com
- WebAIM Contrast Checker: webaim.org/resources/contrastchecker
- Color picker: htmlcolorcodes.com
- Typography scale calculator: type-scale.com
- Fontsquirrel @font-face generator: fontsquirrel.com/tools/webfont-generator

---

## Submission Format

Submit a folder named `LastName_FirstName_Task2` containing:

1. `typography.html`
2. `typography.css`
3. `screenshots/` folder with:
   - Full page screenshot
   - Close-up of color boxes
   - Typography examples
4. `reflection.txt` answering:
   - Why did you choose these particular fonts?
   - What challenges did you face?
   - What did you learn about color and typography?

**Good luck! Typography is an art – experiment and have fun!**