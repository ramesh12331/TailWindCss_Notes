# 📌 CSS z-index Property – Complete Guide

The CSS `z-index` property specifies the **stack order** of positioned elements. Elements with higher `z-index` values appear in front of elements with lower values.

---

## 1. 🛠 Syntax

```css
selector {
  position: relative | absolute | fixed | sticky;
  z-index: value;
}
```

* **value:** Can be positive, negative, or zero.
* **Important:** Only works on **positioned elements** (relative, absolute, fixed, sticky) or **flex items**.

**Example:**

```css
img {
  position: absolute;
  left: 0;
  top: 0;
  z-index: -1;
}
```

**Tailwind Equivalent:**

```html
<img class="absolute left-0 top-0 -z-10" src="image.jpg" alt="">
```

---

## 2. 🔹 Example of z-index stacking

```html
<div class="container relative">
  <div class="black-box relative z-10 border-2 border-black h-[100px] m-7">Black box</div>
  <div class="gray-box absolute z-30 bg-gray-300 h-[60px] w-[70%] left-[50px] top-[50px]">Gray box</div>
  <div class="green-box absolute z-20 bg-green-300 w-[35%] left-[270px] top-[-15px] h-[100px]">Green box</div>
</div>
```

* **Result:** Gray box appears on top, green box behind it, black box at the bottom.

---

## 3. 🔹 Without z-index

* Positioned elements without `z-index` are stacked in **HTML source order**.
* First elements in HTML appear **below** later elements if overlapping.

**Example:**

```html
<div class="container relative">
  <div class="black-box relative border-2 border-black h-[100px] m-7">Black box</div>
  <div class="gray-box absolute bg-gray-300 h-[60px] w-[70%] left-[50px] top-[50px]">Gray box</div>
  <div class="green-box absolute bg-green-300 w-[35%] left-[270px] top-[-15px] h-[100px]">Green box</div>
</div>
```

* **Result:** Elements stack according to HTML order.

---

## 4. 🖼 Diagram – z-index Stacking Order

```
HTML order (no z-index)
Top: last element in HTML
Middle: middle element in HTML
Bottom: first element in HTML

With z-index
z-index: 30 -> Gray box (Top)
z-index: 20 -> Green box (Middle)
z-index: 10 -> Black box (Bottom)
```

---

## 5. ✋ Interview Q&A

**✋ Q1:** What is the purpose of `z-index`?

* 👉 Specifies the **stack order** of positioned elements.

**✋ Q2:** Does `z-index` work on static elements?

* 👉 No. Only works on **positioned** or **flex item** elements.

**✋ Q3:** Can `z-index` be negative?

* 👉 Yes. Elements with negative `z-index` appear **behind** others.

**✋ Q4:** What happens if multiple elements have the same `z-index`?

* 👉 Stacking follows **HTML source order**.

**✋ Q5:** Tailwind equivalent for z-index?

* 👉 `z-0`, `z-10`, `z-20`, `z-30`, `z-40`, `z-50`, `-z-10`, etc.

---

## 6. ✅ Summary

* `z-index` controls **overlapping and stacking order**.
* Works only on **positioned elements** or **flex items**.
* Positive, negative, or zero values can be used.
* Without `z-index`, elements stack based on **HTML source order**.
* Tailwind provides utility classes for easy stacking control.

🔗 References:

* [W3Schools – CSS z-index](https://www.w3schools.com/cssref/pr_pos_z-index.asp)
* [Tailwind CSS – z-index](https://tailwindcss.com/docs/z-index)
