# 🎨 Tailwind CSS Animations Demo – Beginner to Advanced

---

## 📌 What are CSS Animations?

CSS Animations allow smooth transitions of element properties over time using `@keyframes`.
They can change colors, move elements, fade, scale, or rotate without JavaScript.

Tailwind CSS supports animations via **custom utilities** and `@layer utilities`.

---

## 📝 Basic Syntax

```css
selector {
  animation-name: myAnimation;
  animation-duration: 4s;
  animation-delay: 2s;
  animation-iteration-count: 3;
  animation-direction: alternate;
  animation-timing-function: ease;
  animation-fill-mode: forwards;
}
```

### ✅ Shorthand Example

```css
animation: myAnimation 5s linear 2s infinite alternate;
```

---

## 🔑 Key Concepts

* **Simple Color Change**: from red → yellow.
* **Multiple Colors with Percentages**: 0%, 25%, 50%, 100%.
* **Movement (Square Path)**: top-left → top-right → bottom-right → bottom-left → top-left.
* **Animation Delay**: delays start time.
* **Negative Delay**: starts animation mid-way.
* **Iteration Count**: `infinite` loops animation.
* **Animation Direction**: `alternate` or `alternate-reverse`.
* **Timing Functions**: `linear`, `ease`, `ease-in`, `ease-out`, `ease-in-out`.
* **Shorthand Property**: combine all animation properties.

---

## 🔑 Examples

### 1️⃣ Square Path Animation

```css
@keyframes squarePath {
  0%   {background-color:red; left:0px; top:0px;}
  25%  {background-color:yellow; left:200px; top:0px;}
  50%  {background-color:blue; left:200px; top:200px;}
  75%  {background-color:green; left:0px; top:200px;}
  100% {background-color:red; left:0px; top:0px;}
}

.animate-squarePath { animation: squarePath 4s linear; }
.animate-squarePathDelay { animation: squarePath 4s linear 2s; }
.animate-squarePathNegDelay { animation: squarePath 4s linear -2s; }
.animate-squarePathInfinite { animation: squarePath 4s linear infinite; }
.animate-fillBoth { animation: squarePath 4s linear both; }
.animate-altReverse { animation: squarePath 4s linear infinite alternate-reverse; }
.animate-shorthand { animation: squarePath 5s linear 2s infinite alternate; }
```

### 2️⃣ Timing Functions Demo

```css
@keyframes moveLeft {
  from { left: 0px; }
  to   { left: 300px; }
}

.animate-linear    { animation: moveLeft 5s linear; }
.animate-ease      { animation: moveLeft 5s ease; }
.animate-easeIn    { animation: moveLeft 5s ease-in; }
.animate-easeOut   { animation: moveLeft 5s ease-out; }
.animate-easeInOut { animation: moveLeft 5s ease-in-out; }
```

---

## 🖼️ Square Path Diagram

```
(0,0) ───────────────► (200,0)
 🔴 Red Start          🟡 Yellow
   Top-Left              Top-Right

       ▲
       │
       │
       ▼

(0,200) ◄────────────── (200,200)
 🟢 Green                🔵 Blue
 Bottom-Left             Bottom-Right
```

### ✅ Explanation

0% → Top-Left (Red)
25% → Top-Right (Yellow)
50% → Bottom-Right (Blue)
75% → Bottom-Left (Green)
100% → Back to Top-Left (Red)

---

## 📌 Tailwind CSS Equivalent

Tailwind allows custom keyframes in `@layer utilities` or `tailwind.config.js`.

Example:

```html
<div class="w-24 h-24 relative animate-squarePath"></div>
<div class="w-24 h-12 bg-red-500 relative animate-linear mt-2"></div>
```

---

## ✋ Interview Q&A

❓ **Q1: Difference between transition and animation?**
👉 Transition needs a trigger; animation runs automatically.

❓ **Q2: What is animation-fill-mode?**
👉 Defines element appearance before & after animation.

❓ **Q3: What does animation-iteration-count: infinite; mean?**
👉 Repeats animation forever ♾️.

❓ **Q4: What is animation-direction: alternate?**
👉 Plays forward then backward 🔄.

❓ **Q5: Can Tailwind handle keyframes?**
👉 Yes ✅, via `@layer utilities` or `tailwind.config.js`.
