# 📘 Advanced HTML Notes

## 1. Semantic HTML

**Definition:** Tags that clearly describe their meaning, improving readability and SEO.

**Common Semantic Tags:**

| Tag         | Purpose                                    |
| ----------- | ------------------------------------------ |
| `<header>`  | Top section, typically navigation or title |
| `<footer>`  | Bottom section                             |
| `<nav>`     | Navigation links                           |
| `<main>`    | Main content area                          |
| `<section>` | Section of content                         |
| `<article>` | Independent, self-contained content        |
| `<aside>`   | Sidebar, related content                   |

**Example:**

```html
<header>
  <h1>Website Title</h1>
  <nav>
    <a href="#">Home</a>
    <a href="#">About</a>
  </nav>
</header>

<main>
  <article>
    <h2>Article Title</h2>
    <p>Article content...</p>
  </article>
  <aside>
    <p>Related Info</p>
  </aside>
</main>

<footer>
  <p>&copy; 2025 My Website</p>
</footer>
```

---

## 2. HTML Forms

Forms collect user input.

**Basic Form:**

```html
<form action="/submit" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required><br><br>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email"><br><br>

  <label>Password:</label>
  <input type="password" name="password"><br><br>

  <input type="submit" value="Submit">
</form>
```

**Common Input Types:** text, email, password, number, date, color, file, checkbox, radio, range, url

**Advanced Attributes:**

* `placeholder` → Example text
* `required` → Mandatory field
* `maxlength`, `min`, `max`, `step`
* `pattern` → Regex validation

---

## 3. HTML5 Multimedia

**Images:** `<img>`

**Video:**

```html
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  Your browser does not support HTML5 video.
</video>
```

**Audio:**

```html
<audio controls>
  <source src="audio.mp3" type="audio/mp3">
  Your browser does not support audio.
</audio>
```

**Attributes:** controls, autoplay, loop, muted

---

## 4. HTML5 APIs

**Modern HTML supports APIs for dynamic features:**

| API             | Description                             |
| --------------- | --------------------------------------- |
| Geolocation API | Get user’s location                     |
| Drag & Drop API | Drag elements within a page             |
| LocalStorage    | Store data in the browser persistently  |
| SessionStorage  | Store data in the browser for a session |
| Canvas API      | Draw graphics dynamically               |
| Web Workers     | Run scripts in background threads       |

**Example – LocalStorage:**

```html
<script>
  localStorage.setItem("username", "Ramesh");
  console.log(localStorage.getItem("username")); // Ramesh
</script>
```

---

## 5. HTML Meta Tags

Used in `<head>` for SEO, responsiveness, and page info.

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Complete HTML tutorial for beginners and advanced">
<meta name="keywords" content="HTML, HTML5, Tutorial, Web Development">
<meta name="author" content="Ramesh">
```

**Icons:**

* favicon: `<link rel="icon" href="favicon.ico">`
* apple-touch-icon: for mobile devices

---

## 6. HTML Accessibility (a11y)

Make websites usable for all users, including those with disabilities.

**Techniques:**

* `alt` attribute for images
* `aria-*` attributes for better screen reader support
* `<label>` associated with inputs
* Proper heading hierarchy (`<h1>` → `<h2>` → `<h3>`)
* Keyboard navigable links and forms

**Example:**

```html
<img src="logo.png" alt="Company Logo">
<label for="email">Email</label>
<input type="email" id="email" aria-required="true">
```

---

## 7. HTML SEO Best Practices

* Use semantic tags
* Descriptive `<title>` and `<meta>`
* Use `<h1>` for main title, `<h2>` for sections
* Use meaningful alt in images
* Keep URLs clean and readable

---

## 8. HTML Entities & Symbols

HTML entities are special characters:

| Entity     | Symbol |
| ---------- | ------ |
| `&copy;`   | ©      |
| `&reg;`    | ®      |
| `&trade;`  | ™      |
| `&lt;`     | <      |
| `&gt;`     | >      |
| `&amp;`    | &      |
| `&hearts;` | ♥      |

**Example:**

```html
<p>&copy; 2025 My Website</p>
<p>Love &hearts; HTML</p>
```

---

## 9. HTML Canvas

The `<canvas>` element allows drawing graphics via JavaScript.

```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>
<script>
  const canvas = document.getElementById('myCanvas');
  const ctx = canvas.getContext('2d');
  ctx.fillStyle = 'red';
  ctx.fillRect(20, 20, 150, 50);
</script>
```

---

## 10. HTML Drag & Drop

```html
<div id="drag1" draggable="true" ondragstart="drag(event)">Drag me</div>
<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>

<script>
function allowDrop(ev) { ev.preventDefault(); }
function drag(ev) { ev.dataTransfer.setData("text", ev.target.id); }
function drop(ev) {
  ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}
</script>
```

---

## 11. HTML Templates

Use `<template>` to define reusable HTML fragments.

```html
<template id="my-template">
  <p>Hello, this is a template!</p>
</template>

<div id="content"></div>

<script>
  const template = document.getElementById('my-template');
  const clone = template.content.cloneNode(true);
  document.getElementById('content').appendChild(clone);
</script>
```

---

## 12. HTML Best Practices

* Always use semantic tags
* Keep code clean and indented
* Use lowercase for tags and attributes
* Close all tags properly
* Validate HTML using W3C Validator
* Minimize inline styles (use CSS files)
* Optimize images and multimedia

---

## ✅ Advanced HTML Summary

* Semantic tags improve readability and SEO
* Forms and input validation enhance user experience
* Multimedia tags handle audio, video, and interactive content
* HTML5 APIs enable dynamic, interactive websites
* Accessibility and SEO practices make your website user-friendly
* Canvas and templates allow advanced graphics and reusable components
