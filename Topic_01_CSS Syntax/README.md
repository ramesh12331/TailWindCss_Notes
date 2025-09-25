# 🎨 CSS Syntax – Beginner to Pro

CSS (Cascading Style Sheets) is used to style HTML elements. Every CSS rule follows a basic syntax → **Selector + Declaration Block**.

---

## 📌 1. CSS Rule Syntax

A CSS rule consists of:

* **Selector** → Points to the HTML element(s) you want to style.
* **Declaration Block** → Contains one or more declarations inside `{}`.

Each declaration = `property: value;`

✅ General Syntax:

```css
selector {
  property: value;
  property: value;
}
```

---

## 📌 2. Example – Styling Paragraph

```css
p {
  color: red;
  text-align: center;
}
```

✅ Example Explained:

* `p` → Selector (applies to `<p>` elements).
* `color: red;` → Declaration (property = color, value = red).
* `text-align: center;` → Declaration (property = text-align, value = center).

---

## 📊 3. CSS Rule Diagram

```css
p {
  color: red;
  text-align: center;
}
```

```
 ↑       ↑              ↑
Selector Property:Value Declaration Block
```

---

## 📌 4. Multiple Declarations

Each declaration is separated by a `;` semicolon.
Curly braces `{}` wrap the block.

```css
h1 {
  font-size: 32px;
  font-weight: bold;
  background-color: yellow;
}
```

---

## 📌 5. CSS Syntax vs Tailwind CSS

Tailwind CSS uses utility classes instead of writing custom CSS rules.

✅ CSS Syntax:

```css
p {
  color: red;
  text-align: center;
}
```

✅ Tailwind CSS Equivalent:

```html
<p class="text-red-500 text-center">Hello World</p>
```

---

## 📊 6. CSS vs Tailwind Visual Diagram

```
+-----------------------------+      +-----------------------------+
|          CSS Syntax         |      |      Tailwind CSS Syntax    |
+-----------------------------+      +-----------------------------+
| Selector: p                 |      | HTML Element: <p>           |
| Declaration Block {         |      | class="text-red-500         |
|   color: red;               |      |        text-center"         |
|   text-align: center;       |      |                             |
| }                           |      |                             |
+-----------------------------+      +-----------------------------+
   ↓ Applied to all <p> tags          ↓ Applied directly via class
```

---

## 📌 7. More Tailwind Examples

✅ CSS:

```css
h1 {
  font-size: 24px;
  font-weight: bold;
  color: blue;
}
```

✅ Tailwind:

```html
<h1 class="text-2xl font-bold text-blue-500">Heading</h1>
```

---

## 📌 8. Summary Table

| Term              | Meaning                                  |
| ----------------- | ---------------------------------------- |
| Selector          | HTML element you want to style           |
| Property          | Style attribute (e.g., color, font-size) |
| Value             | Setting for property (e.g., red, 16px)   |
| Declaration       | Combination of property + value          |
| Declaration Block | `{}` wrapping multiple declarations      |

---

## 📌 9. Interview Questions & Answers

**Q1. What is a CSS selector?**
👉 It identifies which HTML element(s) should be styled. Example: `p`, `.class`, `#id`.

**Q2. Difference between property and value?**
👉 Property = styling attribute (e.g., color). Value = assigned setting (e.g., red).

**Q3. Can a CSS rule have multiple declarations?**
👉 Yes, multiple declarations are separated by `;` inside `{}`.

**Q4. What’s the difference between CSS and Tailwind CSS?**
👉 CSS → Write rules manually. Tailwind → Apply prebuilt utility classes directly.

**Q5. Is Tailwind CSS inline CSS?**
👉 No. Tailwind is utility-first CSS where classes map to CSS rules.

---

## ✅ Summary

* **CSS** = `Selector + Declaration Block { property: value; }`
* **Tailwind** = Use utility classes instead of writing CSS manually.
* Both achieve the same result but Tailwind speeds up styling.
