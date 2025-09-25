# 🎨 How to Add CSS in HTML

When a browser reads a **stylesheet**, it formats the HTML document according to the rules inside the stylesheet.

---

## 📌 Ways to Insert CSS

There are **3 main ways** to add CSS to HTML:

1. **External CSS**
2. **Internal CSS**
3. **Inline CSS**

Each method has its use-cases. External is best for large sites, internal for single-page special styles, and inline for quick one-off changes.

---

## 1️⃣ External CSS

* Keep styles in a separate `.css` file.
* Reusable across multiple HTML pages.
* Best practice for medium/large projects (separation of concerns).

**HTML (index.html):**

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <link rel="stylesheet" href="mystyle.css">
  <title>External CSS Example</title>
</head>
<body>
  <h1>This is a heading</h1>
  <p>This is a paragraph.</p>
</body>
</html>
```

**CSS (mystyle.css):**

```css
body {
  background-color: lightblue;
}
h1 {
  color: navy;
  margin-left: 20px;
}
```

⚠️ Note: **No space between number and unit**. Example:

* ✅ `margin-left: 20px;`
* ❌ `margin-left: 20 px;`

---

## 2️⃣ Internal CSS

* Defined inside a `<style>` tag in the document `<head>`.
* Useful for styles unique to that single page.

**Example:**

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    body {
      background-color: linen;
    }
    h1 {
      color: maroon;
      margin-left: 40px;
    }
  </style>
  <title>Internal CSS Example</title>
</head>
<body>
  <h1>This is a heading</h1>
  <p>This is a paragraph.</p>
</body>
</html>
```

---

## 3️⃣ Inline CSS

* Added directly to an HTML element using the `style` attribute.
* Useful for quick testing or one-off styling.

**Example:**

```html
<h1 style="color:blue; text-align:center;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>
```

⚠️ **Disadvantage:** mixes structure and style — hard to maintain in larger projects.

---

## 🔁 Multiple Stylesheets & Overrides

If the same element is styled in multiple places, the **last one loaded** (or the one with higher specificity) wins.

**Example:**

```html
<head>
  <link rel="stylesheet" href="mystyle.css">  <!-- external loaded first -->
  <style>
    h1 {
      color: orange; /* internal style loaded after external */
    }
  </style>
</head>
```

In this case, `<h1>` will be **orange** because the internal style overrides the external one (later in cascade).

---

## 🎯 Cascading Order (Priority)

From **highest** priority to **lowest**:

1. Inline CSS (style attribute) — Highest priority
2. Internal CSS (inside `<style>` in `<head>`)
3. External CSS (linked `.css` files)
4. Browser default styles — Lowest priority

Specificity rules and `!important` can affect this order.

---

## 📊 Diagram – CSS Application Order (mermaid)

```
flowchart TD
    A[Browser loads HTML] --> B[Inline CSS]
    A --> C[Internal CSS]
    A --> D[External CSS]
    A --> E[Browser Default]

    B --> F[Final Style Applied]
    C --> F
    D --> F
    E --> F
```

> Note: To render the mermaid diagram you need a viewer that supports mermaid (e.g., VS Code mermaid plugin, GitHub README preview with mermaid enabled, etc.).

---

## 🌀 Tailwind CSS Equivalent

Instead of writing custom CSS, Tailwind provides utility classes that you add directly to HTML elements.

**Normal CSS:**

```html
<h1 style="color:blue; text-align:center;">This is a heading</h1>
```

**Tailwind equivalent:**

```html
<h1 class="text-blue-500 text-center">This is a heading</h1>
```

Tailwind encourages a utility-first approach, reducing the need for custom CSS files in many cases.

---

## ❓ Interview Questions & Answers

**Q1. Difference between Inline, Internal and External CSS?**

* Inline → Inside element (`style` attribute). Highest priority.
* Internal → Inside `<style>` tag in `<head>`.
* External → Separate `.css` file linked with `<link>`; best for reusability.

**Q2. Which CSS has highest priority?**

* Inline CSS has the highest priority (unless overridden by `!important` rules and specificity).

**Q3. Why use External CSS?**

* Reusability across pages
* Separation of concerns (HTML vs CSS)
* Easier maintenance and caching benefits

**Q4. What is the disadvantage of Inline CSS?**

* Not reusable, mixes markup with presentation, and hard to maintain at scale.

**Q5. How does the cascade work when multiple stylesheets are used?**

* Later rules override earlier ones when specificity is equal. Specificity and `!important` can change the result.

---

## ✅ Summary

* **External CSS** → Best for large projects and reuse.
* **Internal CSS** → Useful for single-page custom styles.
* **Inline CSS** → Quick one-off styling (not recommended for production).
* **Tailwind** → Utility-first approach that reduces custom CSS.

---

If you want, I can also generate a downloadable `README.md` file (in the project folder) so you can directly download it. Let me know and I will create the file for you.
