# 📘 HTML Complete Tutorial (Beginner → Advanced)

A complete HTML guide with examples, Tailwind CSS integration, detailed explanations, visual diagrams, and previous year & advanced questions.

---

## 📝 Table of Contents

1. [HTML Basics](#html-basics)
2. [HTML Elements & Attributes](#html-elements--attributes)
3. [HTML Headings & Paragraphs](#html-headings--paragraphs)
4. [HTML Styles & Formatting](#html-styles--formatting)
5. [HTML Links & Images](#html-links--images)
6. [HTML Tables & Lists](#html-tables--lists)
7. [HTML Div, Classes & Id](#html-div-classes--id)
8. [HTML Forms](#html-forms)
9. [HTML Media](#html-media)
10. [HTML Graphics](#html-graphics)
11. [HTML APIs](#html-apis)
12. [HTML Semantics & Advanced Topics](#html-semantics--advanced-topics)
13. [HTML Responsive Design](#html-responsive-design)
14. [Visual Diagrams](#visual-diagrams)
15. [Previous Year Questions & Answers](#previous-year-questions--answers)
16. [Advanced Interview Questions](#advanced-interview-questions)

---

## HTML Basics

### 📌 HTML Introduction

* **Definition:** HTML (HyperText Markup Language) is the standard language for creating web pages.
* **Syntax:**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <!-- Page content goes here -->
  </body>
</html>
```

* **Example:**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Page</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <p>This is my first HTML page.</p>
  </body>
</html>
```

* **Summary:**

  * `<!DOCTYPE html>` → Defines HTML5 document
  * `<html>` → Root element
  * `<head>` → Contains metadata
  * `<body>` → Visible content

### 📌 HTML Editors

* **Definition:** Tools used to write HTML code
* **Examples:** VS Code, Sublime Text, Atom, Notepad++
* **Summary:** Editors with live preview and syntax highlighting improve productivity.

---

## HTML Elements & Attributes

### 🔹 HTML Elements

* **Definition:** Basic building blocks of HTML.
* **Syntax:** `<tagname>Content</tagname>`
* **Example:** `<p>This is a paragraph.</p>`

### 🔹 HTML Attributes

* **Definition:** Extra information about elements.
* **Syntax:** `<tag attribute="value">Content</tag>`
* **Example:**

```html
<a href="https://example.com" target="_blank">Visit Example</a>
```

* **Summary:** Common attributes: `id`, `class`, `style`, `href`, `src`, `alt`.

---

## HTML Headings & Paragraphs

### 🔹 Headings

```html
<h1>Main Title</h1>
<h2>Subheading</h2>
```

* **Summary:** Use `<h1>` to `<h6>` to structure content hierarchically.

### 🔹 Paragraphs

```html
<p>This is a paragraph.</p>
```

* **Summary:** Wrap text in `<p>` tags for semantic structure.

---

## HTML Styles & Formatting

### 🔹 Inline CSS

```html
<p style="color:blue; font-size:18px;">Styled paragraph</p>
```

### 🔹 Tailwind CSS Example

```html
<p class="text-blue-500 text-lg">Styled with Tailwind</p>
```

### 🔹 Formatting Tags

* `<b>` → Bold text
* `<i>` → Italic text
* `<strong>` → Important text
* `<em>` → Emphasized text
* `<mark>` → Highlighted text

---

## HTML Links & Images

### 🔹 Links

```html
<a href="https://example.com" target="_blank">Visit Example</a>
```

### 🔹 Images

```html
<img src="image.jpg" alt="Description">
```

### 🔹 Tailwind Example

```html
<a href="#" class="text-blue-500 hover:underline">Click Here</a>
<img src="image.jpg" alt="Sample" class="rounded-lg shadow-md">
```

---

## HTML Tables & Lists

### 🔹 Tables

```html
<table>
  <tr>
    <th>Header1</th>
    <th>Header2</th>
  </tr>
  <tr>
    <td>Data1</td>
    <td>Data2</td>
  </tr>
</table>
```

### 🔹 Lists

* Ordered: `<ol><li>Item</li></ol>`
* Unordered: `<ul><li>Item</li></ul>`
* Definition: `<dl><dt>Term</dt><dd>Definition</dd></dl>`

---

## HTML Div, Classes & Id

```html
<div id="container" class="bg-gray-100 p-4">
  <p>Content inside div</p>
</div>
```

* **Summary:** Use `id` for unique element, `class` for reusable styling.

---

## HTML Forms

```html
<form action="/submit" method="post">
  <input type="text" name="username" placeholder="Enter name">
  <input type="submit" value="Submit">
</form>
```

* **Summary:** Forms collect user input. Common attributes: `action`, `method`, `name`, `placeholder`.

---

## HTML Media

### 🔹 Video

```html
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
</video>
```

### 🔹 Audio

```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
</audio>
```

---

## HTML Graphics

### 🔹 Canvas

```html
<canvas id="myCanvas" width="200" height="100"></canvas>
<script>
  const c = document.getElementById("myCanvas");
  const ctx = c.getContext("2d");
  ctx.fillStyle = "red";
  ctx.fillRect(10,10,150,80);
</script>
```

### 🔹 SVG

```html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" stroke="green" fill="yellow" stroke-width="4"/>
</svg>
```

---

## HTML APIs

### 🔹 Geolocation

```html
<button onclick="getLocation()">Get Location</button>
<script>
function getLocation() {
  navigator.geolocation.getCurrentPosition(pos => {
    alert(`Latitude: ${pos.coords.latitude}, Longitude: ${pos.coords.longitude}`);
  });
}
</script>
```

### 🔹 Drag & Drop

```html
<div id="drag" draggable="true">Drag me</div>
```

---

## HTML Semantics & Advanced Topics

* Semantic tags: `<header>`, `<footer>`, `<article>`, `<section>`, `<nav>`
* Improves accessibility and SEO.

---

## HTML Responsive Design

* Use **media queries**:

```html
<style>
@media (max-width:600px){
  body{background-color: lightblue;}
}
</style>
```

* Tailwind responsive example:

```html
<p class="text-lg md:text-xl lg:text-2xl">Responsive Text</p>
```

---

## Visual Diagrams

### HTML Document Structure

```
HTML
├── Head
│   └── Title
└── Body
    ├── Header
    ├── Nav
    ├── Main
    └── Footer
```

### HTML Forms Structure

```
Form
├── Label + Input (Username)
├── Label + Input (Password)
└── Submit Button
```

### HTML Table Structure

```
Table
├── Row 1 (Headers)
│   ├── Header1
│   └── Header2
└── Row 2 (Data)
    ├── Data1
    └── Data2
```

---

## Previous Year Questions & Answers

### 🔹 Q1: Difference between HTML and XHTML?

* ✅ HTML is flexible, XHTML is strict.

### 🔹 Q2: What are semantic tags?

* ✅ `<header>`, `<footer>`, `<article>`, `<section>`

### 🔹 Q3: Difference between `<div>` and `<span>`?

* ✅ `<div>` block-level, `<span>` inline

### 🔹 Q4: Types of lists?

* ✅ `<ol>`, `<ul>`, `<dl>`

### 🔹 Q5: Inline, block, inline-block difference?

* ✅ Inline: no new line, Block: new line, Inline-block: inline + accepts width/height

### 🔹 Q6: How to include CSS?

* ✅ Inline, Internal, External

### 🔹 Q7: `<strong>` vs `<b>`?

* ✅ `<strong>` semantic, `<b>` visual

### 🔹 Q8: Purpose of `alt` in `<img>`?

* ✅ Accessibility, SEO, fallback text

### 🔹 Q9: `<iframe>` vs `<object>`?

* ✅ `<iframe>` embeds HTML, `<object>` embeds media

### 🔹 Q10: `<section>` vs `<div>`?

* ✅ `<section>` semantic, `<div>` generic

---

## Advanced Interview Questions

### 🔹 Q11: Difference between `position: relative` and `position: absolute`?

* ✅ Relative: positioned relative to normal position
* ✅ Absolute: positioned relative to nearest positioned ancestor

### 🔹 Q12: Difference between `<link>` and `<script>`?

* ✅ `<link>`: link CSS
* ✅ `<script>`: embed JavaScript

### 🔹 Q13: How does HTML5 improve web accessibility?

* ✅ Semantic tags `<header>`, `<nav>`, `<main>`, `<footer>`
* ✅ ARIA attributes

### 🔹 Q14: Difference between cookies, localStorage, sessionStorage?

* ✅ Cookies: sent to server, expires
* ✅ localStorage: persists in browser
* ✅ sessionStorage: session-only

### 🔹 Q15: Difference between `<canvas>` and `<svg>`?

* ✅ Canvas: pixel-based, good for animations
* ✅ SVG: vector-based, scalable graphics
