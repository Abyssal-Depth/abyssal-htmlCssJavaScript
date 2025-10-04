# **Lesson 2 Tasks: Sectioning and Grouping Elements**

## **Setup Instructions**

Before starting these exercises:
1. Create a new folder called `html-lesson2` on your computer
2. Open your text editor
3. Save each exercise as a separate `.html` file
4. Open the files in your web browser to test them

---

## **Task 1: Basic Semantic Structure**

**Objective:** Create a page using HTML5 semantic elements.

**Instructions:**
1. Create a new file called `basic-structure.html`
2. Build a complete HTML document with:
   - A `<header>` containing an `<h1>` with "My Website"
   - A `<nav>` section (leave empty for now)
   - A `<main>` section with an `<h2>` saying "Welcome"
   - A `<footer>` with a copyright notice

**Starter Code:**
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>Basic Structure</title>
</head>
<body>
    <!-- Add header here -->
    
    <!-- Add nav here -->
    
    <!-- Add main here -->
    
    <!-- Add footer here -->
</body>
</html>
```

**Success Criteria:**
- Document uses proper semantic HTML5 elements
- Each section contains appropriate content
- Page displays correctly in browser

---

## **Task 2: Creating Navigation**

**Objective:** Build a navigation menu using lists and links.

**Instructions:**
1. Create a file called `navigation.html`
2. Create a complete page with:
   - A header with your site name
   - A `<nav>` element containing an unordered list with 5 navigation links:
     - Home (links to `index.html`)
     - About (links to `about.html`)
     - Services (links to `services.html`)
     - Portfolio (links to `portfolio.html`)
     - Contact (links to `contact.html`)
   - A main section with some welcome text
   - A footer

**Navigation Structure:**
```html
<nav>
    <ul>
        <li><!-- First link here --></li>
        <!-- More list items here -->
    </ul>
</nav>
```

**Success Criteria:**
- Navigation uses semantic `<nav>` element
- Links are contained in an unordered list
- Each link has proper href attribute
- Links are clickable (even if destination doesn't exist yet)

---

## **Task 3: Working with Sections and Articles**

**Objective:** Understand the difference between `<section>` and `<article>`.

**Instructions:**
1. Create a file called `blog-page.html`
2. Create a blog homepage with:
   - Header with site title "My Blog"
   - Navigation with links to Home, Archives, About
   - Main content area containing:
     - A `<section>` with heading "Recent Posts"
     - Inside that section, create 3 `<article>` elements, each containing:
       - An `<h3>` with a post title
       - A paragraph with post date and author
       - A paragraph with post excerpt
   - Footer with copyright

**Example Article Structure:**
```html
<article>
    <h3>My First Blog Post</h3>
    <p>Posted on October 4, 2025 by Your Name</p>
    <p>This is an excerpt from my first blog post...</p>
</article>
```

**Success Criteria:**
- Section contains multiple articles
- Each article is self-contained
- Proper heading hierarchy (h1 for page, h2 for section, h3 for articles)
- All semantic elements used correctly

---

## **Task 4: Using Aside Elements**

**Objective:** Add sidebar content with the `<aside>` element.

**Instructions:**
1. Create a file called `article-with-sidebar.html`
2. Create a page about a topic of your choice with:
   - Header and navigation
   - Main section with:
     - An `<article>` with 3-4 paragraphs about your topic
     - An `<aside>` containing:
       - A heading "Related Information"
       - An unordered list with 3-4 related links or facts
   - Footer

**Layout Concept:**
```html
<main>
    <article>
        <h2>Main Article Title</h2>
        <p>Main content...</p>
    </article>
    
    <aside>
        <h3>Did You Know?</h3>
        <!-- Related content here -->
    </aside>
</main>
```

**Success Criteria:**
- Aside content is related but supplementary
- Aside could be removed without losing main message
- Proper semantic structure throughout

---

## **Task 5: List Practice**

**Objective:** Create and use all three types of lists.

**Instructions:**
1. Create a file called `lists-practice.html`
2. Create a recipe page with:
   - Header with recipe name
   - Main section containing three subsections:

**Section 1 - Ingredients:** Use an unordered list
```html
<section>
    <h2>Ingredients</h2>
    <ul>
        <li>2 cups flour</li>
        <!-- Add more ingredients -->
    </ul>
</section>
```

**Section 2 - Instructions:** Use an ordered list
```html
<section>
    <h2>Instructions</h2>
    <ol>
        <li>Preheat oven to 350°F</li>
        <!-- Add more steps -->
    </ol>
</section>
```

**Section 3 - Cooking Terms:** Use a description list with 3 terms
```html
<section>
    <h2>Cooking Terms</h2>
    <dl>
        <dt>Sauté</dt>
        <dd>To cook quickly in a small amount of fat</dd>
        <!-- Add more terms -->
    </dl>
</section>
```

**Success Criteria:**
- Each list type used appropriately
- At least 5 items in ingredient list
- At least 5 steps in instructions
- At least 3 term-definition pairs

---

## **Task 6: Nested Lists**

**Objective:** Create multi-level list structures.

**Instructions:**
1. Create a file called `course-outline.html`
2. Create a course outline page with:
   - Header with "Web Development Course"
   - Main section with heading "Course Outline"
   - An ordered list representing modules with nested unordered lists for topics:

```html
<ol>
    <li>Introduction to HTML
        <ul>
            <li>HTML Basics</li>
            <li>Document Structure</li>
            <li>Semantic Elements</li>
        </ul>
    </li>
    <li>CSS Fundamentals
        <ul>
            <li>Selectors</li>
            <li>Box Model</li>
            <li>Layout</li>
        </ul>
    </li>
    <!-- Add at least 2 more modules -->
</ol>
```

**Requirements:**
- At least 4 main modules (ordered list items)
- Each module has at least 3 subtopics (nested unordered list)
- Proper indentation to show structure

**Success Criteria:**
- Nested lists display correctly
- Numbering and bullets appear appropriately
- Structure is clear and logical

---

## **Task 7: Complete Restaurant Website Page**

**Objective:** Create a comprehensive page using all learned elements.

**Instructions:**

Create `restaurant-about.html` for a restaurant with the following structure:

**Header Section:**
- Restaurant logo (use placeholder text "LOGO" in an `<img>` tag for now)
- Restaurant name in `<h1>`
- Tagline in a `<p>`

**Navigation:**
- Links to: Home, About, Menu, Locations, Contact

**Main Content:**
```html
<main>
    <section>
        <h2>Our Story</h2>
        <!-- 2 paragraphs about restaurant history -->
    </section>
    
    <section>
        <h2>What We Offer</h2>
        <!-- Unordered list with 4+ items -->
    </section>
    
    <section>
        <h2>Customer Favorites</h2>
        <!-- Ordered list with top 5 dishes -->
    </section>
    
    <aside>
        <h3>Hours of Operation</h3>
        <!-- Description list with days and hours -->
    </aside>
    
    <section>
        <h2>What People Say</h2>
        <article>
            <!-- Customer review 1 with blockquote -->
        </article>
        <article>
            <!-- Customer review 2 with blockquote -->
        </article>
    </section>
</main>
```

**Footer:**
- Copyright information
- Address
- Phone number

**Success Criteria:**
- All semantic elements used appropriately
- Multiple list types included
- Proper heading hierarchy
- Reviews use `<blockquote>`
- Code is well-organized and indented

---

## **Task 8: Portfolio Homepage**

**Objective:** Build a personal portfolio structure.

**Instructions:**

Create `portfolio.html` with these sections:

1. **Header:** Your name and professional title
2. **Navigation:** Home, About, Projects, Skills, Contact
3. **Main Content:**
   - **Section 1:** "About Me" with 2 paragraphs
   - **Section 2:** "Projects" with 3 articles (each representing a project):
     - Project name
     - Description
     - Technologies used (unordered list)
   - **Section 3:** "Skills" with categories:
     - Programming Languages (unordered list)
     - Tools & Technologies (unordered list)
   - **Aside:** "Currently Learning" with 3-4 items
4. **Footer:** Contact information and social links

**Bonus Challenge:**
- Use `<figure>` and `<figcaption>` for project images (use placeholder text for images)
- Add `<hr>` between major sections
- Use `<pre>` to display a code snippet in one project

**Success Criteria:**
- Complete semantic structure
- Multiple sections and articles
- Various list types
- Aside content is supplementary
- Professional appearance when viewed

---

## **Task 9: News Website Structure**

**Objective:** Create a news-style layout with multiple content areas.

**Instructions:**

Create `news-homepage.html` with:

```html
<body>
    <header>
        <!-- Site name and date -->
        <nav><!-- Navigation links --></nav>
    </header>
    
    <main>
        <section>
            <h2>Top Stories</h2>
            <article>
                <h3>Main Headline</h3>
                <p>Article preview...</p>
            </article>
            <!-- 2 more featured articles -->
        </section>
        
        <section>
            <h2>Categories</h2>
            <!-- Nested list showing news categories and subcategories:
                 - World News
                   - Politics
                   - Economics
                 - Technology
                   - Software
                   - Hardware
                 - Sports
                   - Football
                   - Basketball
            -->
        </section>
        
        <aside>
            <h3>Quick Links</h3>
            <!-- List of useful links -->
            
            <h3>Weather</h3>
            <dl>
                <dt>Today</dt>
                <dd>Sunny, 72°F</dd>
                <!-- More days -->
            </dl>
        </aside>
    </main>
    
    <footer>
        <!-- Copyright and links -->
    </footer>
</body>
```

**Success Criteria:**
- Clear visual hierarchy
- Articles are self-contained
- Nested category list
- Aside with supplementary information
- Description list for structured data

---

## **Task 10: Debugging Exercise**

**Objective:** Find and fix semantic structure errors.

**Instructions:**

Copy this code into `debug-structure.html` and fix all **8 errors**:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>Debug Practice</title>
</head>
<body>
    <heading>
        <h1>My Website</h1>
    </heading>
    
    <navigation>
        <ol>
            <li><a href="index.html">Home</a>
            <li><a href="about.html">About</a></li>
        </ol>
    </navigation>
    
    <main>
        <section>
            <h2>Welcome</h2>
            <p>This is the main content.
        </section>
        
        <article>
            <h2>Blog Post</h2>
            <p>Post content here...</p>
        </main>
        
        <sidebar>
            <h3>Related Links</h3>
            <ul>
                <li>Link 1</li>
                <li>Link 2</li>
            </ul>
        </sidebar>
    </article>
    
    <footer>
        <p>Copyright 2025</p>
    </footer>
</body>
</html>
```

**Questions to Answer:**
1. List all the errors you found
2. What are the correct element names?
3. Which elements were improperly nested?
4. How did you identify the errors?

---

## **Task 11: Creating Figure Elements**

**Objective:** Use figures with captions.

**Instructions:**

Create `gallery.html` with:
- Header and navigation
- Main section with heading "Photo Gallery"
- Three `<figure>` elements, each containing:
  - An `<img>` tag (use placeholder: `src="image1.jpg"`)
  - A `<figcaption>` describing the image

**Example:**
```html
<figure>
    <img src="sunset.jpg" alt="Beautiful sunset over ocean" />
    <figcaption>Sunset at Malibu Beach, California</figcaption>
</figure>
```

**Success Criteria:**
- Each figure groups image with caption
- Alt text describes each image
- Captions are descriptive
- Proper semantic structure

---

## **Task 12: Comprehensive Website**

**Objective:** Build a complete multi-section website page.

**Instructions:**

Create `complete-site.html` for a fictional company with ALL of the following:

**Required Elements:**
- [ ] Header with logo and company name
- [ ] Navigation with at least 5 links
- [ ] Main element containing:
  - [ ] Hero section with h1 and introductory paragraph
  - [ ] Services section with unordered list
  - [ ] Process section with ordered list
  - [ ] Testimonials section with 2 articles using blockquotes
  - [ ] FAQ section with description list (3+ items)
- [ ] Aside with:
  - [ ] Contact information
  - [ ] Office hours (description list)
- [ ] Footer with:
  - [ ] Copyright
  - [ ] Address
  - [ ] Social media links (list)

**Quality Requirements:**
- Proper heading hierarchy (only one h1)
- Well-commented code
- Consistent indentation
- All tags properly closed
- Semantic elements used appropriately

---

## **Self-Assessment Checklist**

After completing these tasks, you should be able to:

- [ ] Use header, nav, main, section, article, aside, and footer appropriately
- [ ] Understand the difference between section and article
- [ ] Create navigation with lists and links
- [ ] Build unordered, ordered, and description lists
- [ ] Create nested lists
- [ ] Use proper heading hierarchy
- [ ] Structure a complete semantic HTML5 page
- [ ] Use figure and figcaption elements
- [ ] Apply aside elements for supplementary content
- [ ] Debug semantic structure errors

---

## **Extension Activities**

Ready for more challenges?

1. **Multi-Page Site:** Create 3 connected pages (home, about, contact) with consistent navigation

2. **Blog Template:** Create a blog post template with comments section (each comment is an article)

3. **Product Catalog:** Build a product page with categories (nested lists) and product cards (articles)

4. **Event Schedule:** Create an event page with schedule (description list), speakers (articles), and venue info (aside)

5. **Documentation Page:** Build a technical documentation page with sections, code examples in `<pre>`, and a table of contents

---

## **Common Mistakes to Avoid**

- Using `<div>` when a semantic element would be better
- Using multiple `<main>` elements (only one per page)
- Skipping heading levels (h1 → h3)
- Putting navigation links directly in `<nav>` without a list
- Using `<article>` for non-independent content
- Forgetting to close list items
- Improper nesting of lists
- Using `<section>` without a heading

---

## **Best Practices Review**

**Semantic HTML Checklist:**
- ✓ Use semantic elements over `<div>` when possible
- ✓ Only one `<h1>` per page
- ✓ Only one `<main>` per page
- ✓ Every `<section>` should have a heading
- ✓ `<article>` content should be self-contained
- ✓ `<aside>` content should be supplementary
- ✓ Navigation should use `<nav>` with a list

---

## **Next Steps**

Once you've completed these exercises, you're ready for Lesson 3, where we'll explore:
- Text-level elements (bold, italic, emphasis)
- Inline images with proper attributes
- Character entities and special symbols
- Creating hypertext links
- Linking to email addresses and phone numbers