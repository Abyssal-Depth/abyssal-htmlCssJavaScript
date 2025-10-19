# HTML Basics Lesson Series

---

# **Lesson 1: Introduction to HTML and Document Structure**

## **Learning Objectives**
- Understand the history and purpose of HTML
- Create a basic HTML document structure
- Work with the document head and metadata
- Add comments to HTML documents

---

## **What is HTML?**

**HTML (Hypertext Markup Language)** is a markup language that describes the content and structure of web documents by identifying, or tagging, different document elements.

HTML files are text files that:
- Can be created in any text editor
- Are displayed by web browsers
- Form the foundation of every web page

---

## **A Brief History**

- **1989**: Tim Berners-Lee and researchers at CERN developed the World Wide Web
- **1995**: HTML 2.0 introduced interactive elements (web forms)
- **1999**: HTML 4.01 added support for style sheets and multimedia
- **2001**: XHTML 1.0 introduced stricter standards
- **2012**: HTML5 became the current standard

**W3C (World Wide Web Consortium)** maintains HTML standards, though it has no enforcement power. The industry follows these recommendations for consistency.

---

## **Basic HTML Document Structure**

Every HTML document follows this basic structure:

```html
<!DOCTYPE html>
<html>
<head>
    <!-- Document metadata goes here -->
</head>
<body>
    <!-- Visible page content goes here -->
</body>
</html>
```

### **Breaking It Down**

1. **`<!DOCTYPE html>`** - Declares this is an HTML5 document
2. **`<html>`** - Root element containing all other elements
3. **`<head>`** - Contains metadata about the document
4. **`<body>`** - Contains the visible page content

---

## **Understanding HTML Elements**

### **Two-Sided Tags**

Most HTML elements use opening and closing tags:

```html
<element>content</element>
```

**Example:**
```html
<p>Welcome to Curbside Thai.</p>
```

### **Empty Elements**

Some elements are self-closing (empty elements):

```html
<element />
```

**Examples:**
```html
<br />
<img src="logo.png" alt="Logo" />
<meta charset="utf-8" />
```

---

## **Element Attributes**

Attributes provide additional information about elements:

```html
<element attr1="value1" attr2="value2">content</element>
```

**Example:**
```html
<img src="logo.png" alt="Company Logo" />
```

Common attributes:
- `src` - Source file location
- `alt` - Alternative text
- `href` - Hyperlink reference
- `class` - CSS class name
- `id` - Unique identifier

---

## **The Document Head**

The `<head>` section contains **metadata** - information about the document that doesn't appear in the browser window.

### **Essential Head Elements**

```html
<head>
    <!-- Character encoding -->
    <meta charset="utf-8" />
    
    <!-- Page title -->
    <title>About Curbside Thai</title>
    
    <!-- Keywords for search engines -->
    <meta name="keywords" content="Thai, restaurant, Charlotte, food" />
    
    <!-- Link to style sheet -->
    <link href="styles.css" rel="stylesheet" />
</head>
```

---

## **Setting the Page Title**

The `<title>` element is required and serves multiple purposes:
- Appears in the browser tab or title bar
- Shows in browser bookmarks
- Displays in search engine results

```html
<title>About Curbside Thai</title>
```

---

## **Character Encoding**

Character encoding tells the browser how to interpret text characters:

```html
<meta charset="utf-8" />
```

**UTF-8** is the standard encoding that supports:
- All English characters
- International characters
- Special symbols
- Emoji

---

## **Adding Comments**

Comments help document your code but don't appear in the browser:

```html
<!-- This is a comment -->
```

**Multi-line comments:**
```html
<!--
    New Perspectives on HTML5 and CSS3, 7th Edition
    Tutorial 1
    Author: Your Name
    Date: October 4, 2025
    
    Filename: about.html
-->
```

**Best Practice:** Always include a comment block at the top of your HTML files with:
- Project information
- Author name
- Date
- Filename

---

## **White Space in HTML**

HTML collapses multiple white-space characters (spaces, tabs, line breaks) into a single space.

This code:
```html
<p>Welcome    to
   Curbside    Thai.</p>
```

Displays as:
```
Welcome to Curbside Thai.
```

**Use white space to make your code readable!**

---

## **Complete Example**

Here's a complete basic HTML document:

```html
<!DOCTYPE html>
<html>
<head>
    <!--
        Curbside Thai Website
        Author: Your Name
        Date: October 4, 2025
        Filename: about.html
    -->
    <meta charset="utf-8" />
    <meta name="keywords" content="Thai, restaurant, Charlotte, food" />
    <title>About Curbside Thai</title>
    <link href="ct_base.css" rel="stylesheet" />
</head>
<body>
    <h1>Welcome to Curbside Thai</h1>
    <p>Authentic gourmet Thai food.</p>
</body>
</html>
```

---

## **Key Takeaways**

- HTML uses tags to mark up content
- Every HTML document needs: `<!DOCTYPE html>`, `<html>`, `<head>`, and `<body>`
- The `<head>` contains metadata (title, character encoding, keywords)
- The `<body>` contains visible content
- Comments help document your code
- White space improves code readability but doesn't affect display
