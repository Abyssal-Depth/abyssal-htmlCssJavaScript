# **Lesson 3: Text-Level Elements, Images, and Hyperlinks**

## **Learning Objectives**
- Use text-level elements to mark up inline content
- Insert and configure inline images
- Work with character entities and special symbols
- Create hypertext links to pages, email addresses, and phone numbers
- Understand URLs and link protocols
- Build navigation systems with links

---

## **Text-Level Elements**

Text-level elements (also called inline elements) mark up content within block-level elements like paragraphs and headings. They don't create line breaks.

### **Common Text-Level Elements**

**Emphasis and Importance:**

```html
<p>This is <em>emphasized text</em> (usually italic).</p>
<p>This is <strong>important text</strong> (usually bold).</p>
```

**Visual Styling (Semantic Meaning):**

```html
<p>The book <cite>To Kill a Mockingbird</cite> is a classic.</p>
<p>Press <kbd>Ctrl+C</kbd> to copy.</p>
<p>The program output was: <samp>Hello World</samp></p>
<p>Use the <code>&lt;p&gt;</code> tag for paragraphs.</p>
```

**Other Common Elements:**

```html
<p>H<sub>2</sub>O is the chemical formula for water.</p>
<p>E = mc<sup>2</sup> is Einstein's famous equation.</p>
<p>The price was <s>$50</s> now only $35!</p>
<p>This is <mark>highlighted text</mark>.</p>
<p>The <abbr title="World Wide Web">WWW</abbr> was created in 1989.</p>
```

---

### **Text-Level Elements Reference**

| Element | Purpose | Typical Display |
|---------|---------|-----------------|
| `<em>` | Emphasized text | Italic |
| `<strong>` | Important text | Bold |
| `<b>` | Stylistically bold | Bold |
| `<i>` | Alternate voice/mood | Italic |
| `<cite>` | Title of a work | Italic |
| `<code>` | Computer code | Monospace |
| `<kbd>` | Keyboard input | Monospace |
| `<samp>` | Sample output | Monospace |
| `<var>` | Variable | Italic |
| `<mark>` | Highlighted text | Yellow background |
| `<small>` | Side comments | Smaller text |
| `<sub>` | Subscript | Lower, smaller |
| `<sup>` | Superscript | Higher, smaller |
| `<s>` | Struck-through | Line through |
| `<u>` | Underlined | Underline |
| `<abbr>` | Abbreviation | Dotted underline |
| `<q>` | Short quotation | Quotation marks |

---

### **When to Use `<em>` vs `<i>` and `<strong>` vs `<b>`**

**Semantic (Preferred):**
- `<em>` - For emphasis that changes meaning
- `<strong>` - For strong importance

**Visual (Use sparingly):**
- `<i>` - For technical terms, foreign words, thoughts
- `<b>` - For keywords, product names

**Example:**
```html
<p>You <em>must</em> submit your assignment by Friday.</p>
<p>The term <i>carpe diem</i> means "seize the day."</p>
```

---

## **Line Breaks**

The `<br />` element creates a line break without starting a new paragraph.

```html
<p>
    Curbside Thai<br />
    411 Belde Drive<br />
    Charlotte, NC 28201
</p>
```

**Displays as:**
```
Curbside Thai
411 Belde Drive
Charlotte, NC 28201
```

**Note:** Use `<br />` sparingly. For most layouts, CSS is better than multiple `<br />` tags.

---

## **Special Characters and Character Entities**

### **Why Character Entities?**

Some characters have special meaning in HTML or aren't on your keyboard:

| Character | Entity Code | Named Entity | Description |
|-----------|-------------|--------------|-------------|
| < | `&#60;` | `&lt;` | Less than |
| > | `&#62;` | `&gt;` | Greater than |
| & | `&#38;` | `&amp;` | Ampersand |
| © | `&#169;` | `&copy;` | Copyright |
| ® | `&#174;` | `&reg;` | Registered |
| ™ | `&#8482;` | `&trade;` | Trademark |
| " | `&#34;` | `&quot;` | Quote |
| ' | `&#39;` | `&apos;` | Apostrophe |
| — | `&#8212;` | `&mdash;` | Em dash |
| – | `&#8211;` | `&ndash;` | En dash |
| &nbsp; | `&#160;` | `&nbsp;` | Non-breaking space |
| € | `&#8364;` | `&euro;` | Euro |

---

### **Using Character Entities**

```html
<p>Curbside Thai &copy; 2025</p>
<p>Prices range from $10&ndash;$25</p>
<p>Our Pad Thai&trade; is the best!</p>
<p>Call us at 704&ndash;555&ndash;1151</p>
<p>To display &lt;p&gt; tags, use character entities.</p>
```

**Displays as:**
```
Curbside Thai © 2025
Prices range from $10–$25
Our Pad Thai™ is the best!
Call us at 704–555–1151
To display <p> tags, use character entities.
```

---

### **Non-Breaking Spaces**

`&nbsp;` prevents text from wrapping at that space.

```html
<p>Price: $25&nbsp;per&nbsp;person</p>
```

**Use for:**
- Keeping numbers with units together
- Preventing awkward line breaks
- Creating multiple spaces (though CSS is preferred)

---

## **Working with Inline Images**

### **The `<img>` Element**

Images are embedded content placed inline with text.

```html
<img src="file" alt="description" />
```

**Required Attributes:**
- `src` - Path to the image file
- `alt` - Alternative text description

---

### **Image File Types**

| Format | Extension | Best For | Notes |
|--------|-----------|----------|-------|
| JPEG | .jpg, .jpeg | Photos | Compressed, no transparency |
| PNG | .png | Graphics, logos | Supports transparency |
| GIF | .gif | Simple animations | Limited colors |
| SVG | .svg | Scalable graphics | Vector, infinitely scalable |
| WebP | .webp | Modern web | Better compression |

---

### **Basic Image Examples**

```html
<!-- Simple image -->
<img src="logo.png" alt="Curbside Thai Logo" />

<!-- Image with dimensions -->
<img src="photo.jpg" alt="Restaurant interior" width="600" height="400" />

<!-- Image in a different folder -->
<img src="images/menu-item.jpg" alt="Pad Thai dish" />
```

---

### **The `alt` Attribute**

The `alt` attribute is **required** and serves multiple purposes:

**1. Accessibility:** Screen readers read alt text to visually impaired users

**2. SEO:** Search engines use alt text to understand images

**3. Fallback:** Displays if image fails to load

**Good Alt Text:**
```html
<img src="pad-thai.jpg" alt="Plate of Pad Thai with shrimp, peanuts, and lime" />
```

**Poor Alt Text:**
```html
<img src="pad-thai.jpg" alt="image" />
<img src="pad-thai.jpg" alt="img_001.jpg" />
```

**Decorative Images:**
```html
<img src="decorative-line.png" alt="" />
```
*(Empty alt for purely decorative images)*

---

### **Image Dimensions**

Specify width and height to prevent page jumping during load:

```html
<img src="banner.jpg" alt="Welcome banner" width="800" height="200" />
```

**Best Practice:** Set dimensions in CSS, not HTML attributes (covered in CSS lessons).

---

### **Images with Figures**

Group images with captions using `<figure>`:

```html
<figure>
    <img src="restaurant.jpg" alt="Exterior of Curbside Thai restaurant" />
    <figcaption>Our Charlotte location on Belde Drive</figcaption>
</figure>
```

---

## **Hypertext Links**

### **The `<a>` Element**

Create clickable links with the anchor element:

```html
<a href="url">link text</a>
```

**Example:**
```html
<p>Visit our <a href="menu.html">menu page</a> to see all dishes.</p>
```

---

### **Understanding URLs**

**URL (Uniform Resource Locator)** specifies the location of a resource.

**General Structure:**
```
scheme://server/path/filename
```

**Examples:**
```
https://www.example.com/products/item.html
mailto:info@example.com
tel:+17045551151
```

---

### **URL Schemes**

| Scheme | Purpose | Example |
|--------|---------|---------|
| `http://` | Web page (unsecured) | `http://example.com` |
| `https://` | Web page (secured) | `https://example.com` |
| `file://` | Local file | `file:///C:/documents/file.html` |
| `mailto:` | Email address | `mailto:contact@example.com` |
| `tel:` | Phone number | `tel:+17045551151` |
| `ftp://` | File transfer | `ftp://ftp.example.com` |
| `sms:` | Text message | `sms:+17045551151` |

---

### **Relative vs Absolute Paths**

**Absolute URL** - Complete path from the root:
```html
<a href="https://www.curbsidethai.com/menu.html">Menu</a>
<a href="http://www.example.com/about.html">About</a>
```

**Relative URL** - Path relative to current file:
```html
<!-- Same folder -->
<a href="menu.html">Menu</a>

<!-- Subfolder -->
<a href="pages/about.html">About</a>

<!-- Parent folder -->
<a href="../index.html">Home</a>

<!-- Root of site -->
<a href="/contact.html">Contact</a>
```

---

### **Relative Path Examples**

**File Structure:**
```
website/
├── index.html
├── about.html
├── pages/
│   ├── menu.html
│   └── contact.html
└── images/
    └── logo.png
```

**From `index.html`:**
```html
<a href="about.html">About</a>
<a href="pages/menu.html">Menu</a>
<img src="images/logo.png" alt="Logo" />
```

**From `pages/menu.html`:**
```html
<a href="../index.html">Home</a>
<a href="../about.html">About</a>
<a href="contact.html">Contact</a>
<img src="../images/logo.png" alt="Logo" />
```

---

### **Linking to Specific Page Sections**

Use `id` attributes to create anchors:

```html
<!-- Target section -->
<section id="hours">
    <h2>Hours of Operation</h2>
    <p>Monday-Friday: 11am-10pm</p>
</section>

<!-- Link to that section -->
<a href="#hours">View our hours</a>

<!-- Link from another page -->
<a href="about.html#hours">See hours</a>
```

---

### **Link Attributes**

**Open in New Tab:**
```html
<a href="https://external-site.com" target="_blank">External Site</a>
```

**Add Title (Tooltip):**
```html
<a href="menu.html" title="View our full menu">Menu</a>
```

**Download File:**
```html
<a href="menu.pdf" download>Download Menu (PDF)</a>
```

---

## **Email Links**

Create clickable email addresses with `mailto:`:

```html
<a href="mailto:info@curbsidethai.com">Email Us</a>
```

**With Subject Line:**
```html
<a href="mailto:info@curbsidethai.com?subject=Catering Inquiry">
    Catering Questions
</a>
```

**With CC and Body:**
```html
<a href="mailto:info@curbsidethai.com?subject=Feedback&cc=manager@curbsidethai.com&body=Hello,">
    Send Feedback
</a>
```

**Multiple Recipients:**
```html
<a href="mailto:info@curbsidethai.com,support@curbsidethai.com">
    Contact Team
</a>
```

---

## **Phone Links**

Create clickable phone numbers with `tel:`:

```html
<a href="tel:+17045551151">704-555-1151</a>
```

**International Format:**
```html
<a href="tel:+1-704-555-1151">(704) 555-1151</a>
```

**Best Practices:**
- Use full international format in `href`: `+1-XXX-XXX-XXXX`
- Format displayed text for readability: `(704) 555-1151`
- Especially useful for mobile devices

```html
<p>
    Call us at 
    <a href="tel:+17045551151">704-555-1151</a> 
    to place an order.
</p>
```

---

## **SMS Links**

Create links that open messaging apps:

```html
<a href="sms:+17045551151">Text Us</a>
```

**With Pre-filled Message:**
```html
<a href="sms:+17045551151?body=I would like to place an order">
    Text to Order
</a>
```

---

## **Image Links**

Turn images into clickable links:

```html
<a href="index.html">
    <img src="logo.png" alt="Curbside Thai Logo" />
</a>
```

**Image with Caption as Link:**
```html
<figure>
    <a href="menu.html">
        <img src="pad-thai.jpg" alt="Delicious Pad Thai" />
        <figcaption>Click to see full menu</figcaption>
    </a>
</figure>
```

---

## **Navigation Lists**

Combine lists and links for website navigation:

```html
<nav>
    <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="menu.html">Menu</a></li>
        <li><a href="locations.html">Locations</a></li>
        <li><a href="contact.html">Contact</a></li>
    </ul>
</nav>
```

---

### **Multi-Level Navigation**

```html
<nav>
    <ul>
        <li><a href="index.html">Home</a></li>
        <li>
            <a href="menu.html">Menu</a>
            <ul>
                <li><a href="menu.html#appetizers">Appetizers</a></li>
                <li><a href="menu.html#entrees">Entrees</a></li>
                <li><a href="menu.html#desserts">Desserts</a></li>
            </ul>
        </li>
        <li><a href="contact.html">Contact</a></li>
    </ul>
</nav>
```

---

## **Complete Example Page**

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>Curbside Thai - About Us</title>
</head>
<body>
    <header>
        <a href="index.html">
            <img src="images/logo.png" alt="Curbside Thai Logo" />
        </a>
        <h1>Curbside Thai</h1>
        <p>Authentic Gourmet Thai Food</p>
    </header>
    
    <nav>
        <ul>
            <li><a href="index.html">Home</a></li>
            <li><a href="about.html">About</a></li>
            <li><a href="menu.html">Menu</a></li>
            <li><a href="locations.html">Locations</a></li>
            <li><a href="contact.html">Contact</a></li>
        </ul>
    </nav>
    
    <main>
        <section id="story">
            <h2>Our Story</h2>
            <p>
                Founded in 2010, <strong>Curbside Thai</strong> brings 
                <em>authentic</em> Thai cuisine to Charlotte.
            </p>
            
            <figure>
                <img src="images/restaurant.jpg" 
                     alt="Interior of Curbside Thai restaurant" 
                     width="600" 
                     height="400" />
                <figcaption>Our welcoming dining room</figcaption>
            </figure>
        </section>
        
        <section id="contact-info">
            <h2>Visit Us</h2>
            <p>
                <strong>Address:</strong><br />
                411 Belde Drive<br />
                Charlotte, NC 28201
            </p>
            
            <p>
                <strong>Phone:</strong> 
                <a href="tel:+17045551151">704-555-1151</a>
            </p>
            
            <p>
                <strong>Email:</strong> 
                <a href="mailto:info@curbsidethai.com">info@curbsidethai.com</a>
            </p>
        </section>
        
        <section id="hours">
            <h2>Hours of Operation</h2>
            <dl>
                <dt>Monday&ndash;Friday</dt>
                <dd>11:00am&ndash;10:00pm</dd>
                
                <dt>Saturday&ndash;Sunday</dt>
                <dd>12:00pm&ndash;11:00pm</dd>
            </dl>
        </section>
    </main>
    
    <footer>
        <p>&copy; 2025 Curbside Thai. All rights reserved.</p>
        <p>
            <a href="#story">Back to Top</a> | 
            <a href="privacy.html">Privacy Policy</a>
        </p>
    </footer>
</body>
</html>
```

---

## **Best Practices**

### **Images:**
- Always include `alt` attributes
- Use appropriate file formats
- Optimize image file sizes
- Specify dimensions when possible

### **Links:**
- Use descriptive link text (not "click here")
- Test all links regularly
- Use relative paths for internal links
- Open external links in new tabs if appropriate

### **Accessibility:**
- Provide meaningful alt text
- Use semantic HTML
- Ensure sufficient color contrast
- Make interactive elements keyboard-accessible

---

## **Key Takeaways**

- **Text-level elements** add semantic meaning to inline content
- **Character entities** display special symbols: `&copy;`, `&ndash;`, `&lt;`
- **Images** require `src` and `alt` attributes
- **Links** are created with `<a href="url">text</a>`
- **Navigation** typically uses `<nav>` with `<ul>` lists
- Use **relative paths** for internal links
- **Email links** use `mailto:`
- **Phone links** use `tel:`
- Always write **descriptive link text** and **meaningful alt text**
