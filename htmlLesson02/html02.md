# **Lesson 2: Sectioning and Grouping Elements**

## **Learning Objectives**
- Understand HTML5 semantic sectioning elements
- Mark up page structure with header, nav, section, article, aside, and footer
- Use grouping elements to organize content
- Create different types of lists
- Apply proper document hierarchy

---

## **Sectioning Elements (Semantic Elements)**

HTML5 introduced **semantic elements** that describe the meaning and structure of content, not just its appearance.

### **Why Use Semantic Elements?**

- **Accessibility:** Screen readers can navigate by sections
- **SEO:** Search engines better understand content structure
- **Maintainability:** Code is easier to read and update
- **Standards:** Modern best practice for web development

---

## **Main Sectioning Elements**

### **The `<header>` Element**

Contains introductory content for a page or section.

```html
<header>
    <img src="logo.png" alt="Company Logo" />
    <h1>Curbside Thai</h1>
    <p>Authentic Gourmet Thai Food</p>
</header>
```

**Typical header content:**
- Logo
- Site title
- Tagline or slogan
- Top-level navigation

---

### **The `<nav>` Element**

Contains navigation links (major navigation sections only).

```html
<nav>
    <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="menu.html">Menu</a></li>
        <li><a href="locations.html">Locations</a></li>
        <li><a href="reviews.html">Reviews</a></li>
        <li><a href="contact.html">Contact</a></li>
    </ul>
</nav>
```

**Best Practices:**
- Use for main site navigation
- Not needed for every group of links
- Can have multiple nav elements on a page

---

### **The `<section>` Element**

Marks content that shares a common theme or purpose.

```html
<section>
    <h2>Our Story</h2>
    <p>Curbside Thai was founded in 2010...</p>
    <p>We believe in authentic ingredients...</p>
</section>

<section>
    <h2>Our Menu</h2>
    <p>We offer a wide variety of dishes...</p>
</section>
```

**When to use:**
- Thematic groupings of content
- Each section typically has a heading
- Multiple sections make up a page

---

### **The `<article>` Element**

Marks self-contained, independently distributable content.

```html
<article>
    <h2>Customer Review: Amazing Pad Thai!</h2>
    <p>Posted by: Sarah Johnson on October 1, 2025</p>
    <p>I've been coming to Curbside Thai for years...</p>
</article>
```

**Good uses for `<article>`:**
- Blog posts
- News articles
- Customer reviews
- Forum posts
- Product listings

**Test:** Could this content stand alone if syndicated elsewhere?

---

### **The `<aside>` Element**

Contains content related to the main content but separate from it.

```html
<article>
    <h2>Thai Cuisine History</h2>
    <p>Thai cuisine is known for its balance of flavors...</p>
    
    <aside>
        <h3>Did You Know?</h3>
        <p>Thai food is influenced by Chinese, Indian, and Malaysian cuisines.</p>
    </aside>
</article>
```

**Common uses:**
- Sidebars
- Pull quotes
- Related links
- Tangential information
- Advertisements

---

### **The `<footer>` Element**

Contains closing content for a page or section.

```html
<footer>
    <p>Curbside Thai &copy; 2025</p>
    <p>411 Belde Drive, Charlotte NC 28201</p>
    <p>Phone: 704-555-1151</p>
</footer>
```

**Typical footer content:**
- Copyright information
- Contact details
- Social media links
- Secondary navigation
- Legal links (privacy policy, terms)

---

### **Headings: `<h1>` through `<h6>`**

Create a document hierarchy with six levels of headings.

```html
<h1>Main Page Title</h1>

<section>
    <h2>Major Section</h2>
    <p>Content...</p>
    
    <h3>Subsection</h3>
    <p>More content...</p>
    
    <h4>Sub-subsection</h4>
    <p>Even more content...</p>
</section>
```

**Best Practices:**
- Use only ONE `<h1>` per page (the main title)
- Don't skip heading levels (h2 → h4)
- Use headings for structure, not styling

---

## **Complete Semantic Structure Example**

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>Curbside Thai - Home</title>
</head>
<body>
    <header>
        <img src="logo.png" alt="Curbside Thai Logo" />
        <h1>Curbside Thai</h1>
    </header>
    
    <nav>
        <ul>
            <li><a href="index.html">Home</a></li>
            <li><a href="menu.html">Menu</a></li>
            <li><a href="contact.html">Contact</a></li>
        </ul>
    </nav>
    
    <main>
        <section>
            <h2>Welcome</h2>
            <p>Experience authentic Thai cuisine...</p>
        </section>
        
        <section>
            <h2>Featured Dishes</h2>
            <article>
                <h3>Pad Thai</h3>
                <p>Our signature dish...</p>
            </article>
        </section>
        
        <aside>
            <h3>Special Offer</h3>
            <p>10% off lunch specials!</p>
        </aside>
    </main>
    
    <footer>
        <p>&copy; 2025 Curbside Thai</p>
    </footer>
</body>
</html>
```

---

## **HTML5 vs HTML4 Structure**

### **HTML4 Approach (Older)**

```html
<div id="header">
    <div id="nav">...</div>
</div>
<div id="section">
    <div id="article">...</div>
</div>
<div id="aside">...</div>
<div id="footer">...</div>
```

### **HTML5 Approach (Current)**

```html
<header>
    <nav>...</nav>
</header>
<section>
    <article>...</article>
</section>
<aside>...</aside>
<footer>...</footer>
```

**HTML5 semantic elements make structure clearer and more meaningful.**

---

## **Grouping Elements**

Grouping elements organize content within sections.

### **The `<div>` Element**

A generic container with no semantic meaning.

```html
<div class="card">
    <h3>Menu Item</h3>
    <p>Description...</p>
</div>
```

**When to use:**
- For styling purposes (with CSS)
- When no semantic element fits
- To group elements for layout

---

### **The `<p>` Element**

Marks paragraphs of text.

```html
<p>This is a paragraph of text.</p>
<p>This is another paragraph.</p>
```

**Note:** Browsers automatically add spacing between paragraphs.

---

### **The `<main>` Element**

Contains the main content of the page (use only once per page).

```html
<body>
    <header>...</header>
    <nav>...</nav>
    
    <main>
        <!-- Primary content here -->
        <h2>About Us</h2>
        <p>Main content...</p>
    </main>
    
    <footer>...</footer>
</body>
```

**Rules:**
- Only ONE `<main>` per page
- Contains the primary content
- Should not be inside header, footer, nav, aside

---

### **The `<hr>` Element**

Creates a thematic break (often rendered as a horizontal line).

```html
<section>
    <h2>Section One</h2>
    <p>Content...</p>
</section>

<hr />

<section>
    <h2>Section Two</h2>
    <p>Different content...</p>
</section>
```

---

### **The `<blockquote>` Element**

Marks content quoted from another source.

```html
<blockquote>
    <p>"The food was absolutely amazing! Best Thai in Charlotte."</p>
    <p>- Food Magazine Review</p>
</blockquote>
```

**Note:** Often displayed with indentation.

---

### **The `<pre>` Element**

Preserves white space and formatting (displays in monospace font).

```html
<pre>
    Curbside Thai
    411 Belde Drive
    Charlotte, NC 28201
</pre>
```

**Use cases:**
- Code samples
- ASCII art
- Preformatted text
- Poetry with specific line breaks

---

## **Working with Lists**

### **Unordered Lists (`<ul>`)**

For items with no specific order.

```html
<h3>Menu Categories</h3>
<ul>
    <li>Appetizers</li>
    <li>Soups</li>
    <li>Curries</li>
    <li>Noodles</li>
    <li>Desserts</li>
</ul>
```

**Default:** Displays with bullet points.

---

### **Ordered Lists (`<ol>`)**

For items in a specific sequence.

```html
<h3>How to Order</h3>
<ol>
    <li>Browse the menu</li>
    <li>Add items to cart</li>
    <li>Review your order</li>
    <li>Enter delivery address</li>
    <li>Complete payment</li>
</ol>
```

**Default:** Displays with numbers (1, 2, 3...).

---

### **Nested Lists**

Lists can contain other lists.

```html
<h3>Our Locations</h3>
<ul>
    <li>Charlotte
        <ul>
            <li>Downtown Location</li>
            <li>University Area</li>
        </ul>
    </li>
    <li>Raleigh
        <ul>
            <li>Main Street</li>
        </ul>
    </li>
</ul>
```

---

### **Description Lists (`<dl>`)**

For term-definition pairs.

```html
<h3>Thai Cooking Terms</h3>
<dl>
    <dt>Pad</dt>
    <dd>Stir-fried dish</dd>
    
    <dt>Tom</dt>
    <dd>Boiled or soup dish</dd>
    
    <dt>Gaeng</dt>
    <dd>Curry dish</dd>
</dl>
```

**Structure:**
- `<dl>` - Description list container
- `<dt>` - Description term
- `<dd>` - Description definition

---

### **Navigation Lists**

Combine nav element with unordered list.

```html
<nav>
    <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="menu.html">Menu</a></li>
        <li><a href="contact.html">Contact</a></li>
    </ul>
</nav>
```

**This is the standard pattern for website navigation.**

---

## **The `<figure>` and `<figcaption>` Elements**

Group media content with its caption.

```html
<figure>
    <img src="pad-thai.jpg" alt="Plate of Pad Thai" />
    <figcaption>Our signature Pad Thai dish with shrimp</figcaption>
</figure>
```

**Can be used for:**
- Images with captions
- Code listings
- Diagrams
- Charts
- Videos

---

## **Complete Page Example**

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>About Curbside Thai</title>
</head>
<body>
    <header>
        <h1>Curbside Thai</h1>
        <p>Authentic Gourmet Thai Food</p>
    </header>
    
    <nav>
        <ul>
            <li><a href="index.html">Home</a></li>
            <li><a href="about.html">About</a></li>
            <li><a href="menu.html">Menu</a></li>
        </ul>
    </nav>
    
    <main>
        <section>
            <h2>Our Story</h2>
            <p>Founded in 2010, Curbside Thai brings authentic Thai cuisine to Charlotte.</p>
            <p>We use traditional recipes and fresh ingredients.</p>
        </section>
        
        <section>
            <h2>What We Offer</h2>
            <ul>
                <li>Dine-in service</li>
                <li>Take-out orders</li>
                <li>Catering for events</li>
            </ul>
        </section>
        
        <aside>
            <h3>Hours</h3>
            <dl>
                <dt>Monday - Friday</dt>
                <dd>11am - 10pm</dd>
                
                <dt>Saturday - Sunday</dt>
                <dd>12pm - 11pm</dd>
            </dl>
        </aside>
    </main>
    
    <footer>
        <p>&copy; 2025 Curbside Thai</p>
        <p>411 Belde Drive, Charlotte NC 28201</p>
    </footer>
</body>
</html>
```

---

## **Key Takeaways**

- **Semantic elements** describe content meaning (header, nav, section, article, aside, footer)
- **Grouping elements** organize content (div, p, lists, blockquote, figure)
- Use **ONE** `<h1>` per page
- Use **ONE** `<main>` per page
- **Navigation** should be marked with `<nav>` containing an unordered list
- **Lists** come in three types: unordered (`<ul>`), ordered (`<ol>`), and description (`<dl>`)
- Choose semantic elements over generic `<div>` when possible

