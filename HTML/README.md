# 📘 Complete HTML Notes

## 1. HTML Introduction

**Definition:** HTML (HyperText Markup Language) is the standard language used to create and design web pages. It structures content using tags.

**Key Points:**

* HTML is not a programming language, it’s a markup language.
* Web browsers read HTML to display web pages.

**Example Structure:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>My First Page</title>
</head>
<body>
    <h1>Welcome to HTML!</h1>
    <p>This is a paragraph.</p>
</body>
</html>
```

**Explanation:**

* `<!DOCTYPE html>` → Declares the HTML version.
* `<html>` → Root element.
* `<head>` → Contains meta information, title, styles.
* `<body>` → Visible content on the webpage.

💡 **Tip:** HTML elements are case-insensitive, but lowercase is preferred.

---

## 2. HTML Editors

* **Online Editors:** CodePen, JSFiddle, JSBin
* **Desktop Editors:** VS Code, Sublime Text, Atom, Notepad++
* **Browser Developer Tools:** Inspect element to see HTML structure

---

## 3. HTML Basic Structure

**Minimal HTML Page:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Simple Page</title>
</head>
<body>
    <h1>Hello World!</h1>
</body>
</html>
```

**Symbols/Icons for Readability:**

* 📝 Head Section
* 🖥 Body Section

---

## 4. HTML Elements

**Definition:** An element is a combination of a start tag, content, and an end tag.

**Example:**

```html
<p>This is a paragraph.</p>
```

**Common HTML Tags:**

* Headings: `<h1>` to `<h6>`
* Paragraph: `<p>`
* Link: `<a>`
* Image: `<img>`
* List: `<ul>`, `<ol>`, `<li>`

---

## 5. HTML Attributes

**Definition:** Additional information about HTML elements.

**Syntax:**

```html
<tagname attribute="value">Content</tagname>
```

**Example:**

```html
<a href="https://www.example.com" target="_blank">Visit Example</a>
```

**Common Attributes:** `id`, `class`, `style`, `title`, `alt` (images), `src` (images)

💡 **Tip:** Always use `alt` for accessibility.

---

## 6. HTML Headings

* `<h1>` → Largest heading
* `<h6>` → Smallest heading

**Example:**

```html
<h1>Main Title</h1>
<h2>Sub Title</h2>
<h3>Section</h3>
```

🖼 **Diagram Concept:** `<h1> 1 <h2> 2 <h3> 3 <h4> 4 <h5> 5 <h6> 6`

---

## 7. HTML Paragraphs

```html
<p>This is a paragraph of text.</p>
<p>Second paragraph.</p>
```

**Special Paragraph Tags:**

* `<br>` → Line break
* `<hr>` → Horizontal rule (divider)

---

## 8. HTML Styles (Inline & Internal)

**Inline CSS Example:**

```html
<p style="color:red; font-size:18px;">Styled Paragraph</p>
```

**Internal CSS Example:**

```html
<head>
<style>
  p { color: blue; font-size: 20px; }
</style>
</head>
```

---

## 9. HTML Formatting

**Tags for Text Formatting:**

* `<b>` → Bold
* `<i>` → Italic
* `<u>` → Underline
* `<mark>` → Highlight
* `<small>` → Smaller text

**Example:**

```html
<p>This is <b>bold</b> and <i>italic</i> text.</p>
```

---

## 10. HTML Comments

```html
<!-- This is a comment -->
```

Comments are ignored by the browser. Useful for notes or temporarily disabling code.

---

## 11. HTML Colors

**Inline:**

```html
<p style="color:green;">Green Text</p>
```

**Hex Codes:** `#FF5733`
**RGB:** `rgb(255,87,51)`
**Predefined Names:** `red, blue, green`

---

## 12. HTML CSS

**Using `<style>` in HTML:**

```html
<style>
body { background-color: lightyellow; }
h1 { color: darkblue; }
</style>
```

**Linking External CSS:**

```html
<link rel="stylesheet" href="style.css">
```

---

## 13. HTML Links

```html
<a href="https://example.com" target="_blank">Visit Example</a>
```

* `target="_blank"` → Opens in new tab
* `mailto:` → Email link

---

## 14. HTML Images

```html
<img src="image.jpg" alt="My Image" width="300">
```

**Attributes:** `src`, `alt`, `width`, `height`

---

## 15. HTML Favicon

```html
<link rel="icon" href="favicon.ico" type="image/x-icon">
```

Small icon in browser tab.

---

## 16. HTML Page Title

```html
<title>My Website</title>
```

Appears on the browser tab.

---

## 17. HTML Tables

```html
<table border="1">
<tr><th>Name</th><th>Age</th></tr>
<tr><td>Ramesh</td><td>30</td></tr>
</table>
```

* `<tr>` → Table row
* `<th>` → Table header
* `<td>` → Table data

---

## 18. HTML Lists

**Ordered List:**

```html
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
</ol>
```

**Unordered List:**

```html
<ul>
  <li>Item A</li>
  <li>Item B</li>
</ul>
```

---

## 19. HTML Block & Inline Elements

* **Block elements:** Take full width (e.g., `<div>`, `<p>`, `<h1>`)
* **Inline elements:** Take only needed width (e.g., `<span>`, `<a>`, `<strong>`)

---

## 20. HTML Div & Span

```html
<div style="background:lightblue;">Block Section</div>
<span style="color:red;">Inline Text</span>
```

* `div` → Block-level container
* `span` → Inline container

---

## 21. HTML Classes & Ids

```html
<p class="text">Paragraph with class</p>
<p id="unique">Paragraph with id</p>
```

* `class` → Can be used multiple times
* `id` → Unique identifier

---

## 22. HTML Iframes

```html
<iframe src="https://example.com" width="600" height="400"></iframe>
```

Embed another webpage inside your page.

---

## 23. HTML JavaScript

```html
<script>
  alert("Hello World!");
</script>
```

`<script>` used to write or link JS.

---

## 24. HTML File Paths

* **Absolute path:** Full URL
* **Relative path:** Relative to current file

---

## 25. HTML Head

```html
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My Page</title>
</head>
```

* `meta charset` → Character encoding
* `viewport` → Responsive design

---

## 26. HTML Layout

* Use `<div>` and CSS (Flexbox/Grid) for layout
* HTML5 semantic tags: `<header>`, `<footer>`, `<nav>`, `<main>`, `<section>`, `<article>`

---

## ✅ Final Summary

* HTML is the skeleton of webpages.
* Tags and attributes define structure & content.
* Combine with CSS (styles) and JS (interactivity) for full webpages.
* Use semantic tags for better accessibility and SEO.
