# 🎨 CSS Clip-path — Shapes Explained (with Tailwind Examples)

Create **custom non-rectangular layouts** using `clip-path` in CSS — from simple circles to complex polygons and SVG paths.

---

## 🧩 What is `clip-path`?

`clip-path` lets you **mask or cut** specific parts of an element, defining which region remains visible.
The rest becomes **transparent or hidden** — like cutting shapes out of paper. ✂️

---

## 🔵 1. Circle Shape

### 📘 Syntax

```css
clip-path: circle(radius at x-position y-position);
```

### 🧠 Explanation

| Part                       | Meaning                                            |
| -------------------------- | -------------------------------------------------- |
| `radius`                   | How big the circle is (e.g., `50%`, `100px`)       |
| `at x-position y-position` | Where the circle’s center is (X and Y coordinates) |

### 💻 Example

```css
.element {
  width: 200px;
  height: 200px;
  background: coral;
  clip-path: circle(50% at 50% 50%);
}
```

🎯 Circle centered in the middle of the box with 50% radius.

### 🪄 Tailwind CSS

```html
<div class="w-48 h-48 bg-orange-400 [clip-path:circle(50%_at_50%_50%)]"></div>
```

---

## 🟣 2. Ellipse Shape

### 📘 Syntax

```css
clip-path: ellipse(x-radius y-radius at x-position y-position);
```

### 🧠 Explanation

| Part       | Meaning                   |
| ---------- | ------------------------- |
| `x-radius` | Horizontal radius (width) |
| `y-radius` | Vertical radius (height)  |
| `at x y`   | Center of ellipse         |

### 💻 Example

```css
.element {
  width: 300px;
  height: 200px;
  background: violet;
  clip-path: ellipse(50% 30% at 50% 50%);
}
```

🎨 Creates an oval in the middle.

### 🪄 Tailwind CSS

```html
<div class="w-72 h-48 bg-purple-400 [clip-path:ellipse(50%_30%_at_50%_50%)]"></div>
```

---

## 🔷 3. Polygon Shape

### 📘 Syntax

```css
clip-path: polygon(x1 y1, x2 y2, x3 y3, ...);
```

### 🧠 Explanation

Each pair `(x, y)` defines a **point (vertex)** in the clipping path.

* `x` → horizontal position (0% = left, 100% = right)
* `y` → vertical position (0% = top, 100% = bottom)

The browser **connects these points** in order to form the shape.

### 📊 Example Coordinates (for a rectangle)

| Point   | Coordinates | Position            |
| ------- | ----------- | ------------------- |
| (x₁ y₁) | `0 0`       | Top-left corner     |
| (x₂ y₂) | `100% 0`    | Top-right corner    |
| (x₃ y₃) | `100% 100%` | Bottom-right corner |
| (x₄ y₄) | `0 100%`    | Bottom-left corner  |

### 💻 Example 1 – Rectangle

```css
clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
```

### 💻 Example 2 – Triangle

```css
clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
```

### 💻 Example 3 – Diamond

```css
clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0 50%);
```

### 🧱 Diagram

```
Diamond (polygon points)
       (50% 0%)
          ▲
(0 50%) ◀   ▶ (100% 50%)
          ▼
       (50% 100%)
```

### 🪄 Tailwind CSS

```html
<!-- Rectangle -->
<div class="w-64 h-64 bg-sky-400 [clip-path:polygon(0_0,100%_0,100%_100%,0_100%)]"></div>

<!-- Triangle -->
<div class="w-64 h-64 bg-blue-500 [clip-path:polygon(50%_0%,0%_100%,100%_100%)]"></div>

<!-- Diamond -->
<div class="w-64 h-64 bg-indigo-400 [clip-path:polygon(50%_0%,100%_50%,50%_100%,0_50%)]"></div>
```

💡 You can create **any geometric shape** by adjusting point coordinates.

---

## 🟥 4. Inset Shape

### 📘 Syntax

```css
clip-path: inset(top right bottom left);
```

### 🧠 Explanation

| Value    | Meaning                      |
| -------- | ---------------------------- |
| `top`    | How much to cut from the top |
| `right`  | Cut from right side          |
| `bottom` | Cut from bottom              |
| `left`   | Cut from left                |

### 💻 Example

```css
.element {
  width: 300px;
  height: 200px;
  background: tomato;
  clip-path: inset(10px 20px 30px 40px);
}
```

🧱 Cuts the box inward from all sides.

### 🪄 Tailwind CSS

```html
<div class="w-72 h-48 bg-red-400 [clip-path:inset(10px_20px_30px_40px)]"></div>
```

---

## 🟡 5. Path (SVG) Shape

### 📘 Syntax

```css
clip-path: path('SVG path data');
```

### 💻 Example

```css
.element {
  width: 200px;
  height: 200px;
  background: gold;
  clip-path: path('M10 10 h80 v80 h-80 Z');
}
```

### 🧠 Explanation (SVG Commands)

| Command  | Meaning                     |
| -------- | --------------------------- |
| `M10 10` | Move to (10,10)             |
| `h80`    | Draw line horizontally 80px |
| `v80`    | Draw line vertically 80px   |
| `h-80`   | Move left 80px              |
| `Z`      | Close the path              |

🧩 Creates a square with SVG vector logic.

### 🪄 Tailwind CSS

```html
<div class="w-48 h-48 bg-yellow-400 [clip-path:path('M10_10_h80_v80_h-80_Z')]"></div>
```

---

## 🧠 Summary Table

| 🔖 Shape       | 🧩 Syntax                       | 💡 Description                     | 🪄 Tailwind Example                       |
| -------------- | ------------------------------- | ---------------------------------- | ----------------------------------------- |
| 🔵 **Circle**  | `circle(50% at 50% 50%)`        | Round shape centered               | `[clip-path:circle(50%_at_50%_50%)]`      |
| 🟣 **Ellipse** | `ellipse(50% 30% at 50% 50%)`   | Oval-like shape                    | `[clip-path:ellipse(50%_30%_at_50%_50%)]` |
| 🔷 **Polygon** | `polygon(x₁ y₁, x₂ y₂, …)`      | Custom points joined to form shape | `[clip-path:polygon(…)]`                  |
| 🟥 **Inset**   | `inset(10px 20px 30px 40px)`    | Cuts inward from edges             | `[clip-path:inset(10px_20px_30px_40px)]`  |
| 🟡 **Path**    | `path('M10 10 h80 v80 h-80 Z')` | Uses SVG path data                 | `[clip-path:path('…')]`                   |

---

## 🧭 Visual Shape Icons

```
🔵 Circle   → ○
🟣 Ellipse  → ◉
🔷 Polygon  → △ / ⬡ / ◇
🟥 Inset    → ☐
🟡 Path     → Custom Vector ✏️
```

---

## 💡 Pro Tips

✨ Use [Clippy](https://bennettfeely.com/clippy/) — a visual generator for `clip-path`.
🎨 Combine `clip-path` with gradients or animations for hero sections.
⚡ In **Tailwind CSS**, always use the **arbitrary value syntax**: `[clip-path:…]`.

---

**📘 Author:** Ramesh
**💡 Topic:** CSS Clip-path Shapes Explained — with Tailwind CSS Examples
**🕹️ Level:** Beginner → Advanced
