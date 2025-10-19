# Lesson B1 Tasks: Bootstrap Components Practice

---

## Task 1: GUIDED EXAMPLE - Bootstrap Button Gallery

**Follow these steps to create a page showcasing different Bootstrap buttons.**

### Step 1: Create the HTML
Create a file called `button-gallery.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Button Gallery</title>
    
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    
    <style>
        body {
            padding: 30px;
        }
        .section {
            margin-bottom: 40px;
        }
    </style>
</head>
<body>
    <h1 class="text-center mb-5">My Button Gallery</h1>
    
    <div class="section">
        <h2>Colored Buttons</h2>
        <button class="btn btn-primary">Primary</button>
        <button class="btn btn-secondary">Secondary</button>
        <button class="btn btn-success">Success</button>
        <button class="btn btn-danger">Danger</button>
        <button class="btn btn-warning">Warning</button>
        <button class="btn btn-info">Info</button>
    </div>
    
    <div class="section">
        <h2>Button Sizes</h2>
        <button class="btn btn-primary btn-lg">Large</button>
        <button class="btn btn-primary">Normal</button>
        <button class="btn btn-primary btn-sm">Small</button>
    </div>
    
    <div class="section">
        <h2>Outline Buttons</h2>
        <button class="btn btn-outline-primary">Primary</button>
        <button class="btn btn-outline-success">Success</button>
        <button class="btn btn-outline-danger">Danger</button>
    </div>
</body>
</html>
```

### Step 2: Test It
1. Open the file in your browser
2. You should see three sections with different styled buttons
3. Hover over the buttons to see the hover effects!

### Step 3: Experiment
Now try adding:
- A new section called "My Favorite Buttons"
- At least 3 buttons in different colors
- Try mixing sizes and outline styles

**Checkpoint:** Your page should have 4 sections of buttons total.

---

## Task 2: Alert Message Page

**Goal:** Practice creating different types of alerts.

### Instructions:
1. Create a file called `alerts.html`
2. Add Bootstrap to your page
3. Create these alerts:
   - A success alert saying "Account created successfully!"
   - A danger alert saying "Error: Invalid password"
   - A warning alert saying "Your trial expires in 3 days"
   - An info alert saying "Did you know? Bootstrap was created by Twitter!"

4. Add proper spacing between alerts using Bootstrap margin classes

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alert Messages</title>
    
    <!-- Add Bootstrap CSS here -->
    
</head>
<body>
    <div class="container mt-5">
        <h1 class="text-center mb-4">System Messages</h1>
        
        <!-- Success Alert -->
        <div class="alert alert-success">
            Account created successfully!
        </div>
        
        <!-- Add the other 3 alerts here -->
        
    </div>
</body>
</html>
```

### Expected Output:
- Green box with success message
- Red box with error message
- Yellow box with warning message
- Light blue box with info message
- All alerts should have space between them

**💡 Hint:** Use `mb-3` class on each alert to add margin-bottom spacing.

---

## Task 3: User Profile Card with Badges

**Goal:** Create a simple user profile using badges and spacing utilities.

### Instructions:
1. Create a file called `profile-card.html`
2. Create a profile that displays:
   - User's name as an h1
   - An "Active" status badge next to the name (use green/success)
   - A list of skills as pill badges (at least 4 skills)
   - A bio paragraph with proper spacing

3. Use Bootstrap spacing utilities to make it look organized

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Profile</title>
    
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container mt-5">
        <!-- Name with status badge -->
        <h1>
            Sarah Johnson 
            <span class="badge bg-success">Active</span>
        </h1>
        
        <!-- Bio -->
        <p class="mt-3">
            Web developer and designer passionate about creating beautiful, 
            user-friendly websites.
        </p>
        
        <!-- Skills section -->
        <h3 class="mt-4">Skills</h3>
        <div class="mt-2">
            <span class="badge rounded-pill bg-secondary">HTML</span>
            <!-- Add more skill badges here -->
            
        </div>
    </div>
</body>
</html>
```

### Requirements:
- ✅ Name with a status badge
- ✅ Bio paragraph
- ✅ At least 4 skill badges (use rounded-pill style)
- ✅ Proper spacing using Bootstrap classes (mt, mb, etc.)

**💡 Challenge:** Add more badges showing:
- Number of projects completed
- Years of experience
- Location

---

## Task 4: Text Styling Practice

**Goal:** Practice Bootstrap text utility classes.

### Instructions:
1. Create a file called `text-styles.html`
2. Create sections demonstrating:
   - Text colors (at least 4 different colors)
   - Text alignment (left, center, right)
   - Font weights (bold, normal, light)
   - Text transforms (uppercase, lowercase, capitalize)

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Text Styling</title>
    
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container mt-5">
        <h1 class="text-center mb-5">Bootstrap Text Utilities</h1>
        
        <!-- Text Colors Section -->
        <div class="mb-5">
            <h2>Text Colors</h2>
            <p class="text-primary">This is primary blue text</p>
            <p class="text-success">This is success green text</p>
            <!-- Add more colored text here -->
        </div>
        
        <!-- Text Alignment Section -->
        <div class="mb-5">
            <h2>Text Alignment</h2>
            <p class="text-start">This text is left aligned</p>
            <!-- Add center and right aligned text here -->
        </div>
        
        <!-- Font Weight Section -->
        <div class="mb-5">
            <h2>Font Weights</h2>
            <p class="fw-bold">This text is bold</p>
            <!-- Add normal and light weight text here -->
        </div>
        
        <!-- Text Transform Section -->
        <div class="mb-5">
            <h2>Text Transforms</h2>
            <p class="text-uppercase">this should be uppercase</p>
            <!-- Add lowercase and capitalize examples here -->
        </div>
    </div>
</body>
</html>
```

### Success Criteria:
- ✅ At least 4 different text colors
- ✅ Examples of left, center, and right alignment
- ✅ Examples of bold, normal, and light font weights
- ✅ Examples of uppercase, lowercase, and capitalize
- ✅ Proper section spacing using mb-5

---

## Task 5: Notification Dashboard

**Goal:** Combine multiple Bootstrap components in one page.

### Instructions:
1. Create a file called `dashboard.html`
2. Build a simple notification dashboard that includes:
   - A title with proper text alignment
   - At least 3 different alert types showing different notifications
   - A section showing notification counts using badges
   - Action buttons for each notification

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Notification Dashboard</title>
    
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container mt-5">
        <h1 class="text-center mb-4">Notification Dashboard</h1>
        
        <!-- Summary Section -->
        <div class="mb-4">
            <h3>Summary</h3>
            <p>
                Messages <span class="badge bg-primary">5</span>
                Alerts <span class="badge bg-warning">2</span>
                Updates <span class="badge bg-info">8</span>
            </p>
        </div>
        
        <!-- Notification 1 -->
        <div class="alert alert-success mb-3">
            <h4 class="alert-heading">New Message Received</h4>
            <p>You have a new message from Alex Johnson.</p>
            <button class="btn btn-success btn-sm">Read Message</button>
        </div>
        
        <!-- Add 2 more notifications here -->
        
    </div>
</body>
</html>
```

### Requirements:
- ✅ Title centered at the top
- ✅ Summary section with at least 3 badges showing counts
- ✅ At least 3 different notification alerts (different colors)
- ✅ Each notification should have a heading and a button
- ✅ Proper spacing throughout

**💡 Bonus:** 
- Add a "Clear All" button at the bottom using `btn-outline-danger`
- Add timestamps to notifications using the `text-muted` class

---

## Task 6: Debug the Bootstrap Code

**Goal:** Find and fix Bootstrap class errors.

### Instructions:
1. Create a file called `debug-bootstrap.html`
2. Copy this code (it has errors!):

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Debug Practice</title>
    
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container mt-5">
        <h1 class="text-centre">Welcome!</h1>
        
        <div class="alert success">
            Success! Your profile was updated.
        </div>
        
        <button class="btn primary">Click Me</button>
        
        <p class="text top">
            Status: <span class="badge bg-succes">Active</span>
        </p>
        
        <div class="mb3">
            <button class="btn btn-outline">Outline Button</button>
        </div>
    </div>
</body>
</html>
```

3. Find and fix ALL errors
4. Code should display properly with correct Bootstrap styling

### Errors to Find (6 total):
- ❌ Text alignment class misspelled
- ❌ Alert class missing prefix
- ❌ Button class missing prefix
- ❌ Invalid text utility class
- ❌ Badge color class misspelled
- ❌ Spacing class missing hyphen
- ❌ Outline button class incomplete

**Debugging Tips:**
1. Bootstrap classes must be spelled exactly right
2. Most Bootstrap components need a prefix (like `btn-` or `alert-`)
3. Spacing classes need hyphens: `mb-3` not `mb3`
4. Check the Bootstrap lesson notes for correct class names

**Success:** Page should display with:
- Centered title
- Green success alert
- Blue primary button
- Active badge (green)
- Gray outline button
- All with proper spacing

---

## Challenge Task: Welcome Page

**Goal:** Create a complete welcome page using everything you've learned.

### Instructions:
1. Create `welcome-page.html`
2. Your page must include:
   - A centered title with custom styling
   - A welcome alert with a heading
   - At least 3 feature sections, each with:
     - A heading
     - A description paragraph
     - A call-to-action button
   - A status section with multiple badges
   - Proper spacing throughout

### Starter Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome Page</title>
    
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container mt-5">
        <!-- Main Title -->
        <h1 class="text-center mb-4 text-primary">Welcome to MyApp!</h1>
        
        <!-- Welcome Alert -->
        <div class="alert alert-info mb-5">
            <h4 class="alert-heading">Getting Started</h4>
            <p>Thanks for joining! Here's what you can do with MyApp.</p>
        </div>
        
        <!-- Feature 1 -->
        <div class="mb-4">
            <h3>Feature 1: Easy to Use</h3>
            <p>Our app is designed to be simple and intuitive.</p>
            <button class="btn btn-primary">Learn More</button>
        </div>
        
        <!-- Add Feature 2 and Feature 3 here -->
        
        <!-- Status Section -->
        <div class="mt-5 text-center">
            <h4>Platform Status</h4>
            <p class="mt-3">
                <span class="badge rounded-pill bg-success">All Systems Operational</span>
                <span class="badge rounded-pill bg-info">99.9% Uptime</span>
                <span class="badge rounded-pill bg-secondary">Last Updated: Today</span>
            </p>
        </div>
    </div>
</body>
</html>
```

### Requirements:
- ✅ At least 3 feature sections with buttons
- ✅ At least 1 alert with a heading
- ✅ At least 5 badges total
- ✅ Use at least 4 different button colors/styles
- ✅ Use proper spacing classes (mt, mb, etc.) throughout
- ✅ Use at least 3 text utility classes

### Bonus Challenges:
- ✨ Add a footer section with contact information
- ✨ Use different button sizes for different importance levels
- ✨ Add more alerts for tips or warnings
- ✨ Use text-muted class for less important information
- ✨ Add section dividers or extra styling

### Grading Yourself:
- ✅ Page looks organized and professional
- ✅ All Bootstrap classes are spelled correctly
- ✅ Good use of spacing (not too cramped, not too spread out)
- ✅ Buttons and alerts are appropriate for their purpose
- ✅ Page is easy to read and navigate

---

## Tips for Success

1. **Double-check spelling** - Bootstrap classes must be exact
2. **Use the docs** - When in doubt, check the Bootstrap lesson notes
3. **Test frequently** - Save and refresh after each change
4. **Use spacing** - Don't forget margin and padding classes
5. **Stay organized** - Use comments to label sections in your HTML
6. **Be consistent** - Use similar spacing throughout the page

---

## Common Mistakes to Avoid

❌ `<button class="btn primary">` - Missing the hyphen  
✅ `<button class="btn btn-primary">`

❌ `<div class="alert success">` - Missing the prefix  
✅ `<div class="alert alert-success">`

❌ `<div class="mb3">` - Missing the hyphen  
✅ `<div class="mb-3">`

❌ `<span class="badge primary">` - Wrong class name  
✅ `<span class="badge bg-primary">`

❌ Forgetting to add Bootstrap CSS link  
✅ Always include the Bootstrap CDN link in `<head>`

---

## Answer Key for Task 6

Here's the corrected code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Debug Practice</title>
    
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container mt-5">
        <h1 class="text-center">Welcome!</h1>
        
        <div class="alert alert-success">
            Success! Your profile was updated.
        </div>
        
        <button class="btn btn-primary">Click Me</button>
        
        <p class="mt-3">
            Status: <span class="badge bg-success">Active</span>
        </p>
        
        <div class="mb-3">
            <button class="btn btn-outline-primary">Outline Button</button>
        </div>
    </div>
</body>
</html>
```

**Corrections Made:**
1. `text-centre` → `text-center`
2. `alert success` → `alert alert-success`
3. `btn primary` → `btn btn-primary`
4. `text top` → `mt-3` (margin-top)
5. `bg-succes` → `bg-success`
6. `mb3` → `mb-3`
7. `btn-outline` → `btn btn-outline-primary`