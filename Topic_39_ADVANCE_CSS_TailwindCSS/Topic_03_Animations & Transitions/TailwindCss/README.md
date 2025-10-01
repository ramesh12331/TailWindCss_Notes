# 🎨 Tailwind CSS Transitions – Complete Guide

---

## 📌 What is CSS Transition?

CSS Transitions let you change CSS property values smoothly over time instead of instantly. They can animate properties like width, height, background-color, and transform without JavaScript.

---

## 📝 Basic Syntax

```css
selector {
  transition-property: width;           /* Property to animate */
  transition-duration: 2s;             /* Animation duration */
  transition-timing-function: linear;  /* Speed curve */
  transition-delay: 1s;                /* Delay before start */
}

/* Shorthand */
selector {
  transition: width 2s linear 1s;
}
```

---

## 🔑 Examples

### 1. Simple Width Transition with Delay

```html
<div class="w-24 h-24 bg-red-500 relative transition-width-delay hover:w-72"></div>
```

* Width changes from 6rem → 18rem after 3s delay.

### 2. Multiple Property Transition

```html
<div class="w-24 h-24 bg-red-500 relative transition-multi hover:w-72 hover:h-72 hover:bg-orange-500"></div>
```

* Animates width, height, and background-color simultaneously.

### 3. Transition + Transform

```html
<div class="w-24 h-24 bg-red-500 relative transition-transform-multi hover:w-72 hover:h-72 hover:bg-orange-500 hover:rotate-180"></div>
```

* Rotates the box while resizing and changing color.

### 4. Button Hover Transition

```html
<button class="bg-gray-300 px-4 py-2 rounded transition-colors transition-transform duration-[1000ms] ease-out hover:bg-green-300 hover:scale-110">Hover Me</button>
```

* Smooth color and scaling effect on hover.

### 5. Width Transition with Different Timing Functions

```html
<div class="w-24 h-24 bg-red-500 relative transition-linear hover:w-72 mt-4"></div>
<div class="w-24 h-24 bg-red-500 relative transition-ease hover:w-72 mt-2"></div>
<div class="w-24 h-24 bg-red-500 relative transition-ease-in hover:w-72 mt-2"></div>
<div class="w-24 h-24 bg-red-500 relative transition-ease-out hover:w-72 mt-2"></div>
<div class="w-24 h-24 bg-red-500 relative transition-ease-in-out hover:w-72 mt-2"></div>
```

* Demonstrates linear, ease, ease-in, ease-out, ease-in-out curves.

---

## 🔹 Tailwind Utility Explanation

| Original CSS                                         | Tailwind Equivalent                            |
| ---------------------------------------------------- | ---------------------------------------------- |
| transition: width 2s                                 | .transition-width duration-[2000ms]            |
| transition-delay: 3s                                 | .transition-width-delay                        |
| transition: width 2s, height 4s, background-color 3s | .transition-multi                              |
| transform: rotate(180deg)                            | hover:rotate-180 + .transition-transform-multi |
| transition-timing-function: linear                   | .transition-linear                             |
| transition-timing-function: ease                     | .transition-ease                               |
| transition-timing-function: ease-in                  | .transition-ease-in                            |
| transition-timing-function: ease-out                 | .transition-ease-out                           |
| transition-timing-function: ease-in-out              | .transition-ease-in-out                        |
| hover:width/height/background-color                  | hover:w-72 hover:h-72 hover:bg-orange-500      |

---

## ✋ Interview Q&A

❓ **Q1: Difference between transition and animation?**
👉 Transition needs a trigger (like hover); animation can run automatically.

❓ **Q2: Can we transition multiple properties?**
👉 Yes, separate them with commas or use Tailwind utility classes.

❓ **Q3: What is transition-timing-function?**
👉 Defines the speed curve: linear, ease, ease-in, ease-out, ease-in-out.

❓ **Q4: How does transition-delay work?**
👉 Specifies time to wait before the transition starts.

❓ **Q5: Can Tailwind handle transitions?**
👉 Yes, using utility classes like `transition-all`, `transition-colors`, `transition-transform`.

---

## 📝 Summary

* **CSS Transitions** create smooth property changes.
* **Trigger** transitions via pseudo-classes like `:hover`.
* **Multiple properties** can be transitioned together.
* **Timing functions** control animation curve.
* **Delay** schedules start time.
* **Transform** allows scaling, rotation, and movement.
* **Tailwind CSS** provides simple utility classes for all common transitions.
