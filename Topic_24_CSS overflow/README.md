# 📌 CSS Overflow Property – Complete Guide

The CSS `overflow` property controls **what happens to content that exceeds the size of its container**. It can **clip content, add scrollbars, or allow content to overflow**.

---

## 1. 🛠 Syntax

```css
selector {
  overflow: visible | hidden | scroll | auto;
}
```

* `visible` → Default, content is not clipped.
* `hidden` → Content is clipped.
* `scroll` → Scrollbars always appear.
* `auto` → Scrollbars appear only when necessary.

**Tailwind Equivalent:**

* `overflow-visible`
* `overflow-hidden`
* `overflow-scroll`
* `overflow-auto`

---

## 2. 🔹 Examples

### Overflow: visible

```css
div {
  width: 200px;
  height: 65px;
  background-color: coral;
  overflow: visible;
}
```

Tailwind:

```html
<div class="w-[200px] h-[65px] bg-coral overflow-visible">Content</div>
```

### Overflow: hidden

```css
div {
  overflow: hidden;
}
```

Tailwind:

```html
<div class="overflow-hidden">Content</div>
```

### Overflow: scroll

```css
div {
  overflow: scroll;
}
```

Tailwind:

```html
<div class="overflow-scroll">Content</div>
```

### Overflow: auto

```css
div {
  overflow: auto;
}
```

Tailwind:

```html
<div class="overflow-auto">Content</div>
```

### Overflow-x and Overflow-y

```css
div {
  overflow-x: hidden; /* Hide horizontal */
  overflow-y: scroll; /* Show vertical */
}
```

Tailwind:

```html
<div class="overflow-x-hidden overflow-y-scroll">Content</div>
```

---

## 3. 🖼 Diagram – Overflow Behavior

```
Container box
+---------------------+
| Content fits        | -> visible: shows all content
|---------------------|
| Extra content       | -> hidden: clipped
|                     | -> scroll/auto: scrollbars added
+---------------------+
```

---

## 4. ✋ Interview Q&A

**✋ Q1:** What is the default value of `overflow`?

* 👉 `visible`

**✋ Q2:** Difference between `hidden`, `scroll`, and `auto`?

* 👉 `hidden` clips content.
* 👉 `scroll` always shows scrollbars.
* 👉 `auto` shows scrollbars only when needed.

**✋ Q3:** How to control overflow only horizontally or vertically?

* 👉 Use `overflow-x` and `overflow-y`.

**✋ Q4:** Tailwind equivalent of `overflow-x: hidden`?

* 👉 `overflow-x-hidden`

**✋ Q5:** When should you use `overflow: auto`?

* 👉 For **responsive containers** to show scrollbars only when content exceeds container size.

---

## 5. ✅ Summary

* `overflow` controls content overflow behavior.
* Use `overflow-x` and `overflow-y` for directional control.
* Tailwind provides utility classes for quick implementation.
* Choose `hidden` to clip, `scroll` to always scroll, `auto` for conditional scroll.

🔗 References:

* [W3Schools – CSS Overflow](https://www.w3schools.com/css/css_overflow.asp)
* [Tailwind CSS – Overflow](https://tailwindcss.com/docs/overflow)
