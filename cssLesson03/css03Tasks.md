# Task 3: Box Model & Layout

## Objective
Master the CSS box model by working with padding, margins, borders, and list styling to create well-spaced, professional layouts.

## Setup
Create:
- `layout.html`
- `layout.css`

**Total Points: 100**

---

## Part A: Product Cards with Box Model (30 points)

1. Create `layout.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Box Model Practice</title>
  <link rel="stylesheet" href="layout.css">
</head>
<body>
  <div class="container">
    <h1>Our Products</h1>
    
    <div class="card-grid">
      <div class="card">
        <div class="card-image">📱</div>
        <h2>Smartphone</h2>
        <p class="description">Latest model with advanced features.</p>
        <p class="price">$699</p>
        <button class="buy-button">Add to Cart</button>
      </div>
      
      <div class="card featured">
        <div class="featured-badge">Featured</div>
        <div class="card-image">💻</div>
        <h2>Laptop</h2>
        <p class="description">Powerful laptop for professionals.</p>
        <p class="price">$1,299</p>
        <button class="buy-button">Add to Cart</button>
      </div>
      
      <div class="card">
        <div class="card-image">⌚</div>
        <h2>Smart Watch</h2>
        <p class="description">Track your fitness and stay connected.</p>
        <p class="price">$399</p>
        <button class="buy-button">Add to Cart</button>
      </div>
    </div>
  </div>
</body>
</html>
```

2. Style the cards (30 points):

**Requirements for `.card`:**
- Width: 300px
- Padding: 25px
- Border: 1px solid #e0e0e0
- Border-radius: 12px
- Margin-bottom: 30px
- Background: white
- Box shadow: 0 4px 6px rgba(0,0,0,0.1)
- Use `box-sizing: border-box`

**Requirements for `.featured`:**
- Border: 3px solid #4CAF50
- Position relative (for badge positioning)

**Requirements for `.featured-badge`:**
- Position absolute, top-right corner
- Background: #4CAF50
- Color: white
- Padding: 5px 15px
- Border-radius: 0 12px 0 8px
- Font size: 0.8rem
- Font weight: bold

**Requirements for `.price`:**
- Color: #4CAF50
- Font size: 1.5rem
- Font-weight: bold
- Margin: 15px 0

**Grading:**
- Proper use of padding (7 points)
- Proper use of margins (7 points)
- Border and border-radius (8 points)
- Featured card stands out (8 points)

---

## Part B: Styled Navigation with Lists (20 points)

3. Add navigation to your HTML (before `.container`):

```html
<nav class="main-nav">
  <ul>
    <li><a href="#home">Home</a></li>
    <li><a href="#products">Products</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#blog">Blog</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>
```

4. Style the navigation:

**Requirements:**
- Remove list-style from ul
- Remove default padding/margin from ul
- Display list items as inline-block
- Style links:
  - Padding: 12px 20px
  - No text decoration
  - Color: #333
  - Border-radius: 4px
  - Add smooth transition (0.3s)
- Hover effect: background #4CAF50, color white
- Add 5px margin-right between items
- Center the navigation

**Grading:**
- List styling removed correctly (5 points)
- Links properly padded and styled (10 points)
- Hover effect works smoothly (5 points)

---

## Part C: Container Layout (15 points)

5. Style `.container`:

```css
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 20px;
}

.container h1 {
  text-align: center;
  margin-bottom: 40px;
  font-size: 2.5rem;
}
```

6. Create `.card-grid` for responsive layout:

```css
.card-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
  justify-content: center;
}
```

**Grading:**
- Container properly centered (8 points)
- Spacing is consistent (7 points)

---

## Part D: Feature List Styling (15 points)

7. Add features to one card:

```html
<div class="card">
  <div class="card-image">💻</div>
  <h2>Premium Laptop</h2>
  <ul class="features">
    <li>16GB RAM</li>
    <li>512GB SSD</li>
    <li>15" Retina Display</li>
    <li>All-day Battery</li>
  </ul>
  <p class="price">$1,899</p>
  <button class="buy-button">Add to Cart</button>
</div>
```

8. Style `.features` list:

**Requirements:**
- Custom bullet: use checkmark ✓
- Remove default list styling
- Padding-left: 0
- Each item: margin-bottom: 8px
- Use ::before pseudo-element for custom bullet
- Bullet color: #4CAF50

**Grading:**
- Custom bullets implemented (8 points)
- Proper spacing (7 points)

---

## Part E: Border Variations (20 points)

9. Add different card types:

```html
<div class="card card-success">
  <h2>In Stock</h2>
  <p>This product is available now.</p>
</div>

<div class="card card-warning">
  <h2>Low Stock</h2>
  <p>Only a few items remaining!</p>
</div>

<div class="card card-danger">
  <h2>Out of Stock</h2>
  <p>This product is temporarily unavailable.</p>
</div>
```

10. Style with different borders:

**Requirements for each:**
- `.card-success`: 4px solid left border, #4CAF50
- `.card-warning`: 4px solid left border, #FF9800
- `.card-danger`: 4px solid left border, #F44336
- Add corresponding background colors (very light tints)
- Match heading colors to border colors

**Grading:**
- All border styles correct (10 points)
- Colors and visual hierarchy clear (10 points)

---

## Bonus Challenges (20 extra points)

### Bonus 1: Box Shadow Hover Effect (10 points)
Add hover effects to cards:
```css
.card {
  transition: all 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 16px rgba(0,0,0,0.2);
}
```

### Bonus 2: Nested Lists (10 points)
Create a nested list with different styling for each level:
```html
<ul class="category-list">
  <li>Electronics
    <ul>
      <li>Phones</li>
      <li>Laptops</li>
      <li>Tablets</li>
    </ul>
  </li>
  <li>Accessories
    <ul>
      <li>Cases</li>
      <li>Chargers</li>
    </ul>
  </li>
</ul>
```

Style with different markers for each level.

---

## Submission Checklist

- [ ] Box model properties used correctly throughout
- [ ] All cards have proper padding, margins, borders
- [ ] Navigation list is properly styled
- [ ] Container centers and limits content width
- [ ] Feature lists have custom bullets
- [ ] Border variations demonstrate different card states
- [ ] Code is well-organized and commented
- [ ] Page displays correctly in browser

**Submit your folder with both HTML and CSS files plus screenshots!**