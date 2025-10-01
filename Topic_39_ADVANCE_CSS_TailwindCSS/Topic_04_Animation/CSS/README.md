# 🎨 CSS Animations – Beginner to Advanced

---

## 📌 What is CSS Animation?

CSS **Animations** allow you to smoothly change CSS properties over time using `@keyframes`.
Unlike **transitions** (which need a trigger like hover), animations can run automatically, loop infinitely, and follow custom paths.

Animations can:

* Move elements 🚶
* Change colors 🎨
* Fade in/out 👻
* Rotate/scale 🔄

---

## 📝 Basic Syntax

```css
selector {
  animation-name: myAnimation;      /* Keyframe name */
  animation-duration: 4s;           /* How long it runs */
  animation-delay: 2s;              /* Delay before start */
  animation-iteration-count: 3;     /* Number of repeats */
  animation-direction: alternate;   /* Normal, reverse, alternate */
  animation-timing-function: ease;  /* Speed curve */
  animation-fill-mode: forwards;    /* Retain end state */
}
```

👉 **Shorthand Example**

```css
animation: myAnimation 5s linear 2s infinite alternate;
```

---

## 🔑 Key Properties

| Property                    | Meaning                                               |
| --------------------------- | ----------------------------------------------------- |
| `animation-name`            | Name of keyframes to use                              |
| `animation-duration`        | Time the animation takes                              |
| `animation-delay`           | Delay before starting                                 |
| `animation-iteration-count` | Number of loops (`1`, `infinite`)                     |
| `animation-direction`       | `normal`, `reverse`, `alternate`, `alternate-reverse` |
| `animation-timing-function` | Speed curve (`ease`, `linear`, `ease-in`, etc.)       |
| `animation-fill-mode`       | How element behaves before/after animation            |

---

## 🎬 Examples

### 🔑 Example 1 – Color Change

```css
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: myAnimation;
  animation-duration: 4s;
}

@keyframes myAnimation {
  from { background-color: red; }
  to   { background-color: yellow; }
}
```

➡️ Smoothly changes **Red → Yellow** in 4s.

---

### 🔑 Example 2 – Multiple Colors

```css
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: myAnimation;
  animation-duration: 4s;
}

@keyframes myAnimation {
  0%   { background-color: red; }
  25%  { background-color: yellow; }
  50%  { background-color: blue; }
  100% { background-color: green; }
}
```

➡️ Changes **Red → Yellow → Blue → Green**.

---

### 🔑 Example 3 – Moving Box (Square Path)

```css
div {
  width: 100px;
  height: 100px;
  background-color: red;
  position: relative;
  animation: myAnimation 5s linear infinite;
}

@keyframes myAnimation {
  0%   { background-color: red;   left: 0px;   top: 0px; }
  25%  { background-color: yellow; left: 200px; top: 0px; }
  50%  { background-color: blue;   left: 200px; top: 200px; }
  75%  { background-color: green;  left: 0px;   top: 200px; }
  100% { background-color: red;    left: 0px;   top: 0px; }
}
```

---

## 🖼️ Neat Diagram (Square Path)

```
(0,0) ───────────────► (200,0)
 🔴 Start (Red)        🟡 Yellow
   Top-Left              Top-Right

       ▲
       │
       │
       ▼

(0,200) ◄────────────── (200,200)
 🟢 Green                🔵 Blue
 Bottom-Left             Bottom-Right
```

---

## 🔎 Explanation of the Diagram

1. **Start Point – (0,0) → Top-Left Corner**

   * Position: `left: 0px; top: 0px;`
   * Color: 🔴 **Red**

2. **Move Right – (200,0) → Top-Right Corner**

   * Position: `left: 200px; top: 0px;`
   * Color: 🟡 **Yellow**

3. **Move Down – (200,200) → Bottom-Right Corner**

   * Position: `left: 200px; top: 200px;`
   * Color: 🔵 **Blue**

4. **Move Left – (0,200) → Bottom-Left Corner**

   * Position: `left: 0px; top: 200px;`
   * Color: 🟢 **Green**

5. **Return to Start – Back to (0,0)**

   * Position: `left: 0px; top: 0px;`
   * Color: 🔴 **Red**

---

## 📌 Final Summary

✅ CSS animations allow elements to **move, change color, fade, or scale** automatically.
✅ Each keyframe percentage represents a **specific moment in time**.
✅ Diagrams help **visualize paths** like the square movement example.
✅ Tailwind can handle custom animations via `extend.keyframes` in `tailwind.config.js`.
✅ Using animation properties (`duration`, `delay`, `iteration-count`, `direction`, `timing-function`, `fill-mode`) allows full **control over the animation flow**.

---

## 🎯 Tailwind CSS Example

```js
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      keyframes: {
        myAnimation: {
          '0%':   { backgroundColor: 'red', left: '0px', top: '0px' },
          '25%':  { backgroundColor: 'yellow', left: '200px', top: '0px' },
          '50%':  { backgroundColor: 'blue', left: '200px', top: '200px' },
          '75%':  { backgroundColor: 'green', left: '0px', top: '200px' },
          '100%': { backgroundColor: 'red', left: '0px', top: '0px' },
        },
      },
      animation: {
        myAnimation: 'myAnimation 5s linear infinite',
      },
    },
  },
};
```

HTML Usage:

```html
<div class="w-24 h-24 bg-red-500 relative animate-myAnimation"></div>
```

---

## ✋ Interview Q&A

❓ **Q1: Transition vs Animation?**
👉 Transition needs a trigger; animation can run automatically.

❓ **Q2: What is animation-fill-mode?**
👉 Defines how element looks before & after animation.

❓ **Q3: What does animation-iteration-count: infinite; mean?**
👉 Animation repeats forever ♾️.

❓ **Q4: What is animation-direction: alternate?**
👉 Plays forward then backward 🔄.

❓ **Q5: Can Tailwind support custom keyframes?**
👉 Yes ✅, via `tailwind.config.js → extend.keyframes`.
