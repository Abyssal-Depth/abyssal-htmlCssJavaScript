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
        // Select elements by their ID
        let titleElement = document.getElementById('title');
        let descElement = document.getElementById('description');
        let infoElement = document.getElementById('info');
        
        // Change content using textContent
        titleElement.textContent = 'JavaScript Changed This!';
        descElement.textContent = 'This text was updated using JavaScript DOM manipulation.';
        
        // Use innerHTML when you want to add HTML tags inside
        infoElement.innerHTML = 'This element now has <strong>bold text</strong> and <em>italic text</em>!';
        
        // Add a CSS class to an element
        descElement.classList.add('highlight');
        
        // Change inline styles directly
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
3. Open the console (F12) to see the log message

### Step 3: Experiment
Try modifying:
- Change the text to something different
- Change the title color to a different color (try 'red', '#ff5722', 'rgb(76, 175, 80)')
- Add more style changes (fontSize, backgroundColor)
- Try adding different classes

**✅ Checkpoint:** All content should be changed by JavaScript, not by editing the HTML directly.

---

## Task 2: Text Content Practice

**Goal:** Practice selecting elements and changing their text.

### Instructions:
1. Create a file called `menu.html`
2. Create an HTML structure for a restaurant menu
3. Set initial text to generic placeholders in HTML
4. Use JavaScript to update everything with real content

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Restaurant Menu</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background-color: #fafafa;
        }
        h1 {
            text-align: center;
            color: #d32f2f;
        }
        .menu-item {
            padding: 10px;
            margin: 10px 0;
            background-color: white;
            border-left: 4px solid #d32f2f;
        }
        #hours {
            text-align: center;
            font-style: italic;
            color: #666;
        }
    </style>
</head>
<body>
    <h1 id="restaurant-name">Restaurant Name</h1>
    
    <p class="menu-item" id="item1">Menu item 1</p>
    <p class="menu-item" id="item2">Menu item 2</p>
    <p class="menu-item" id="item3">Menu item 3</p>
    
    <p id="hours">Hours info</p>
    
    <script>
        // Select the restaurant name element
        let restaurantName = document.getElementById('restaurant-name');
        
        // Change the restaurant name
        restaurantName.textContent = "Joe's Pizza Palace";
        
        // Select menu items
        let menuItem1 = document.getElementById('item1');
        let menuItem2 = document.getElementById('item2');
        let menuItem3 = document.getElementById('item3');
        
        // Update menu items (you complete these)
        menuItem1.textContent = "Margherita Pizza - $12.99";
        // Add item2 here
        // Add item3 here
        
        // Select and update hours
        let hoursElement = document.getElementById('hours');
        // Update the hours here
        
        console.log('Menu updated!');
    </script>
</body>
</html>
```

### Expected Output:
```
Joe's Pizza Palace

Margherita Pizza - $12.99
Pepperoni Special - $14.99
Veggie Supreme - $13.99

Open Daily: 11am - 10pm
```

**💡 Hint:** Select each element by ID using `document.getElementById()`, then use `.textContent` to change the text.

---

## Task 3: Style Changer

**Goal:** Practice changing element styles with JavaScript.

### Instructions:
1. Create a file called `style-practice.html`
2. Create three paragraphs with some placeholder text
3. Use JavaScript to style each paragraph differently

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Style Practice</title>
</head>
<body>
    <h1>Styling Elements with JavaScript</h1>
    
    <p id="para1">This is paragraph 1. It will be styled with blue text and larger font.</p>
    <p id="para2">This is paragraph 2. It will have a red background with white text.</p>
    <p id="para3">This is paragraph 3. It will have a green border and be centered.</p>
    
    <script>
        // Select paragraph 1
        let para1 = document.getElementById('para1');
        
        // Style paragraph 1 - blue text, 20px font
        para1.style.color = 'blue';
        para1.style.fontSize = '20px';
        
        // Select paragraph 2
        let para2 = document.getElementById('para2');
        
        // Style paragraph 2 - red background, white text, padding
        // Add styles here...
        // Hint: use backgroundColor, color, and padding
        
        // Select paragraph 3
        let para3 = document.getElementById('para3');
        
        // Style paragraph 3 - green border, padding, centered
        // Add styles here...
        // Hint: use border, padding, and textAlign
        
        console.log('Styles applied!');
    </script>
</body>
</html>
```

### Requirements:
- Para 1: Blue text (`color`), 20px font size (`fontSize`)
- Para 2: Red background (`backgroundColor`), white text, 10px padding (`padding`)
- Para 3: Green border (`border: '3px solid green'`), 15px padding, centered text (`textAlign: 'center'`)

**💡 Important:** CSS properties in JavaScript use camelCase:
- CSS: `background-color` → JavaScript: `backgroundColor`
- CSS: `font-size` → JavaScript: `fontSize`
- CSS: `text-align` → JavaScript: `textAlign`

---

## Task 4: Class Toggle Practice

**Goal:** Practice adding and removing CSS classes.

### Instructions:
1. Create a file called `class-toggle.html`
2. Create CSS classes in a style tag
3. Use JavaScript to add classes to different paragraphs

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Class Toggle</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
        }
        
        /* CSS classes to be added by JavaScript */
        .highlight {
            background-color: #ffeb3b;
            font-weight: bold;
            padding: 10px;
        }
        
        .large {
            font-size: 24px;
        }
        
        .fancy {
            color: purple;
            font-style: italic;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
    </style>
</head>
<body>
    <h1>Class Toggle Practice</h1>
    
    <p id="para1">This paragraph will get the highlight class.</p>
    <p id="para2">This paragraph will get the large class.</p>
    <p id="para3">This paragraph will get both fancy and highlight classes.</p>
    
    <script>
        // Select paragraph 1 and add 'highlight' class
        let para1 = document.getElementById('para1');
        para1.classList.add('highlight');
        
        // Select paragraph 2 and add 'large' class
        // Your code here...
        
        // Select paragraph 3 and add both 'fancy' and 'highlight' classes
        // Your code here...
        // Hint: You can call classList.add() twice, or pass both: .add('fancy', 'highlight')
        
        console.log('Classes added successfully!');
    </script>
</body>
</html>
```

### Expected Result:
- Paragraph 1: Yellow background, bold
- Paragraph 2: Large 24px text
- Paragraph 3: Purple italic text with shadow AND yellow background

**💡 Hint:** Use `.classList.add('className')` to add classes. You can add multiple classes by calling it multiple times or passing multiple arguments.

---

## Task 5: Profile Card Builder

**Goal:** Build a complete profile card using DOM manipulation.

### Instructions:
1. Create a file called `profile-builder.html`
2. Create variables for profile information
3. Use JavaScript to populate all elements
4. Add styling to make it look nice

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Profile Builder</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #e0e0e0;
            padding: 20px;
        }
        
        #profile {
            max-width: 400px;
            margin: 50px auto;
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        
        #profile h2 {
            margin-top: 0;
            color: #1976d2;
        }
        
        #profile p {
            color: #555;
            line-height: 1.6;
        }
    </style>
</head>
<body>
    <div id="profile">
        <h2 id="name"></h2>
        <p id="job"></p>
        <p id="location"></p>
        <p id="bio"></p>
    </div>
    
    <script>
        // Create profile data variables
        let personName = "Sarah Johnson";
        let jobTitle = "Web Developer";
        let personLocation = "San Francisco, CA";
        let personBio = "Passionate about creating beautiful and functional websites. Love learning new technologies!";
        
        // Select elements
        let nameElement = document.getElementById('name');
        let jobElement = document.getElementById('job');
        let locationElement = document.getElementById('location');
        let bioElement = document.getElementById('bio');
        
        // Populate the profile card
        nameElement.textContent = personName;
        // Add the rest of the content here...
        
        // Bonus: Add some extra styling
        nameElement.style.textAlign = 'center';
        // Try adding more styles...
        
        console.log('Profile card created!');
    </script>
</body>
</html>
```

### Bonus Challenges:
- Change the name color to something different
- Center all the text
- Add a border to the profile div
- Make the job title italic

**💡 Hint:** You can add styles directly to elements after populating them with content!

---

## Task 6: innerHTML Practice

**Goal:** Practice using innerHTML to add HTML elements.

### Instructions:
1. Create a file called `todo-list.html`
2. Create an empty div
3. Use `.innerHTML` to build the entire to-do list structure inside it

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>To-Do List</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 500px;
            margin: 50px auto;
            padding: 20px;
        }
        
        #todo-container {
            background-color: #f5f5f5;
            padding: 20px;
            border-radius: 8px;
        }
        
        ul {
            list-style-type: square;
        }
        
        li {
            padding: 5px 0;
        }
    </style>
</head>
<body>
    <div id="todo-container">
        <!-- JavaScript will add everything here -->
    </div>
    
    <script>
        // Select the container
        let container = document.getElementById('todo-container');
        
        // Create the HTML structure as a string
        // Using template literals makes this easier!
        let todoHTML = `
            <h2>My To-Do List</h2>
            <ul>
                <li>Finish homework</li>
                <li>Buy groceries</li>
                <li>Call dentist</li>
                <!-- Add 2 more items here -->
            </ul>
            <p>Total tasks: 5</p>
        `;
        
        // Add the HTML to the container
        container.innerHTML = todoHTML;
        
        console.log('To-do list created!');
    </script>
</body>
</html>
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

**💡 Hint:** Template literals (backticks) let you write HTML across multiple lines, making it much easier to read!

---

## Task 7: Multi-Element Selection

**Goal:** Practice selecting and modifying multiple elements.

### Instructions:
1. Create a file called `paragraph-styler.html`
2. Create 5 paragraphs with the same class
3. Use `querySelectorAll()` to select all of them at once
4. Style different paragraphs by their index position

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Paragraph Styler</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
        }
        
        .highlight {
            background-color: #ffeb3b;
            padding: 10px;
        }
    </style>
</head>
<body>
    <h1>Multi-Element Selection</h1>
    
    <p class="text">Paragraph 1 - This will be blue</p>
    <p class="text">Paragraph 2 - This stays normal</p>
    <p class="text">Paragraph 3 - This will be highlighted (middle)</p>
    <p class="text">Paragraph 4 - This stays normal</p>
    <p class="text">Paragraph 5 - This will be red</p>
    
    <script>
        // Select ALL elements with class "text"
        let paragraphs = document.querySelectorAll('.text');
        
        // Log how many were found
        console.log('Number of paragraphs:', paragraphs.length);
        
        // Change first paragraph to blue
        paragraphs[0].style.color = 'blue';
        
        // Change last paragraph to red
        // Hint: Use paragraphs.length - 1 to get the last index
        paragraphs[paragraphs.length - 1].style.color = 'red';
        
        // Add highlight class to middle paragraph (index 2)
        // Your code here...
        
        console.log('Paragraphs styled!');
    </script>
</body>
</html>
```

### Key Concepts:
- `querySelectorAll()` returns a list (NodeList) of elements
- Access elements by index: `paragraphs[0]`, `paragraphs[1]`, etc.
- First element is at index 0
- Last element is at index `paragraphs.length - 1`
- Middle element (of 5) is at index 2

**💡 Hint:** In an array of 5 items (indexes 0-4), the middle one is at index 2.

---

## Task 8: Attribute Changer

**Goal:** Practice changing HTML attributes.

### Instructions:
1. Create a file called `image-gallery.html`
2. Create an image element with placeholder attributes
3. Use JavaScript to change the image source, alt text, and styling

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Image Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            text-align: center;
        }
        
        #gallery-image {
            max-width: 100%;
            height: auto;
        }
        
        #caption {
            font-style: italic;
            color: #666;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <h1>Image Gallery</h1>
    
    <img id="gallery-image" src="placeholder.jpg" alt="Placeholder">
    <p id="caption">Original caption</p>
    
    <script>
        // Select the image element
        let img = document.getElementById('gallery-image');
        
        // Change the image source
        // Using a placeholder service for a real image
        img.src = 'https://via.placeholder.com/400/0000FF/FFFFFF?text=Changed+Image';
        
        // Change the alt text
        img.alt = 'A blue placeholder image';
        
        // Add a border style
        img.style.border = '5px solid #2196f3';
        img.style.borderRadius = '10px';
        
        // Select and update the caption
        let caption = document.getElementById('caption');
        // Update the caption text here...
        
        console.log('Image updated!');
    </script>
</body>
</html>
```

### Try These Variations:
Change the placeholder URL to experiment with different images:
```javascript
// Red background with white text
img.src = 'https://via.placeholder.com/400/FF0000/FFFFFF?text=Red+Box';

// Green background, size 300x300
img.src = 'https://via.placeholder.com/300/00FF00/000000?text=Green';
```

**💡 Hint:** You can change any HTML attribute with JavaScript: `element.src`, `element.alt`, `element.href`, etc.

---

## Challenge Task: Dynamic Business Card

**Goal:** Create a complete, styled business card using only JavaScript.

### Instructions:
1. Create a file called `business-card.html`
2. Start with minimal HTML - just an empty div
3. Use JavaScript to build the entire card

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Business Card</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #eceff1;
            padding: 50px;
        }
        
        .card {
            max-width: 400px;
            margin: 0 auto;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }
        
        .card h2 {
            margin: 0 0 5px 0;
            font-size: 28px;
        }
        
        .card .title {
            font-size: 16px;
            opacity: 0.9;
            margin-bottom: 20px;
        }
        
        .card .info {
            margin: 10px 0;
            font-size: 14px;
        }
        
        .card .company {
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.3);
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div id="card"></div>
    
    <script>
        // Business card information
        let fullName = "Alex Chen";
        let jobTitle = "Senior Web Developer";
        let company = "TechCorp Solutions";
        let email = "alex.chen@techcorp.com";
        let phone = "(555) 123-4567";
        let website = "www.alexchen.dev";
        
        // Select the card container
        let cardDiv = document.getElementById('card');
        
        // Build the card HTML using template literals
        let cardHTML = `
            <h2>${fullName}</h2>
            <div class="title">${jobTitle}</div>
            <div class="info">📧 ${email}</div>
            <div class="info">📱 ${phone}</div>
            <div class="info">🌐 ${website}</div>
            <div class="company">${company}</div>
        `;
        
        // Add the card class to the div
        cardDiv.classList.add('card');
        
        // Insert the HTML
        cardDiv.innerHTML = cardHTML;
        
        console.log('Business card created for', fullName);
    </script>
</body>
</html>
```

### Your Turn:
1. Change all the variables to YOUR information
2. Experiment with different colors in the CSS gradient
3. Add more information (like address or LinkedIn)

### Bonus Challenges:
- Add an image/logo at the top
- Change the gradient colors
- Add social media links
- Add hover effects in CSS
- Try a different layout (side-by-side columns?)

### Grading Yourself:
- ✅ All 6 pieces of information display
- ✅ Card is styled professionally
- ✅ HTML built with JavaScript (.innerHTML)
- ✅ No hardcoded content in the HTML
- ✅ No errors in console
- ✅ Uses template literals effectively

---

## Challenge Task 2: Theme Switcher

**Goal:** Create a page that can switch between light and dark themes.

### Instructions:
1. Create a file called `theme-switcher.html`
2. Create content with a light theme by default
3. Use JavaScript to switch to dark theme after a delay

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Theme Switcher</title>
    <style>
        /* Light theme styles */
        .light-theme {
            background-color: white;
            color: #333;
            transition: all 0.3s ease;
        }
        
        /* Dark theme styles */
        .dark-theme {
            background-color: #1a1a1a;
            color: #f0f0f0;
            transition: all 0.3s ease;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 50px 20px;
            min-height: 100vh;
        }
        
        h1 {
            text-align: center;
        }
        
        p {
            line-height: 1.8;
            margin: 20px 0;
        }
        
        .theme-indicator {
            text-align: center;
            font-weight: bold;
            padding: 20px;
            margin: 20px 0;
            border-radius: 8px;
            background-color: rgba(0,0,0,0.1);
        }
    </style>
</head>
<body class="light-theme">
    <div class="container">
        <h1>Theme Switcher Demo</h1>
        
        <div class="theme-indicator" id="indicator">
            Current Theme: Light
        </div>
        
        <p>This page demonstrates theme switching using JavaScript and CSS classes.</p>
        <p>Watch as the theme automatically changes from light to dark after 2 seconds!</p>
        <p>The smooth transition effect is created using CSS transitions.</p>
    </div>
    
    <script>
        // Select the body element
        let body = document.body;
        let indicator = document.getElementById('indicator');
        
        // Log initial theme
        console.log('Starting with light theme');
        
        // Wait 2 seconds (2000 milliseconds), then switch themes
        setTimeout(function() {
            // Remove light theme class
            body.classList.remove('light-theme');
            
            // Add dark theme class
            body.classList.add('dark-theme');
            
            // Update the indicator text
            indicator.textContent = 'Current Theme: Dark';
            
            console.log('Switched to dark theme!');
        }, 2000);
        
        // Bonus: Switch back to light after 4 more seconds
        // Uncomment to try this:
        /*
        setTimeout(function() {
            body.classList.remove('dark-theme');
            body.classList.add('light-theme');
            indicator.textContent = 'Current Theme: Light';
            console.log('Switched back to light theme!');
        }, 6000);
        */
    </script>
</body>
</html>
```

### What's Happening:
1. Page loads with `light-theme` class on body
2. After 2 seconds, `setTimeout()` runs
3. JavaScript removes `light-theme` and adds `dark-theme`
4. CSS transition makes the change smooth

### Bonus Challenges:
- Switch back and forth multiple times
- Try different delay times
- Add more theme options (blue, green, etc.)
- Make links a different color in dark mode
- Add a button that lets users switch manually

**💡 Hint:** `setTimeout(function() { ... }, 2000)` runs code after 2000 milliseconds (2 seconds).

---

## Tips for Success

1. **Select first, modify second** - Always store elements in variables before changing them
   ```javascript
   let element = document.getElementById('myId');
   element.textContent = 'New text';
   ```

2. **Console.log your selections** - Make sure you're getting the right element
   ```javascript
   let element = document.getElementById('myId');
   console.log(element); // Should show the HTML element
   ```

3. **Check your IDs** - They must match exactly (case-sensitive!)
   ```javascript
   // HTML: <div id="myElement"></div>
   getElementById('myElement') ✅
   getElementById('myelement') ❌
   getElementById('MyElement') ❌
   ```

4. **Use camelCase for style properties**
   ```javascript
   element.style.backgroundColor = 'blue'; ✅
   element.style.background-color = 'blue'; ❌
   ```

5. **Put script at end of body** - Makes sure HTML loads before JavaScript runs

## Common Mistakes to Avoid

❌ **Including # or . in getElementById**
```javascript
getElementById('#myId')  // Wrong!
getElementById('myId')   // Correct
```

❌ **Script before HTML elements**
```html
<script>
    let element = document.getElementById('myId'); // Element doesn't exist yet!
</script>
<div id="myId"></div>
```
✅ **Script after HTML elements**
```html
<div id="myId"></div>
<script>
    let element = document.getElementById('myId'); // Now it exists!
</script>
```

❌ **Wrong syntax for styles**
```javascript
element.style.background-color = 'blue'; // Wrong - can't use hyphens
```
✅ **Correct camelCase**
```javascript
element.style.backgroundColor = 'blue'; // Correct
```

❌ **Forgetting quotes around strings**
```javascript
element.textContent = Hello; // Error!
element.textContent = 'Hello'; // Correct
```

---

## Quick Reference Guide

### Selecting Elements:
```javascript
// By ID (returns single element)
let element = document.getElementById('myId');

// By class (returns list of elements)
let elements = document.querySelectorAll('.myClass');

// First element with class
let element = document.querySelector('.myClass');
```

### Changing Content:
```javascript
// Plain text only
element.textContent = 'New text';

// HTML markup
element.innerHTML = '<strong>Bold text</strong>';
```

### Changing Styles:
```javascript
element.style.color = 'red';
element.style.fontSize = '20px';
element.style.backgroundColor = '#ffeb3b';
element.style.padding = '10px';
element.style.border = '2px solid black';
```

### Working with Classes:
```javascript
element.classList.add('myClass');
element.classList.remove('myClass');
element.classList.toggle('myClass'); // Adds if not there, removes if there
```

### Changing Attributes:
```javascript
img.src = 'newimage.jpg';
img.alt = 'New description';
link.href = 'https://example.com';
```