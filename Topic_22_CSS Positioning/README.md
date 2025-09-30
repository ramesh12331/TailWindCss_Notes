# 📌 CSS Position Property – Complete Guide

CSS positioning allows **control over element placement** and overrides the normal document flow using the `position` property along with `top`, `right`, `bottom`, and `left` properties.

---

## 1. 🛠 Position Values

| Value      | Description                                                                   |
| ---------- | ----------------------------------------------------------------------------- |
| `static`   | Default. Elements follow normal document flow.                                |
| `relative` | Positioned relative to its normal position.                                   |
| `absolute` | Positioned relative to nearest positioned ancestor. Removed from normal flow. |
| `fixed`    | Positioned relative to viewport. Stays fixed on scroll.                       |
| `sticky`   | Switches between relative and fixed based on scroll position.                 |

---

## 2. 🔹 CSS position: static

* **Default** for all elements.
* **Cannot be moved** using top, right, bottom, or left.

**Example:**

```css
div.static {
  position: static;
  border: 3px solid #73AD21;
}
```

**Tailwind:**

```html
<div class="static border-4 border-green-600">Static Element</div>
```

---

## 3. 🔹 CSS position: relative

* Positioned **relative to its normal position**.
* Allows movement using `top`, `right`, `bottom`, `left`.

**Example:**

```css
div.relative {
  position: relative;
  left: 30px;
  border: 3px solid #73AD21;
}
```

**Tailwind:**

```html
<div class="relative left-7 border-4 border-green-600">Relative Element</div>
```

---

## 4. 🔹 CSS position: fixed

* Positioned **relative to the viewport**.
* Stays in place during scroll.
* Removed from normal flow.

**Example:**

```css
div.fixed {
  position: fixed;
  bottom: 0;
  right: 0;
  width: 300px;
  border: 3px solid #73AD21;
}
```

**Tailwind:**

```html
<div class="fixed bottom-0 right-0 w-[300px] border-4 border-green-600">Fixed Element</div>
```

---

## 5. 🔹 CSS position: absolute

* Positioned **relative to nearest positioned ancestor**.
* Removed from normal flow.

**Example:**

```css
div.relative {
  position: relative;
  width: 400px;
  height: 200px;
  border: 3px solid green;
}
div.absolute {
  position: absolute;
  top: 80px;
  right: 0;
  width: 200px;
  height: 100px;
  border: 3px solid red;
}
```

**Tailwind:**

```html
<div class="relative w-[400px] h-[200px] border-4 border-green-600">
  <div class="absolute top-20 right-0 w-[200px] h-[100px] border-4 border-red-600">Absolute</div>
</div>
```

---

## 6. 🔹 CSS position: sticky

* Switches from **relative to fixed** based on scroll.
* Requires at least one of `top`, `right`, `bottom`, or `left`.

**Example:**

```css
div.sticky {
  position: sticky;
  top: 0;
  background-color: green;
  border: 2px solid #4CAF50;
}
```

**Tailwind:**

```html
<div class="sticky top-0 bg-green-600 border-2 border-green-700">Sticky Element</div>
```

---

## 7. 🖼 Diagram – CSS Positioning

```
Normal Flow
+-------------------+
| Static Element    |
+-------------------+

Relative (offset)
+-------------------+
| Relative Element  | <- shifted 30px
+-------------------+

Absolute
+-------------------+
| Absolute Element  | <- positioned inside Relative Parent
+-------------------+

Fixed
+-------------------+
| Fixed Element     | <- viewport corner
+-------------------+

Sticky
+-------------------+
| Sticky Element    | <- sticks when scrolled to top
+-------------------+
```

---

## 8. ✋ Interview Q&A

**✋ Q1:** Difference between `relative` and `absolute`?

* 👉 `relative` moves element relative to normal position; `absolute` positions it relative to nearest positioned ancestor.

**✋ Q2:** What is `sticky` used for?

* 👉 To make elements stick after scrolling to a certain position.

**✋ Q3:** How does `fixed` differ from `absolute`?

* 👉 `fixed` is relative to viewport and stays on screen; `absolute` is relative to ancestor.

**✋ Q4:** Can static elements use `top` or `left`?

* 👉 No, `static` ignores positioning properties.

**✋ Q5:** Tailwind equivalents?

* `relative` → `class="relative"`
* `absolute` → `class="absolute"`
* `fixed` → `class="fixed"`
* `sticky` → `class="sticky"`
* `static` → `class="static"`

---

## 9. ✅ Summary

* CSS positioning types: `static`, `relative`, `absolute`, `fixed`, `sticky`.
* Use `top`, `right`, `bottom`, `left` to adjust position.
* Tailwind utility classes simplify positioning.
* Absolute & fixed remove element from normal flow; relative & sticky retain flow behavior.

🔗 References:

* [W3Schools – CSS Position](https://www.w3schools.com/css/css_positioning.asp)
* [Tailwind CSS – Position](https://tailwindcss.com/docs/position)
