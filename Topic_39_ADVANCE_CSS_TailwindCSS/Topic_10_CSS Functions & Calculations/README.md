# 🧮 CSS Functions & Calculations

Learn how to perform **dynamic calculations and responsive sizing** in CSS using `calc()`, `clamp()`, `min()`, and `max()`.  
Combine these with **Tailwind CSS** for modern responsive design.

---

## 🔹 1. calc() Function

### 📘 Definition:
`calc()` allows you to perform mathematical operations directly in CSS for properties like width, height, margin, and font-size.

### 💻 Syntax:
```css
width: calc(100% - 50px);
height: calc(50vh - 20px);
```

### 🧠 Explanation:
- Can combine **%, px, em, rem, vw, vh** units.  
- Supports `+`, `-`, `*`, `/` operators (division limited to numbers, not units).  

### 💻 Example:
```css
.container {
  width: calc(100% - 40px);
  padding: 20px;
  background: #4f46e5;
  color: white;
}
```

### 🪄 Tailwind CSS Example:
```html
<div class="[width:calc(100%-2rem)] bg-indigo-600 text-white p-5">
  📐 calc() Example
</div>
```

✅ **Summary:** `calc()` is perfect for **dynamic spacing and responsive adjustments**.

---

## 🔹 2. clamp() Function

### 📘 Definition:
`clamp()` sets a **value with a minimum, preferred, and maximum** limit. Great for responsive sizing.

### 💻 Syntax:
```css
font-size: clamp(min, preferred, max);
```

### 🧠 Explanation:
- **min** → smallest value allowed  
- **preferred** → ideal value (often relative unit like `vw`)  
- **max** → largest value allowed  

### 💻 Example:
```css
h1 {
  font-size: clamp(16px, 2vw, 32px);
}
```

### 🪄 Tailwind CSS Example:
```html
<h1 class="[font-size:clamp(1rem,2vw,2rem)] font-bold text-indigo-700">
  🔠 clamp() Example
</h1>
```

✅ **Summary:** `clamp()` ensures responsive yet controlled font or element sizes.

---

## 🔹 3. min() Function

### 📘 Definition:
`min()` returns the **smaller value** among two or more.

### 💻 Syntax:
```css
width: min(50%, 300px);
height: min(10vh, 100px);
```

### 🧠 Explanation:
- Compares multiple values and uses the **minimum one**.  
- Useful for **responsive widths, heights, or scaling**.

### 💻 Example:
```css
.box {
  width: min(80%, 400px);
  background: #f97316;
  padding: 20px;
  color: white;
}
```

### 🪄 Tailwind CSS Example:
```html
<div class="[width:min(80%,400px)] bg-orange-500 text-white p-5">
  📏 min() Example
</div>
```

✅ **Summary:** `min()` helps maintain **maximum control over responsive sizes**.

---

## 🔹 4. max() Function

### 📘 Definition:
`max()` returns the **larger value** among two or more.

### 💻 Syntax:
```css
width: max(200px, 50%);
height: max(100px, 10vh);
```

### 🧠 Explanation:
- Compares values and uses the **maximum one**.  
- Ensures elements **don’t shrink below a certain size**.

### 💻 Example:
```css
.box {
  width: max(300px, 50%);
  background: #22c55e;
  padding: 20px;
  color: white;
}
```

### 🪄 Tailwind CSS Example:
```html
<div class="[width:max(300px,50%)] bg-green-500 text-white p-5">
  📏 max() Example
</div>
```

✅ **Summary:** `max()` is perfect for **maintaining minimum sizing for responsiveness**.

---

## 🔹 5. Combining Functions

### 💻 Example:
```css
.container {
  width: clamp(200px, 50%, 600px);
  padding: calc(1rem + 2vw);
  height: min(max(300px, 50%), 500px);
}
```

### 🪄 Tailwind CSS Example:
```html
<div class="[width:clamp(200px,50%,600px)] [padding:calc(1rem+2vw)] [height:min(max(300px,50%),500px)] bg-indigo-600 text-white">
  ⚡ Combined CSS Functions Example
</div>
```

✅ **Summary:** Combining these functions gives **full control over responsive design**.

---

## 🧾 6. Quick Reference Table

| 🔖 Function | 🧩 Syntax | 💡 Description | 🪄 Tailwind Example |
|-------------|-----------|----------------|------------------|
| `calc()`    | `calc(100% - 50px)` | Perform math on sizes | `[width:calc(100%-2rem)]` |
| `clamp()`   | `clamp(16px,2vw,32px)` | Min, preferred, max | `[font-size:clamp(1rem,2vw,2rem)]` |
| `min()`     | `min(50%,300px)` | Choose smallest value | `[width:min(80%,400px)]` |
| `max()`     | `max(200px,50%)` | Choose largest value | `[width:max(300px,50%)]` |

---

## 🧠 Pro Tips

- Use `calc()` for **spacing, margins, and combining units`.  
- Use `clamp()` for **responsive typography and element sizing**.  
- Use `min()` & `max()` for **adaptive, constraint-based sizing**.  
- Tailwind supports **arbitrary values** with `[ ]` notation for these CSS functions.

---

**📘 Author:** Ramesh  
**💡 Topic:** CSS Functions & Calculations — `calc()`, `clamp()`, `min()`, `max()`  
**🕹️ Level:** Beginner → Advanced
