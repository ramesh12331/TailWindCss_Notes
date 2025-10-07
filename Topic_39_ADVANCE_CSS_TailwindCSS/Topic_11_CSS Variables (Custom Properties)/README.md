# 🎨 CSS Variables (Custom Properties)

Learn how to use **CSS Variables** (Custom Properties) for **reusable themes, consistent design, and easy maintenance**.

---

## 🔹 1. What are CSS Variables?

### 📘 Definition:
CSS Variables (Custom Properties) allow you to **store values** like colors, fonts, sizes, etc., and **reuse them across your styles**.

### 💻 Syntax:
```css
:root {
  --main-color: #ff0000; /* Define variable */
}

button {
  background-color: var(--main-color); /* Use variable */
}
```

🧠 **Explanation:**
- `:root` → global scope (applies to the whole document).  
- `--main-color` → variable name (must start with `--`).  
- `var(--main-color)` → retrieves the stored value.  
- Can define variables for **colors, fonts, spacing, sizes**.

---

## 🔹 2. Example – Themed Buttons

### 💻 CSS Example:
```css
:root {
  --primary-color: #4f46e5;
  --secondary-color: #f97316;
  --text-color: #ffffff;
}

button.primary {
  background-color: var(--primary-color);
  color: var(--text-color);
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
}

button.secondary {
  background-color: var(--secondary-color);
  color: var(--text-color);
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
}
```

### 🪄 Tailwind CSS Example (Using Arbitrary Values):
```html
<button class="[background-color:var(--primary-color)] text-white p-2 rounded">Primary Button</button>
<button class="[background-color:var(--secondary-color)] text-white p-2 rounded">Secondary Button</button>
```

✅ **Summary:**  
Variables make **theme management easier**, allowing consistent colors across multiple elements.

---

## 🔹 3. Example – Dynamic Theme Switch

### 💻 CSS:
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
  transition: 0.3s;
}
```

### 💻 HTML + JS Example:
```html
<button id="toggleTheme">🌗 Toggle Theme</button>
<p>Hello! This text will change color based on theme.</p>

<script>
  const toggleBtn = document.getElementById("toggleTheme");
  toggleBtn.addEventListener("click", () => {
    document.body.classList.toggle("dark-mode");
  });
</script>
```

### 🪄 Tailwind CSS Example:
```html
<div class="bg-white dark:bg-gray-900 text-black dark:text-white p-4 rounded">
  🌗 Tailwind Theme Example
</div>
```

✅ **Summary:**  
Combine CSS Variables with a **class toggle** to implement light/dark themes efficiently.

---

## 🔹 4. Advanced Example – Spacing & Fonts

### 💻 CSS:
```css
:root {
  --spacing: 1rem;
  --heading-font: 'Arial', sans-serif;
}

h1 {
  margin-bottom: var(--spacing);
  font-family: var(--heading-font);
  font-size: 2rem;
}
```

### 🪄 Tailwind CSS Example:
```html
<h1 class="[margin-bottom:var(--spacing)] [font-family:var(--heading-font)] text-2xl">
  Heading with Variable Spacing & Font
</h1>
```

✅ **Summary:**  
CSS variables can store **any property value**, making layout, typography, and spacing reusable.

---

## 🧾 Quick Reference Table

| 🔖 Concept | 🧩 Syntax | 💡 Description | 🪄 Tailwind Example |
|-------------|------------|----------------|----------------------|
| **Define variable** | `--main-color: #ff0000;` | Store reusable value | `[background-color:var(--main-color)]` |
| **Use variable** | `var(--main-color)` | Retrieve stored value | `[color:var(--main-color)]` |
| **Theming** | `.dark-mode { --bg: #121212; }` | Dynamic theme switching | `dark:[background-color:var(--bg)]` |
| **Fonts & Spacing** | `--spacing: 1rem;` | Reusable spacing & font | `[margin-bottom:var(--spacing)]` |

---

## 🧠 Pro Tips

- Store common **colors, fonts, and spacing** in `:root` for global use.  
- Combine with **class toggles** for dynamic themes.  
- Works with **any CSS property**, not just colors.  
- Use in **Tailwind CSS** via `[var(--variable-name)]` arbitrary values.

---

📘 **Author:** Ramesh  
💡 **Topic:** CSS Variables (Custom Properties)  
🕹️ **Level:** Beginner → Advanced
