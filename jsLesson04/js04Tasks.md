# Lesson 04 Tasks: DOM Manipulation Practice

---

## Task 1: GUIDED EXAMPLE - Content Changer

**Follow these steps to select and modify HTML elements.**

### Step 1: Create the HTML File
Create a file called `content-changer.html`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Content Changer</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background-color: #f0f0f0;
        }
        
        .card {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        
        .highlight {
            background-color: #fff9c4;
            padding: 10px;
            border-left: 4px solid #ffc107;
        }
    </style>
</head>
<body>
    <div class="card">
        <h1 id="title">Original Title</h1>
        <p id="description">Original description text.</p>
        <p id="info">Original info text.</p>
    </div>
    
    <script>
        // Select elements
        let titleElement = document.getElementById('title');
        let descElement = document.getElementById('description');
        let infoElement = document.getElementById('info');
        
        // Change content
        titleElement.textContent = 'JavaScript Changed This!';
        descElement.textContent = 'This text was updated using JavaScript DOM manipulation.';
        infoElement.innerHTML = 'This element now has <strong>bold text</strong> and <em>italic text</em>!';
        
        // Add a class
        descElement.classList.add('highlight');
        
        // Change a style
        titleElement.style.color = '#2196f3';
        
        // Log to console
        console.log('Content successfully updated!');
    </script>
</body>
</html>
```

### Step 2: Test It
1. Open the file in your browser
2. See the changed content and styles
3. Open the console to see the log message

### Step 3: Experiment
Try modifying:
- Change the text to something different
- Change the title color to a different color
- Add more style changes
- Try adding different classes

**✅ Checkpoint:** All content should be changed by JavaScript, not by editing the HTML.

---

## Task 2: Text Content Practice

**Goal:** Practice selecting elements and changing their text.

### Instructions:
1. Create a file called `menu.html`
2. Create an HTML structure for a restaurant menu with:
   - A main heading (h1) with id "restaurant-name"
   - 3 menu items (paragraphs with ids "item1", "item2", "item3")
   - A footer paragraph with id "hours"

3. Set the initial text to generic placeholders in HTML
4. Use JavaScript to:
   - Change the restaurant name
   - Update all three menu items with actual food items and prices
   - Update the hours

### Example Output:
```
Joe's Pizza Palace

Margherita Pizza - $12.99
Pepperoni Special - $14.99
Veggie Supreme - $13.99

Open Daily: 11am - 10pm
```

**💡 Hint:** Select each element by ID, then use `.textContent` to change it.

---

## Task 3: Style Changer

**Goal:** Practice changing element styles with JavaScript.

### Instructions:
1. Create a file called `style-practice.html`
2. Create three paragraph elements with ids "para1", "para2", "para3"
3. Add some placeholder text to each
4. Use JavaScript to style each paragraph differently:
   - Para 1: Blue text, 20px font size
   - Para 2: Red background, white text, 10px padding
   - Para 3: Green border (3px solid), 15px padding, centered text

### Requirements:
- Use `.style.property` for all styling
- Each paragraph should look distinctly different
- All styling must be done in JavaScript, not CSS

**💡 Hint:** Remember camelCase for CSS properties: `backgroundColor`, not `background-color`

---

## Task 4: Class Toggle Practice

**Goal:** Practice adding and removing CSS classes.

### Instructions:
1. Create a file called `class-toggle.html`
2. Create CSS classes in a `<style>` tag:
   - `.highlight` - yellow background, bold text
   - `.large` - 24px font size
   - `.fancy` - purple text, italic, text shadow

3. Create 3 paragraph elements with different ids
4. Use JavaScript to:
   - Add the "highlight" class to paragraph 1
   - Add the "large" class to paragraph 2
   - Add both "fancy" and "highlight" classes to paragraph 3

### Expected Result:
Each paragraph should be styled according to the classes you added via JavaScript.

**💡 Hint:** Use `.classList.add()` to add classes.

---

## Task 5: Profile Card Builder

**Goal:** Build a complete profile card using DOM manipulation.

### Instructions:
1. Create a file called `profile-builder.html`
2. Create this HTML structure:
```html
<div id="profile">
    <h2 id="name"></h2>
    <p id="job"></p>
    <p id="location"></p>
    <p id="bio"></p>
</div>
```

3. Create variables for:
   - name
   - job title
   - location
   - bio (short description)

4. Use JavaScript to populate all four elements
5. Add styling to make it look like a nice profile card

### Bonus:
- Add a CSS class to the profile div
- Style the name with a different color
- Center the entire card on the page

---

## Task 6: innerHTML Practice

**Goal:** Practice using innerHTML to add HTML elements.

### Instructions:
1. Create a file called `todo-list.html`
2. Create an empty div with id "todo-container"
3. Use JavaScript and `.innerHTML` to add:
   - An h2 heading "My To-Do List"
   - An unordered list (`<ul>`) with at least 5 to-do items (`<li>`)
   - A paragraph at the bottom with the count: "Total tasks: 5"

### Example Structure:
```html
<div id="todo-container">
    <!-- JavaScript will add everything here -->
</div>
```

### Expected Result:
```
My To-Do List
• Finish homework
• Buy groceries
• Call dentist
• Clean room
• Study JavaScript

Total tasks: 5
```

**💡 Hint:** You can create the entire HTML structure as a string and assign it to `.innerHTML`

---

## Task 7: Multi-Element Selection

**Goal:** Practice selecting and modifying multiple elements.

### Instructions:
1. Create a file called `paragraph-styler.html`
2. Create 5 paragraphs all with the class "text"
3. Give them different initial text
4. Use `querySelectorAll()` to select all paragraphs with class "text"
5. Use JavaScript to:
   - Log how many paragraphs were found
   - Change the color of the first paragraph to blue
   - Change the color of the last paragraph to red
   - Add a highlight class to the middle paragraph

### HTML Structure:
```html
<p class="text">Paragraph 1</p>
<p class="text">Paragraph 2</p>
<p class="text">Paragraph 3</p>
<p class="text">Paragraph 4</p>
<p class="text">Paragraph 5</p>
```

**💡 Hint:** Access elements by index: `elements[0]` (first), `elements[elements.length - 1]` (last)

---

## Task 8: Attribute Changer

**Goal:** Practice changing HTML attributes.

### Instructions:
1. Create a file called `image-gallery.html`
2. Create an `<img>` element with:
   - id="gallery-image"
   - src="placeholder.jpg"
   - alt="Placeholder"

3. Create a paragraph with id="caption"
4. Use JavaScript to:
   - Change the image source to a different image URL
   - Update the alt text
   - Update the caption text
   - Add a border style to the image

### Example:
```javascript
// Change to a real image or any image URL
img.src = 'https://via.placeholder.com/400';
img.alt = 'A beautiful placeholder image';
```

**💡 Hint:** You can use placeholder images from https://via.placeholder.com/

---

## Challenge Task: Dynamic Business Card

**Goal:** Create a complete, styled business card using only JavaScript.

### Instructions:
1. Create a file called `business-card.html`
2. Start with only an empty div: `<div id="card"></div>`
3. Create variables for all business card information:
   - Full name
   - Job title
   - Company name
   - Email
   - Phone
   - Website

4. Use JavaScript to build the entire card HTML inside the div
5. Add CSS classes and styles to make it look professional

### Requirements:
- Everything must be added via JavaScript (innerHTML)
- Must include all 6 pieces of information
- Must be styled nicely with CSS (create classes in a style tag)
- Should look like a real business card

### Bonus Challenges:
- Add a company logo (image)
- Add social media links
- Make it responsive
- Add a subtle shadow or border
- Use a nice color scheme

### Grading Yourself:
- ✅ All information displays correctly
- ✅ Card is styled professionally
- ✅ HTML structure is built with JavaScript
- ✅ No hardcoded content in the HTML div
- ✅ Code is organized and readable
- ✅ No errors in console

---

## Challenge Task 2: Theme Switcher

**Goal:** Create a page that can switch between light and dark themes.

### Instructions:
1. Create a file called `theme-switcher.html`
2. Create a page with:
   - A heading
   - Several paragraphs
   - A container div wrapping everything

3. Create two CSS classes:
   - `.light-theme` (light background, dark text)
   - `.dark-theme` (dark background, light text)

4. Set up your page with the light theme by default
5. Use JavaScript to switch to the dark theme after 2 seconds

### CSS Example:
```css
.light-theme {
    background-color: white;
    color: #333;
}

.dark-theme {
    background-color: #1a1a1a;
    color: #f0f0f0;
}
```

### Bonus:
- Add smooth transition effects in CSS
- Switch back and forth multiple times
- Add a visual indicator of which theme is active
- Style links differently for each theme

**💡 Hint:** Use `.classList.remove()` and `.classList.add()` to switch classes

---

## Tips for Success
1. **Select first, modify second** - Always store elements in variables
2. **Console.log your selections** - Make sure you're getting the right element
3. **Check your IDs** - They must match exactly (case-sensitive)
4. **Use camelCase for styles** - `backgroundColor` not `background-color`
5. **Test incrementally** - Add one change at a time

## Common Mistakes to Avoid
❌ `getElementById('#myId')` - Don't include the #
✅ `getElementById('myId')`

❌ Selecting before element exists - Put script at end of body
✅ Script tag after HTML elements

❌ `element.style.background-color` - Invalid syntax
✅ `element.style.backgroundColor` - CamelCase