# 🎨 CSS Fonts Guide

Fonts are one of the most important parts of **web design**.
They affect **readability, branding, and user experience** ✅

---

## 📖 Summary

### ✨ Why Fonts Matter?

* 🎨 Fonts create a brand identity.
* 👀 Easy-to-read fonts improve user experience.
* 🌍 Always use **fallback fonts** (in case the first choice is not available).

### ✍ CSS `font-family` Property

The `font-family` property defines the font for an element.

🔹 **Syntax:**

```css
selector {
  font-family: "Font Name", FallbackFont, generic-family;
}
```

💡 Always start with your preferred font.
💡 End with a **generic family** (`serif`, `sans-serif`, `monospace`, etc.).

---

## 📝 Examples

### 🎨 CSS Font Examples

```css
.p1 {
  font-family: "Times New Roman", Times, serif;
}

.p2 {
  font-family: Arial, Helvetica, sans-serif;
}

.p3 {
  font-family: "Lucida Console", "Courier New", monospace;
}
```

### 🖱 Tailwind CSS Examples

```html
<p class="font-serif">This is Serif font</p>
<p class="font-sans">This is Sans-serif font</p>
<p class="font-mono">This is Monospace font</p>
```

---

## 📊 Diagram – Font Fallback System

```
🖋 Preferred Font → 📝 Next Fallback → 🌐 Generic Family
"Times New Roman" → Times → serif
```

If the first font is unavailable, the browser tries the next,
and finally defaults to the **generic family**.

---

## 🔤 CSS Font Properties

| Property       | Description                               | Example                                     |
| -------------- | ----------------------------------------- | ------------------------------------------- |
| `font-family`  | Sets font type                            | `font-family: Arial, sans-serif;`           |
| `font-style`   | Normal / Italic / Oblique                 | `font-style: italic;`                       |
| `font-weight`  | Thickness of text (100–900, normal, bold) | `font-weight: 700;`                         |
| `font-variant` | Small caps                                | `font-variant: small-caps;`                 |
| `font-size`    | Size of text (px, em, rem, %, vw)         | `font-size: 16px;`                          |
| `font`         | Shorthand for multiple font properties    | `font: italic bold 16px Arial, sans-serif;` |

---

## 🌍 Web Safe Fonts

| Generic Family | Common Fonts                        |
| -------------- | ----------------------------------- |
| Serif          | Times New Roman, Georgia, Garamond  |
| Sans-serif     | Arial, Verdana, Tahoma, Helvetica   |
| Monospace      | Courier New, Lucida Console         |
| Cursive        | Brush Script MT, Lucida Handwriting |
| Fantasy        | Copperplate, Papyrus                |

---

## 🧩 Font Sizes

* `px` → Absolute, fixed size.
* `em` → Relative to parent font-size.
* `rem` → Relative to root `<html>` font-size.
* `%` → Relative to parent font-size.
* `vw` → Relative to viewport width.

---

## 🛠 Tailwind CSS – Font Size Examples

```html
<h1 class="text-4xl font-bold">Heading</h1>
<p class="text-base">Normal Paragraph</p>
<p class="text-lg italic">Large Italic Text</p>
<p class="text-sm text-gray-600">Small Gray Text</p>
```

---

## 🌐 Google Fonts Example

```html
<head>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto">
</head>
<body style="font-family: 'Roboto', sans-serif;">
  <p>Hello with Roboto! 🖱</p>
</body>
```

### Tailwind Custom Google Font

```js
// tailwind.config.js
theme: {
  extend: {
    fontFamily: {
      roboto: ["Roboto", "sans-serif"],
    },
  },
}
```

Usage:

```html
<p class="font-roboto">Text in Roboto 🖋</p>
```

---

## ❓ Interview Questions & Answers ✋

### Q1: What is the difference between Serif and Sans-serif fonts?

🖐 **Answer:**

* ✅ Serif fonts have small strokes at edges (formal, traditional).
* ✅ Sans-serif fonts have clean lines (modern, minimal).

### Q2: What are Web Safe Fonts?

🖐 **Answer:**

* ✅ Fonts installed across most devices/browsers (e.g., Arial, Times New Roman).
* ✅ Ensures **consistency across platforms**.

### Q3: Difference between `em` and `rem`?

🖐 **Answer:**

* ✅ `em` → Relative to parent element font-size.
* ✅ `rem` → Relative to root `<html>` font-size.

### Q4: What is the `font` shorthand property?

🖐 **Answer:**

* ✅ Combine multiple font properties in **one declaration**.

```css
p {
  font: italic bold 16px Arial, sans-serif;
}
```

### Q5: How do you use custom fonts in CSS?

🖐 **Answer:**

* ✅ Use **@font-face** or **Google Fonts**.
* ✅ Always provide **fallback fonts**.

---

## 📚 Font Pairing Rules

1. 🎯 **Complement:** Fonts should harmonize, not clash.
2. 🖋 **Use Superfamilies:** Fonts designed to work together (e.g., Lucida Sans & Lucida Serif).
3. ⚡ **Contrast is King:** Use serif + sans-serif for balance.
4. 👑 **Choose One Boss:** One font dominates headings, another for body text.

---

## 💡 Popular Google Font Pairings

| Heading Font  | Body Font         |
| ------------- | ----------------- |
| Merriweather  | Open Sans         |
| Ubuntu        | Lora              |
| Abril Fatface | Poppins           |
| Cinzel        | Fauna One         |
| Fjalla One    | Libre Baskerville |
| Space Mono    | Muli              |
| Spectral      | Rubik             |
| Oswald        | Noto Sans         |

---

✅ **Fonts in CSS made simple, readable, and visually appealing.** 🎨
