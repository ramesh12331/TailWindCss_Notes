# 🌙 CSS Dark Mode & Theming Guide

Learn how to create beautiful **light and dark themes** using **CSS variables**, **media queries**, and **Tailwind CSS** utilities.

---

## 🧩 1. CSS Variables (Custom Properties)

### 📘 Definition:
CSS variables (custom properties) let you store values (like colors) and reuse them across your styles. Perfect for **theming**.

### 💻 Syntax:
```css
:root {
  --bg-color: #ffffff;
  --text-color: #000000;
}

body {
  background-color: var(--bg-color);
  color: var(--text-color);
}
```

### 🧠 Explanation:
- `:root` → global scope for variables (applies to the whole document).
- `--bg-color`, `--text-color` → custom property names.
- `var(--bg-color)` → retrieves the stored value.

### 🌗 Example: Theme Switch
```css
:root {
  --bg-color: #ffffff;
  --text-color: #000000;
}

body.dark-mode {
  --bg-color: #121212;
  --text-color: #ffffff;
}

body {
  background-color: var(--bg-color);
  color: var(--text-color);
}
```

✅ **Summary:**
Use CSS variables for dynamic theme updates. Toggle class `dark-mode` to switch instantly.

---

## 🌓 2. Prefers-Color-Scheme (System Dark Mode)

### 📘 Definition:
A **CSS media query** that detects the user's system theme preference (light or dark).

### 💻 Syntax:
```css
@media (prefers-color-scheme: dark) {
  body {
    background-color: #121212;
    color: #ffffff;
  }
}

@media (prefers-color-scheme: light) {
  body {
    background-color: #ffffff;
    color: #000000;
  }
}
```

### 🧠 Explanation:
- Automatically adapts based on OS or browser settings.
- No JavaScript required for detection.

✅ **Summary:**
Use `prefers-color-scheme` for **automatic dark mode detection** based on user preference.

---

## 🎨 3. Tailwind CSS Dark Mode

### 📘 Definition:
Tailwind provides built-in dark mode support using the `dark:` variant.

### ⚙️ Configuration (`tailwind.config.js`)
```js
module.exports = {
  darkMode: 'class', // or 'media'
}
```

### 💻 Example:
```html
<div class="bg-white text-black dark:bg-gray-900 dark:text-white p-4 rounded-lg">
  <h2 class="text-xl font-bold">🌙 Dark Mode Enabled</h2>
  <p>Switch your system theme or toggle the dark class!</p>
</div>
```

### 🌗 Tailwind Explanation:
- `darkMode: 'class'` → enables dark mode when `.dark` class is added to `<html>` or `<body>`.
- `dark:bg-gray-900` → applies only in dark mode.

✅ **Summary:**
Easily implement theme switching in Tailwind using **dark mode variants** and a single toggle class.

---

## 🧠 4. Example: Light & Dark Theme Toggle (Combined)

### 🌈 HTML + CSS
```html
<button id="toggleTheme">🌓 Toggle Theme</button>
<div class="container">
  <h1>Welcome to Theme World</h1>
</div>
```

```css
:root {
  --bg: #fff;
  --text: #000;
}

body {
  background: var(--bg);
  color: var(--text);
  transition: 0.3s;
}

body.dark-mode {
  --bg: #121212;
  --text: #fff;
}
```

```js
document.getElementById("toggleTheme").onclick = () => {
  document.body.classList.toggle("dark-mode");
};
```

✅ **Summary:**
Combine **CSS variables** with a **JavaScript toggle** for interactive light/dark mode switching.

---

## 🪄 5. Tailwind Example – Glassmorphic Dark Card

```html
<div class="backdrop-blur-md bg-white/30 dark:bg-gray-800/30 p-6 rounded-2xl shadow-lg">
  <h3 class="text-2xl font-semibold text-gray-800 dark:text-gray-100">✨ Glassmorphic Card</h3>
  <p class="text-gray-600 dark:text-gray-300">Adapts to your system theme automatically!</p>
</div>
```

✅ **Summary:**
Use **opacity**, **backdrop filters**, and **dark variants** to make modern theme designs in Tailwind.

---

## 🧾 Final Summary

| Concept | Description | Example |
|----------|--------------|----------|
| 🧩 CSS Variables | Define reusable theme values | `--bg-color: #fff;` |
| 🌗 Prefers-Color-Scheme | Auto-detect user theme | `@media (prefers-color-scheme: dark)` |
| 🎨 Tailwind Dark Mode | Class-based theming | `dark:bg-gray-900` |
| ⚡ Combined Toggle | Manual + system mode | JS toggle with `.dark-mode` |
| 💎 Glassmorphism | Style enhancement | `backdrop-blur-md bg-white/30` |

---

### 🏁 Conclusion:
✅ **CSS variables** make themes flexible.  
✅ **Prefers-color-scheme** enables system-driven theming.  
✅ **Tailwind’s dark mode** simplifies responsive theme styling.  
✅ Combine all three for a **complete theming experience**.

---

### 🧠 Bonus Tip:
You can use **localStorage** to remember theme choice:
```js
const theme = localStorage.getItem('theme');
if (theme === 'dark') document.documentElement.classList.add('dark');
```
