# **Lesson 1 Tasks: HTML Document Structure**

## **Setup Instructions**

Before starting these exercises:
1. Create a new folder called `html-lesson1` on your computer
2. Open your text editor (Notepad, Notepad++, VS Code, etc.)
3. Save each exercise as a separate `.html` file
4. Open the files in your web browser to test them

---

## **Task 1: Your First HTML Document**

**Objective:** Create a basic HTML document with proper structure.

**Instructions:**
1. Create a new file called `first-page.html`
2. Type the following code exactly:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My First Web Page</title>
</head>
<body>
    <h1>Hello World!</h1>
    <p>This is my first HTML document.</p>
</body>
</html>
```

3. Save the file and open it in your web browser
4. Verify that you see "Hello World!" as a heading and the paragraph below it

**Expected Result:** A web page with "My First Web Page" in the browser tab and "Hello World!" displayed as a large heading.

---

## **Task 2: Adding Character Encoding and Metadata**

**Objective:** Add essential metadata to your HTML document.

**Instructions:**
1. Create a new file called `about-me.html`
2. Create a complete HTML document with:
   - Proper DOCTYPE declaration
   - Character encoding set to UTF-8
   - A page title with your name (e.g., "About John Smith")
   - Keywords metadata with at least 3 relevant keywords
   - A heading with your name
   - A paragraph describing yourself

**Starter Template:**
```html
<!DOCTYPE html>
<html>
<head>
    <!-- Add character encoding here -->
    
    <!-- Add keywords metadata here -->
    
    <!-- Add title here -->
</head>
<body>
    <!-- Add heading here -->
    
    <!-- Add paragraph here -->
</body>
</html>
```

**Success Criteria:**
- Browser tab shows your name
- Page displays your name as a heading
- Page displays a paragraph about you
- Meta tags are properly formatted in the head section

---

## **Task 3: Working with Comments**

**Objective:** Practice adding comments to document your HTML.

**Instructions:**
1. Create a new file called `restaurant.html`
2. Add a comment block at the top with:
   - Your name
   - Today's date
   - The filename
   - A brief description: "Restaurant landing page"
3. Create a page about a fictional restaurant with:
   - A title
   - Character encoding
   - A main heading with the restaurant name
   - Three paragraphs describing the restaurant
   - Add a comment before each section explaining what it contains

**Example Comment Block:**
```html
<!--
    Student: Your Name
    Date: [Today's Date]
    Filename: restaurant.html
    Description: Restaurant landing page
-->
```

**Success Criteria:**
- Comment block appears at the top of your HTML
- Comments explain different sections of your code
- Comments do NOT appear in the browser window
- Page displays properly with all content visible

---

## **Task 4: Understanding White Space**

**Objective:** Learn how HTML handles white space.

**Instructions:**
1. Create a new file called `whitespace-test.html`
2. Create a basic HTML document
3. In the body, create two paragraphs:

**Paragraph 1:** Type this with all the extra spaces and line breaks:
```html
<p>This    paragraph    has    lots
   of    extra    spaces    and
   line    breaks.</p>
```

**Paragraph 2:** Type this on one line with normal spacing:
```html
<p>This paragraph has normal spacing.</p>
```

4. Save and view in your browser

**Questions to Answer:**
- How do the two paragraphs appear in the browser?
- What happened to the extra spaces and line breaks?
- Why might this behavior be useful for developers?

**Expected Result:** Both paragraphs should appear with single spaces between words, demonstrating that HTML collapses white space.

---

## **Task 5: Multiple Page Elements**

**Objective:** Practice using multiple HTML elements together.

**Instructions:**
1. Create a new file called `book-review.html`
2. Create a complete HTML document about your favorite book with:
   - A proper comment block at the top
   - Character encoding
   - Keywords metadata (book title, author, genre)
   - Page title: "[Book Name] - Review"
   - Main heading (h1): The book title
   - Subheading (h2): "by [Author Name]"
   - Another subheading (h2): "My Review"
   - At least three paragraphs with your review
   - Comments before each major section

**Success Criteria:**
- Proper document structure (DOCTYPE, html, head, body)
- All metadata correctly placed in head
- Content properly structured with headings and paragraphs
- Code is well-commented
- File opens correctly in browser

---

## **Task 6: Comprehensive Website Page**

**Objective:** Create a complete webpage using all learned concepts.

**Instructions:**

Create a file called `coffee-shop.html` for a fictional coffee shop website.

**Requirements:**

**In the HEAD:**
- Comment block with your information
- UTF-8 character encoding
- Page title: "The Daily Grind Coffee Shop"
- Keywords: "coffee, cafe, espresso, [your city]"

**In the BODY:**
- Main heading: "The Daily Grind"
- Subheading: "Artisan Coffee & Community"
- Paragraph: Brief welcome message
- Subheading: "Our Story"
- Paragraph: How the coffee shop started
- Subheading: "Our Philosophy"
- Two paragraphs: About the coffee and community focus

**Code Quality:**
- Use proper indentation (2 or 4 spaces)
- Add comments to separate major sections
- Use white space to make code readable
- Ensure all tags are properly closed

**Bonus Challenges:**
- Add a copyright symbol in a paragraph using `&copy;`
- Add a trademark symbol using `&trade;`
- Add an en dash using `&ndash;`

---

## **Task 7: Error Detection**

**Objective:** Debug a broken HTML document.

**Instructions:**

The following HTML has **5 errors**. Copy it into a file called `debug.html` and fix all the errors:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8"
    <title>Debugging Practice
    <meta name="keywords" content="HTML, practice" />
<body>
    <h1>Welcome to Debugging</h1>
    <p>This document has several errors.</p>
    <p>Can you find and fix them all?
    <h2>Good luck!</h2>
</body>
</html>
```

**Questions:**
1. What errors did you find?
2. How did you identify them?
3. What happened when you tried to view the broken file?

---

## **Self-Assessment Checklist**

After completing these tasks, you should be able to:

- [ ] Create a properly structured HTML5 document
- [ ] Add DOCTYPE declaration correctly
- [ ] Use opening and closing tags properly
- [ ] Add metadata to the document head
- [ ] Set character encoding to UTF-8
- [ ] Create descriptive page titles
- [ ] Add comments to document your code
- [ ] Understand how HTML handles white space
- [ ] Use proper indentation and formatting
- [ ] Debug simple HTML errors

---

## **Extension Activities**

Ready for more practice? Try these:

1. **Personal Portfolio:** Create an `index.html` file as a simple personal portfolio page with sections for About, Skills, and Interests

2. **Recipe Page:** Create a recipe page with proper structure, including ingredients and instructions

3. **Local Business:** Create a page for a local business with information about services, hours, and contact info

4. **Code Review:** Exchange HTML files with a classmate and review each other's code, checking for proper structure and commenting

---

## **Common Mistakes to Avoid**

- Forgetting to close tags
- Misspelling element names
- Missing the DOCTYPE declaration
- Putting body content in the head section
- Forgetting quotation marks around attribute values
- Not using UTF-8 character encoding
- Mixing up opening and closing tag syntax

---

## **Next Steps**

Once you've completed these exercises, you're ready to move on to Lesson 2, where we'll explore:
- Sectioning elements (header, nav, section, footer)
- Grouping elements (div, p, lists)
- Text-level elements
- Working with inline images