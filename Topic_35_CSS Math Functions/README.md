# 🧮 CSS Math Functions

CSS math functions allow **mathematical expressions** to be used as property values.  
The main functions are:

1. `calc()` – perform calculations  
2. `max()` – take the largest value  
3. `min()` – take the smallest value  
4. `clamp()` – set a value between min and max  

---

## 📘 1️⃣ CSS `calc()` Function

The **`calc()`** function performs a mathematical calculation for a CSS property.  

- Supports: `+`, `-`, `*`, `/`  
- Can **combine different units** like `%`, `px`, `vh`, etc.

**Syntax:**

```css
calc(expression)
```

**Example – Using calc() to set width and height:**

```css
#div1 {
  margin: auto;
  width: calc(100% - 100px);
  height: calc(30vh + 50px);
  border: 1px solid black;
  padding: 10px;
}
```

📊 **Diagram:**  
```
Viewport width = 100%
  └─ div width = 100% - 100px
Viewport height = 30vh + 50px
```

---

## 📘 2️⃣ CSS `max()` Function

The `max()` function selects the largest value from a list of values.

**Syntax:**

```css
max(value1, value2, ...)
```

**Example – Width is largest of 50% or 300px:**

```css
#div1 {
  height: 100px;
  width: max(50%, 300px);
  border: 1px solid black;
  padding: 10px;
}
```

📊 **Diagram:**  
```
width = max(50%, 300px)
  ├─ If 50% < 300px → width = 300px
  └─ If 50% > 300px → width = 50%
```

---

## 📘 3️⃣ CSS `min()` Function

The `min()` function selects the smallest value from a list of values.

**Syntax:**

```css
min(value1, value2, ...)
```

**Example – Width is smallest of 50% or 300px:**

```css
#div1 {
  height: 100px;
  width: min(50%, 300px);
  border: 1px solid black;
  padding: 10px;
}
```

📊 **Diagram:**  
```
width = min(50%, 300px)
  ├─ If 50% < 300px → width = 50%
  └─ If 50% > 300px → width = 300px
```

---

## 📘 4️⃣ CSS `clamp()` Function

The `clamp()` function sets a value responsive between min and max based on viewport size.

**Syntax:**

```css
clamp(min, preferred, max)
```

- **min** – smallest allowed value  
- **preferred** – preferred value  
- **max** – largest allowed value  

**Example – Font-size for responsive text:**

```css
h2 {
  font-size: clamp(2rem, 2.5vw, 3.5rem);
}

p {
  font-size: clamp(1rem, 2.5vw, 2.5rem);
}
```

📊 **Diagram:**  
```
h2 font-size:
  min = 2rem
  preferred = 2.5vw (scales with viewport)
  max = 3.5rem

p font-size:
  min = 1rem
  preferred = 2.5vw
  max = 2.5rem
```

---

## ✨ Tailwind CSS Equivalents

Tailwind doesn’t have direct math functions, but you can achieve similar results using responsive utilities:

| CSS                           | Tailwind                       |
|--------------------------------|--------------------------------|
| `width: calc(100% - 100px)`    | `w-[calc(100%-100px)]`         |
| `width: max(50%, 300px)`       | `w-[max(50%,300px)]`           |
| `width: min(50%, 300px)`       | `w-[min(50%,300px)]`           |
| `font-size: clamp(...)`        | `text-[clamp(1rem,2.5vw,2.5rem)]` |

**Example:**

```html
<div class="w-[calc(100%-100px)] h-[calc(30vh+50px)] border p-2">
  Responsive Box
</div>

<h2 class="text-[clamp(2rem,2.5vw,3.5rem)]">Responsive Heading</h2>
<p class="text-[clamp(1rem,2.5vw,2.5rem)]">Responsive paragraph</p>
```

---

## ✋ Interview Q&A

**🙋 Q1: What is calc() in CSS?**  
👉 A1: A function to perform calculations for property values, supports +, -, *, /.  

**🙋 Q2: Difference between min() and max()?**  
👉 A2: `min()` chooses the smallest value, `max()` chooses the largest value from a list.  

**🙋 Q3: What does clamp() do?**  
👉 A3: Sets a value between a minimum and maximum, responsive to viewport size.  

**🙋 Q4: Can calc() mix units like % and px?**  
👉 A4: ✅ Yes, that’s one of its main advantages.  

**🙋 Q5: How to use these in Tailwind CSS?**  
👉 A5: Use arbitrary values with square brackets, e.g., `w-[calc(100%-100px)]`, `text-[clamp(1rem,2.5vw,2.5rem)]`.  

---

## ✅ Best Practices

- Use `calc()` for precise, combined-unit layouts.  
- Use `min()` / `max()` / `clamp()` for responsive sizing.  
- Prefer `clamp()` for font-sizes to maintain readability on different screen sizes.  
