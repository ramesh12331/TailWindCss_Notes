# 🎨 CSS Transitions – Beginner to Advanced

---

## 📌 What is CSS Transition?

CSS Transitions allow property changes in CSS to happen smoothly over time instead of instantly.
You can animate properties like `width`, `height`, `background-color`, `transform`, etc., without JavaScript.

---

## 📝 Basic Syntax

```css
selector {
  transition-property: width;           /* Which property to animate */
  transition-duration: 2s;             /* How long it takes */
  transition-timing-function: linear;  /* Speed curve */
  transition-delay: 1s;                /* Wait before starting */
}

/* Shorthand */
selector {
  transition: width 2s linear 1s;
}
```

---

## 🔑 Key Concepts

1. **How to Trigger the Transition**
   Typically via pseudo-classes like `:hover`, `:focus`, `:active`.

2. **Change Multiple Property Values**

```css
.trans {
  transition: width 2s, height 4s, background-color 3s;
}
.trans:hover {
  width: 300px;
  height: 300px;
  background-color: orange;
}
```

3. **Transition Speed Curve (Timing Functions)**

```css
#div1 { transition-timing-function: linear; }
#div2 { transition-timing-function: ease; }
#div3 { transition-timing-function: ease-in; }
#div4 { transition-timing-function: ease-out; }
#div5 { transition-timing-function: ease-in-out; }
```

4. **Transition Delay**

```css
div {
  transition: width 2s linear 1s; /* delay = 1s */
}
```

5. **Transition + Transform**

```css
div:hover {
  transform: rotate(180deg);
}
button:hover {
  transform: scale(1.1);
}
```

---

## 🖼️ Diagram – Example: Width Change

```
Initial State: Width = 100px  ──── Hover ────> Width = 300px
 🔴 Red Box                          🟠 Orange Box
```

* Delay: Starts after 1s
* Duration: 2s
* Timing Function: Linear (constant speed)

---

## 🔑 Tailwind CSS Equivalents

Tailwind provides utility classes for transitions and transforms:

```html
<div class="w-24 h-24 bg-red-500 transition-all duration-2000 ease-linear hover:w-72 hover:bg-orange-500"></div>
<button class="transition-transform duration-1000 ease-out hover:scale-110 hover:bg-green-300">Hover Me</button>
```

* `transition-all` → transition all properties
* `duration-2000` → 2s duration (milliseconds)
* `ease-linear`, `ease-in`, `ease-out`, `ease-in-out` → timing functions
* `hover:w-72` → width change on hover
* `hover:bg-orange-500` → background-color change on hover
* `hover:scale-110` → transform scale on hover

---

## ✋ Interview Q&A

❓ **Q1: Difference between transition and animation?**
👉 Transition requires a trigger, animation can run automatically.

❓ **Q2: Can we transition multiple properties?**
👉 Yes, separate them with commas.

❓ **Q3: What is transition-timing-function?**
👉 Defines the speed curve of the transition (linear, ease, ease-in, etc.).

❓ **Q4: How does transition-delay work?**
👉 Waits specified time before the transition starts.

❓ **Q5: How to combine transition with transform?**
👉 Use `transition` on element and apply `transform` on hover.

---

## 📝 Summary

* **CSS Transitions** make property changes smooth and visually appealing.
* **Triggered by pseudo-classes** like `:hover` or `:focus`.
* **Multiple properties** can be transitioned together.
* **Timing functions** control speed and acceleration.
* **Delays** allow scheduling of animation.
* **Transform support** enables rotation, scaling, and movement.
* **Tailwind CSS** provides utility classes to implement transitions quickly and responsively.

This guide provides a complete beginner-to-advanced overview of CSS transitions, Tailwind equivalents, examples, diagrams, and interview Q&A.
