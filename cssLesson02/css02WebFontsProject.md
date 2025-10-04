# Project 5: Web Fonts - Themed Image Gallery

## Project Overview
Create a themed image gallery webpage that demonstrates mastery of web font implementation using both locally hosted fonts and Google Fonts. You'll build 5 distinct themed sections, each with custom typography that matches its visual style.

## Setup
Create the following folder structure:
```
web-fonts-project/
├── index.html
├── styles.css
├── fonts/
│   ├── font1.woff2
│   └── font2.woff2
└── images/
    ├── scifi.jpg (or similar)
    ├── holiday.jpg
    ├── sports.jpg
    ├── news.jpg
    └── outdoor.jpg
```

**Total Points: 100**

---

## Part A: HTML Structure and Google Fonts Links (15 points)

1. Create `index.html` with the basic structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web Fonts Gallery</title>
    
    <!-- GOOGLE FONTS: Link to 3 fonts here -->
    <!-- Font 1: For Sci-Fi theme -->
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap" rel="stylesheet">
    
    <!-- Font 2: For your second theme -->
    
    <!-- Font 3: For your third theme -->
    
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Themed Image Gallery</h1>
        <p class="subtitle">Exploring Typography Across Different Visual Styles</p>
    </header>

    <div class="gallery">
        <!-- Theme cards will go here -->
    </div>
</body>
</html>
```

2. Add 5 theme cards using this structure (repeat for each theme):

```html
<div class="theme-card scifi">
    <div class="image-container">
        <img src="images/scifi.jpg" alt="Sci-Fi theme">
        <h2 class="image-title">Future Tech</h2>
    </div>
    <p class="description">Exploring the cutting edge of technology and innovation in a futuristic world.</p>
</div>
```

**Required Themes (use these class names):**
- `.scifi` - Sci-Fi/Futuristic
- `.holiday` - Any holiday you choose
- `.sports` - Athletic/Sports
- `.news` - Journalism/News
- `.outdoor` - Nature/Adventure

**Grading:**
- Proper HTML structure with all required elements (5 points)
- Three Google Fonts linked correctly in `<head>` (6 points)
- All 5 theme cards present with correct class names (4 points)

---

## Part B: Downloading and Converting Fonts (10 points)

3. Download and convert TWO fonts:

**Process:**
1. Go to [Google Fonts](https://fonts.google.com/)
2. Download 2 font families (choose fonts that match 2 of your remaining themes)
3. Go to [Font Converter](https://www.fontconverter.io/en/)
4. Upload your .ttf files
5. Download the converted .woff2 files
6. Save them to your `fonts/` folder

**Font Selection Guidelines:**
- Holiday theme: Decorative, festive font
- Sports theme: Bold, energetic font
- News theme: Classic, readable serif or sans-serif
- Outdoor theme: Rugged or natural-feeling font

**Grading:**
- Two .woff2 font files in fonts folder (5 points)
- Fonts appropriately match theme styles (5 points)

---

## Part C: @font-face Declarations (15 points)

4. At the top of `styles.css`, define your downloaded fonts:

```css
/* Downloaded Font 1 */
@font-face {
    font-family: 'CustomFont1';
    src: url('fonts/your-font-name.woff2') format('woff2');
    font-weight: normal;
    font-style: normal;
}

/* Downloaded Font 2 */
@font-face {
    font-family: 'CustomFont2';
    src: url('fonts/your-other-font.woff2') format('woff2');
    font-weight: normal;
    font-style: normal;
}
```

**Requirements:**
- Use descriptive font-family names that relate to the theme
- Correct file path to fonts folder
- Proper format declaration
- Both fonts declared

**Grading:**
- First @font-face declaration correct (7 points)
- Second @font-face declaration correct (7 points)
- Descriptive naming (1 point)

---

## Part D: Global Styles (10 points)

5. Add base styling to your page:

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background: #f5f5f5;
    padding: 20px;
    line-height: 1.6;
}

header {
    text-align: center;
    margin-bottom: 40px;
    padding: 20px;
    background: white;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

header h1 {
    font-size: 2.5rem;
    color: #333;
    margin-bottom: 10px;
}

.subtitle {
    font-size: 1.1rem;
    color: #666;
}
```

**Grading:**
- Reset styles and box-sizing (2 points)
- Body styling (2 points)
- Header styling (6 points)

---

## Part E: Flexbox Gallery Layout (20 points)

6. Create the gallery layout using Flexbox:

```css
.gallery {
    display: flex;
    flex-wrap: wrap;
    justify-content: center; /* or space-around/space-between */
    gap: 30px;
    max-width: 1400px;
    margin: 0 auto;
}

.theme-card {
    width: 250px; /* Adjust based on your design */
    background: white;
    border-radius: 12px;
    box-shadow: 0 8px 20px rgba(0,0,0,0.15);
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.theme-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 25px rgba(0,0,0,0.2);
}

.image-container {
    position: relative;
    width: 100%;
    height: 300px; /* Adjust based on your images */
    overflow: hidden;
}

.image-container img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.3s ease;
}

.theme-card:hover .image-container img {
    transform: scale(1.05);
}
```

**Requirements:**
- Gallery uses flexbox with proper wrapping
- Cards have consistent width
- Card spacing using gap property
- Cards centered on page with max-width
- Cards have rounded corners and shadow
- Smooth hover effects on cards

**Grading:**
- Flexbox gallery setup (5 points)
- Card sizing and spacing (5 points)
- Image container with proper dimensions (5 points)
- Hover effects working smoothly (5 points)

---

## Part F: Image Titles with Overlays (10 points)

7. Style the titles that overlay the images:

```css
.image-title {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background: linear-gradient(transparent, rgba(0,0,0,0.8));
    color: white;
    padding: 20px 10px 10px;
    font-size: 1.4rem;
    font-weight: bold;
    text-align: center;
    text-shadow: 2px 2px 4px rgba(0,0,0,0.8);
}
```

**Requirements:**
- Position absolute within image container
- Gradient background overlay
- White text with shadow for readability
- Appropriate font size (1.2rem - 1.6rem)
- Centered text

**Grading:**
- Positioning and overlay (5 points)
- Text styling and readability (5 points)

---

## Part G: Description Styling (5 points)

8. Style the description text below images:

```css
.description {
    padding: 15px;
    font-size: 0.9rem;
    line-height: 1.4;
    color: #555;
    text-align: center;
}
```

**Requirements:**
- Appropriate padding
- Readable font size (0.85rem - 1rem)
- Good line height for readability
- Appropriate text color

**Grading:**
- All description requirements met (5 points)

---

## Part H: Theme-Specific Font Assignments (15 points)

9. Assign each font to its theme. Here's the pattern:

```css
/* Sci-Fi Theme - Google Font */
.scifi .image-title,
.scifi .description {
    font-family: 'Orbitron', monospace;
}

/* Holiday Theme - Downloaded Font */
.holiday .image-title,
.holiday .description {
    font-family: 'CustomHoliday', serif;
}

/* Sports Theme - Google Font */
.sports .image-title,
.sports .description {
    font-family: 'FontName', sans-serif;
}

/* News Theme - Downloaded Font */
.news .image-title,
.news .description {
    font-family: 'CustomNews', serif;
}

/* Outdoor Theme - Google Font */
.outdoor .image-title,
.outdoor .description {
    font-family: 'FontName', sans-serif;
}
```

**Requirements:**
- All 5 themes have font-family assigned
- 3 themes use Google Fonts (linked in HTML)
- 2 themes use downloaded fonts (@font-face)
- Fonts match theme aesthetics
- Both title and description use the theme font

**Grading:**
- All 5 themes assigned fonts (5 points)
- Correct distribution (3 Google, 2 downloaded) (5 points)
- Fonts aesthetically match themes (5 points)

---

## Bonus Challenges (20 extra points)

### Bonus 1: Font Weights and Styles (10 points)
Import multiple weights from Google Fonts and demonstrate:
- Use bold weight (700) for titles
- Use regular weight (400) for descriptions
- Add italic style to at least one description

```css
/* Example in your Google Fonts link: */
/* https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap */
```

### Bonus 2: Advanced Typography Effects (10 points)
Add sophisticated typography styling:
- Use `letter-spacing` on at least one title for dramatic effect
- Use `text-transform: uppercase` on at least one theme
- Add custom `line-height` for improved readability
- Use `font-variant: small-caps` on at least one element

```css
.scifi .image-title {
    letter-spacing: 3px;
    text-transform: uppercase;
}
```

---

## Content Requirements

### Images
- Find or create 5 images that clearly represent each theme
- All images should be similar dimensions (recommended: 400-600px wide)
- Use royalty-free images or AI-generated content
- Save as .jpg or .png in the images folder

### Text Content
For each theme:
- **Title**: 2-3 words that capture the theme
- **Description**: 1-2 sentences (15-30 words)
- Content should be relevant and engaging

**Example Content:**

**Sci-Fi:**
- Title: "Future Tech"
- Description: "Exploring the cutting edge of technology and innovation in a futuristic world."

**Holiday:**
- Title: "Festive Joy"
- Description: "Celebrate the magic of the season with warmth, tradition, and togetherness."

---

## Font Pairing Suggestions

Here are recommended font combinations:

**Sci-Fi:** Orbitron, Audiowide, Electrolize, Exo 2
**Holiday:** Mountains of Christmas, Lobster, Great Vibes, Pacifico
**Sports:** Teko, Bebas Neue, Anton, Archivo Black
**News:** Merriweather, Playfair Display, Lora, PT Serif
**Outdoor:** Cabin, Montserrat, Raleway, Lato

Browse more at [Google Fonts](https://fonts.google.com/)

---

## Submission Checklist

- [ ] HTML file with all 5 theme cards
- [ ] Three Google Fonts linked in `<head>`
- [ ] Two downloaded .woff2 font files in fonts folder
- [ ] Two @font-face declarations in CSS
- [ ] All 5 themes have custom fonts assigned
- [ ] Flexbox gallery layout working correctly
- [ ] All images present and properly sized
- [ ] Image titles overlay images with gradient
- [ ] Descriptions styled below each image
- [ ] Hover effects work smoothly
- [ ] Cards have shadows and rounded corners
- [ ] All content is original and theme-appropriate
- [ ] Page is visually polished and professional
- [ ] Code is well-organized and commented

**Submit your complete project folder with screenshots showing:**
1. The full gallery page
2. Hover state on one card
3. Your fonts folder contents
4. Close-up of at least 2 different themes

---

## Grading Summary

| Section | Points |
|---------|--------|
| HTML Structure & Google Fonts Links | 15 |
| Font Download & Conversion | 10 |
| @font-face Declarations | 15 |
| Global Styles | 10 |
| Flexbox Gallery Layout | 20 |
| Image Title Overlays | 10 |
| Description Styling | 5 |
| Theme-Specific Font Assignments | 15 |
| **Total** | **100** |
| **Bonus Challenges** | **20** |

---

## Key Learning Outcomes

By completing this project, you will demonstrate:
- Ability to implement web fonts using multiple methods
- Understanding of @font-face syntax and local font hosting
- Skill in linking and applying Google Fonts
- Proficiency with Flexbox layout techniques
- Knowledge of CSS positioning for overlays
- Understanding of font pairing and typography principles
- Ability to create cohesive themed designs
- Skill in creating hover effects and transitions

**This project combines typography mastery with layout skills to create a professional, interactive gallery!**