# Lesson 2: Colors & Typography

## Learning Objectives
By the end of this lesson, you will be able to:
- Apply colors using different CSS color formats (names, RGB, hex, HSL)
- Work with transparency using RGBA and HSLA
- Choose and apply web-safe fonts and font stacks
- Integrate custom web fonts using @font-face
- Control text appearance with various CSS properties
- Manage text spacing, alignment, and decoration
- Create readable, accessible typography

---

## Working with Color in CSS

Color is one of the most impactful aspects of web design. CSS provides multiple ways to specify colors, each with its own advantages.

### Color Names

CSS recognizes **147 named colors**. These are predefined keywords that represent specific colors.

```css
h1 {
  color: red;
  background-color: lightblue;
}

p {
  color: darkgreen;
}
```

**Common color names:**
- **Basic:** `red`, `green`, `blue`, `yellow`, `black`, `white`, `gray`
- **Shades:** `lightblue`, `darkgreen`, `palevioletred`
- **Special:** `transparent`, `currentColor`

**When to use:**
- Quick prototyping
- Simple designs
- Teaching/learning

**Limitations:**
- Limited palette (only 147 colors)
- Imprecise (what exact shade is "orange"?)
- Not all names are intuitive

---

## RGB Color Values

RGB stands for **Red, Green, Blue** - the three primary colors of light. By mixing these colors at different intensities, you can create millions of colors.

### RGB Syntax

```css
color: rgb(red, green, blue);
```

Each value ranges from 0 (none of that color) to 255 (maximum of that color).

### Examples

```css
/* Primary colors */
color: rgb(255, 0, 0);       /* pure red */
color: rgb(0, 255, 0);       /* pure green */
color: rgb(0, 0, 255);       /* pure blue */

/* Secondary colors */
color: rgb(255, 255, 0);     /* yellow (red + green) */
color: rgb(255, 0, 255);     /* magenta (red + blue) */
color: rgb(0, 255, 255);     /* cyan (green + blue) */

/* Grayscale */
color: rgb(0, 0, 0);         /* black */
color: rgb(255, 255, 255);   /* white */
color: rgb(128, 128, 128);   /* gray */
color: rgb(200, 200, 200);   /* light gray */

/* Custom colors */
color: rgb(230, 120, 60);    /* custom orange */
```

### Understanding RGB Mixing

**Additive color model:** Colors are created by adding light

- All colors at 0 = black (no light)
- All colors at 255 = white (all light)
- Equal values = grayscale

**Tip:** Use online color pickers to find RGB values visually.

---

## Hexadecimal Color Codes

Hexadecimal (hex) codes are a compact way to express RGB values. They're the most common format in web development.

### Hex Syntax

```css
color: #RRGGBB;
```

Each pair of characters represents the red, green, and blue values in base-16 (hexadecimal).

### Hex Values

- `0-9` = 0-9 in decimal
- `A-F` = 10-15 in decimal

So `FF` = 255, `00` = 0

### Examples

```css
color: #FF0000;  /* red (255, 0, 0) */
color: #00FF00;  /* green (0, 255, 0) */
color: #0000FF;  /* blue (0, 0, 255) */

color: #FFFFFF;  /* white */
color: #000000;  /* black */
color: #808080;  /* gray */

color: #FF6347;  /* tomato */
color: #4169E1;  /* royal blue */
color: #FFD700;  /* gold */
```

### Shorthand Hex Codes

When pairs of digits repeat, you can use shorthand:

```css
#FF0000 → #F00    /* red */
#00FF00 → #0F0    /* green */
#0000FF → #00F    /* blue */
#FFFFFF → #FFF    /* white */
#000000 → #000    /* black */

/* But these cannot be shortened: */
#FF6347  /* tomato - digits don't repeat */
#C0C0C0  /* silver - not all pairs identical */
```

**Why use hex?**
- Compact and widely used
- Easy to copy/paste
- Standard in design tools

---

## HSL Color Values

HSL stands for **Hue, Saturation, Lightness**. This format is more intuitive for humans because it matches how we perceive color.

### HSL Syntax

```css
color: hsl(hue, saturation%, lightness%);
```

### Understanding HSL Components

**1. Hue (0-360):** Position on the color wheel
- `0` or `360` = Red
- `30` = Orange
- `60` = Yellow  
- `120` = Green
- `180` = Cyan
- `240` = Blue
- `300` = Magenta

**2. Saturation (0-100%):** Color intensity
- `0%` = Grayscale (no color)
- `50%` = Moderate color
- `100%` = Full color intensity

**3. Lightness (0-100%):** Brightness
- `0%` = Black
- `50%` = Pure color
- `100%` = White

### Examples

```css
/* Primary colors */
color: hsl(0, 100%, 50%);      /* red */
color: hsl(120, 100%, 50%);    /* green */
color: hsl(240, 100%, 50%);    /* blue */

/* Variations of blue */
color: hsl(240, 100%, 50%);    /* pure blue */
color: hsl(240, 100%, 25%);    /* dark blue */
color: hsl(240, 100%, 75%);    /* light blue */
color: hsl(240, 50%, 50%);     /* desaturated blue */

/* Grayscale */
color: hsl(0, 0%, 0%);         /* black */
color: hsl(0, 0%, 50%);        /* gray */
color: hsl(0, 0%, 100%);       /* white */
```

### Why Use HSL?

**Advantages:**
- Intuitive color adjustments
- Easy to create color variations
- Great for creating color schemes
- Better for animations

**Example: Creating a color palette**
```css
:root {
  --primary-hue: 220;
  
  --color-primary: hsl(var(--primary-hue), 70%, 50%);
  --color-primary-light: hsl(var(--primary-hue), 70%, 70%);
  --color-primary-dark: hsl(var(--primary-hue), 70%, 30%);
}
```

---

## Transparency with RGBA and HSLA

Both RGB and HSL have variants that support transparency through an **alpha channel**.

### RGBA Syntax

```css
color: rgba(red, green, blue, alpha);
```

Alpha ranges from 0 (fully transparent) to 1 (fully opaque).

### Examples

```css
background-color: rgba(255, 0, 0, 1);      /* fully opaque red */
background-color: rgba(255, 0, 0, 0.5);    /* 50% transparent red */
background-color: rgba(255, 0, 0, 0.1);    /* 10% opaque red */
background-color: rgba(0, 0, 0, 0);        /* fully transparent */
```

### HSLA Syntax

```css
color: hsla(hue, saturation%, lightness%, alpha);
```

### Examples

```css
background-color: hsla(240, 100%, 50%, 1);     /* fully opaque blue */
background-color: hsla(240, 100%, 50%, 0.5);   /* 50% transparent blue */
background-color: hsla(120, 100%, 50%, 0.3);   /* 30% opaque green */
```

### Practical Uses

**Overlays:**
```css
.overlay {
  background-color: rgba(0, 0, 0, 0.7);  /* dark overlay */
}
```

**Shadows:**
```css
.box {
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
```

**Hover effects:**
```css
.button {
  background-color: rgba(66, 133, 244, 1);
}

.button:hover {
  background-color: rgba(66, 133, 244, 0.8);
}
```

---

## Setting Text and Background Color

The two fundamental color properties are `color` (text) and `background-color`.

### Color Property

Sets the foreground color (text color):

```css
p {
  color: #333;
}

h1 {
  color: rgb(41, 128, 185);
}

.warning {
  color: hsl(0, 80%, 50%);
}
```

### Background-Color Property

Sets the background color:

```css
body {
  background-color: #f5f5f5;
}

header {
  background-color: rgb(44, 62, 80);
}

.alert {
  background-color: hsla(0, 80%, 50%, 0.1);
}
```

### Accessibility: Color Contrast

**WCAG (Web Content Accessibility Guidelines) Requirements:**
- **Normal text:** Contrast ratio of at least 4.5:1
- **Large text:** Contrast ratio of at least 3:1

**Good contrast:**
```css
.good {
  color: #333;                /* dark gray text */
  background-color: #fff;      /* white background */
  /* Contrast ratio: ~12.6:1 ✓ */
}
```

**Poor contrast:**
```css
.poor {
  color: #999;                /* light gray text */
  background-color: #bbb;      /* lighter gray background */
  /* Contrast ratio: ~1.6:1 ✗ */
}
```

**Tools to check contrast:**
- WebAIM Contrast Checker
- Chrome DevTools (Lighthouse audit)
- Contrast ratio calculators

---

## Typography Fundamentals

Good typography makes content readable, accessible, and visually appealing.

### Font Families

The `font-family` property specifies which font to use.

```css
font-family: fonts;
```

### Generic Font Families

CSS defines five generic font families:

**1. Serif** - Traditional fonts with decorative strokes
```css
font-family: serif;
/* Examples: Times New Roman, Georgia, Garamond */
```

**2. Sans-serif** - Clean fonts without decorative strokes
```css
font-family: sans-serif;
/* Examples: Arial, Helvetica, Verdana */
```

**3. Monospace** - Fixed-width fonts (every character same width)
```css
font-family: monospace;
/* Examples: Courier, Consolas, Monaco */
```

**4. Cursive** - Handwriting-style fonts
```css
font-family: cursive;
/* Examples: Comic Sans MS, Brush Script */
```

**5. Fantasy** - Decorative display fonts
```css
font-family: fantasy;
/* Examples: Impact, Papyrus */
```

### Font Stacks

A **font stack** is a list of fonts, tried in order:

```css
body {
  font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
}
```

**How it works:**
1. Try 'Helvetica Neue'
2. If not available, try Helvetica
3. If not available, try Arial
4. If not available, use browser's default sans-serif

**Best practices:**
- List specific fonts first, generic last
- Include fonts likely to be on different systems
- Always end with a generic family

**Common font stacks:**

```css
/* Modern sans-serif */
font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 
             'Helvetica Neue', Arial, sans-serif;

/* Classic serif */
font-family: Georgia, 'Times New Roman', Times, serif;

/* Modern serif */
font-family: 'Palatino Linotype', Palatino, Palladio, 'Book Antiqua', 
             Georgia, serif;

/* Monospace for code */
font-family: Consolas, 'Courier New', Courier, monospace;
```

---

## Web Fonts

Web fonts let you use custom fonts not installed on users' computers.

### The @font-face Rule

Define a custom font:

```css
@font-face {
  font-family: 'CustomFont';
  src: url('customfont.woff2') format('woff2'),
       url('customfont.woff') format('woff');
  font-weight: normal;
  font-style: normal;
}

body {
  font-family: 'CustomFont', sans-serif;
}
```

### Font Formats

**WOFF2 (Web Open Font Format 2):**
- Best compression
- Supported by all modern browsers
- **Use this as your primary format**

**WOFF:**
- Older compression
- Wider browser support
- Good fallback

**Example with multiple formats:**
```css
@font-face {
  font-family: 'MyFont';
  src: url('myfont.woff2') format('woff2'),
       url('myfont.woff') format('woff'),
       url('myfont.ttf') format('truetype');
}
```

### Google Fonts

The easiest way to use web fonts:

**1. Visit fonts.google.com**

**2. Select a font and weights**

**3. Get the import code:**
```css
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');

body {
  font-family: 'Roboto', sans-serif;
}
```

**Or use the HTML link:**
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
```

**Performance tip:** Only load the weights and styles you actually use.

---

## Font Size

Control text size with the `font-size` property.

### Absolute Units

**Pixels (px):**
```css
font-size: 16px;  /* Exact size */
```

Pros: Precise control
Cons: Doesn't scale with user preferences

**Points (pt):**
```css
font-size: 12pt;  /* Mainly for print */
```

### Relative Units

**Em (em):**
Relative to parent element's font size
```css
body { font-size: 16px; }
h1 { font-size: 2em; }  /* 32px (2 × 16px) */
```

**Root Em (rem):**
Relative to root element's font size
```css
html { font-size: 16px; }
h1 { font-size: 2rem; }  /* Always 32px */
p { font-size: 1rem; }   /* Always 16px */
```

**Percentage (%):**
```css
body { font-size: 16px; }
h1 { font-size: 200%; }  /* 32px */
```

**Viewport Units:**
```css
h1 { font-size: 5vw; }   /* 5% of viewport width */
h1 { font-size: 5vh; }   /* 5% of viewport height */
```

### Keywords

```css
font-size: xx-small;
font-size: x-small;
font-size: small;
font-size: medium;    /* browser default, usually 16px */
font-size: large;
font-size: x-large;
font-size: xx-large;

/* Relative keywords */
font-size: smaller;   /* smaller than parent */
font-size: larger;    /* larger than parent */
```

### Best Practices

```css
/* Modern approach using rem */
html {
  font-size: 16px;  /* Base size */
}

body {
  font-size: 1rem;  /* 16px */
}

h1 {
  font-size: 2.5rem;  /* 40px */
}

h2 {
  font-size: 2rem;    /* 32px */
}

small {
  font-size: 0.875rem;  /* 14px */
}
```

---

## Font Weight

Control the boldness of text:

```css
font-weight: normal;    /* 400 */
font-weight: bold;      /* 700 */

/* Numeric values */
font-weight: 100;  /* Thin */
font-weight: 200;  /* Extra Light */
font-weight: 300;  /* Light */
font-weight: 400;  /* Normal */
font-weight: 500;  /* Medium */
font-weight: 600;  /* Semi Bold */
font-weight: 700;  /* Bold */
font-weight: 800;  /* Extra Bold */
font-weight: 900;  /* Black */

/* Relative values */
font-weight: lighter;
font-weight: bolder;
```

**Note:** Font must support the weight. Google Fonts shows available weights.

---

## Font Style and Variant

```css
/* Font style */
font-style: normal;
font-style: italic;
font-style: oblique;

/* Font variant */
font-variant: normal;
font-variant: small-caps;  /* MAKES TEXT LOOK LIKE THIS */
```

---

## Text Properties

### Text Decoration

```css
text-decoration: none;          /* Remove underlines */
text-decoration: underline;
text-decoration: overline;
text-decoration: line-through;

/* Multiple values */
text-decoration: underline overline;

/* With color and style */
text-decoration: underline wavy red;
```

### Text Transform

```css
text-transform: none;
text-transform: uppercase;     /* ALL CAPS */
text-transform: lowercase;     /* all lowercase */
text-transform: capitalize;    /* First Letter Of Each Word */
```

### Text Alignment

```css
text-align: left;
text-align: right;
text-align: center;
text-align: justify;  /* Stretch lines to fill width */
```

### Vertical Alignment

For inline and inline-block elements:

```css
vertical-align: baseline;   /* Default */
vertical-align: top;
vertical-align: middle;
vertical-align: bottom;
vertical-align: sub;        /* Subscript */
vertical-align: super;      /* Superscript */
vertical-align: text-top;
vertical-align: text-bottom;
```

---

## Text Spacing

### Letter Spacing (Kerning)

Space between characters:

```css
letter-spacing: normal;
letter-spacing: 0.1em;
letter-spacing: 2px;
letter-spacing: -1px;  /* Tighter */
```

### Word Spacing (Tracking)

Space between words:

```css
word-spacing: normal;
word-spacing: 0.3em;
word-spacing: 5px;
```

### Line Height (Leading)

Space between lines of text:

```css
line-height: normal;
line-height: 1.5;      /* 1.5× font size */
line-height: 24px;
line-height: 150%;
```

**Best practice:** Use unitless numbers (they multiply by font size)

```css
p {
  font-size: 16px;
  line-height: 1.6;  /* 25.6px line height */
}
```

### Text Indent

Indent the first line:

```css
text-indent: 2em;      /* Indent first line */
text-indent: 50px;
text-indent: -1em;     /* Hanging indent */
```

---

## Shorthand Font Property

Combine multiple font properties:

```css
font: style variant weight size/line-height family;
```

**Examples:**

```css
/* Full syntax */
font: italic small-caps bold 16px/1.5 Georgia, serif;

/* Minimum required: size and family */
font: 16px Arial, sans-serif;

/* Common usage */
font: normal 400 1rem/1.6 'Helvetica Neue', sans-serif;
```

**What gets reset:** Using `font` shorthand resets any font properties not specified.

---

## Progressive Enhancement

Layer styles for broader compatibility:

```css
.element {
  /* Fallback for older browsers */
  background-color: blue;
  
  /* Modern browsers with transparency */
  background-color: rgba(0, 0, 255, 0.5);
}
```

Older browsers ignore properties they don't understand, using the previous value.

---

## Summary

In this lesson, you learned:

- CSS offers multiple color formats: names, RGB, hex, and HSL
- RGBA and HSLA add transparency
- Font stacks provide fallbacks when fonts aren't available
- Web fonts extend design possibilities
- Font size can be set with absolute or relative units (prefer relative)
- Typography involves font families, weights, styles, and spacing
- Text spacing (letter, word, line) affects readability
- Progressive enhancement ensures broader browser support

Next lesson: Box Model & Layout!