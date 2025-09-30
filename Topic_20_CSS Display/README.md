# 📌 CSS Display Property – Complete Guide

The CSS `display` property controls the layout of HTML elements. It determines **how an element is displayed in the document flow**. Every HTML element has a **default display value** (usually `block` or `inline`). You can override this using the `display` property.

---

## 1. 🛠 Block-Level Elements

* **Definition:** Always start on a new line and take full available width.
* **Examples:** `<div>`, `<h1> - <h6>`, `<p>`, `<form>`, `<header>`, `<footer>`, `<section>`

**CSS Example:**

```css
div {
  display: block;
}
```

**Tailwind:**

```html
<div class="block">Content</div>
```

---

## 2. 🟢 Inline Elements

* **Definition:** Do not start on a new line; only take up as much width as needed.
* **Examples:** `<span>`, `<a>`, `<img>`

**CSS Example:**

```css
span {
  display: inline;
}
```

**Tailwind:**

```html
<span class="inline">Text</span>
```

---

## 3. 🔹 Inline-Block Elements

* **Definition:** Behaves like inline element (on same line) but can have width, height, padding, and margin like block element.

**CSS Example:**

```css
span {
  display: inline-block;
  width: 150px;
  height: 50px;
  background-color: lightblue;
}
```

**Tailwind:**

```html
<span class="inline-block w-[150px] h-[50px] bg-blue-200">Inline Block</span>
```

---

## 4. 🎯 Block vs Inline vs Inline-Block – Diagram & Icons

```
📦 Block       |──────────── full width ───────────|
              | Content inside block             |

🔹 Inline     |Content1|Content2|Content3|
             | only takes content width          |

🟦 Inline-Block |Content1|Content2|Content3|
               | can set width/height            |
```

* 📦 = Block
* 🔹 = Inline
* 🟦 = Inline-Block

---

## 5. 🎯 Common Display Values

| Value          | Description                                             |
| -------------- | ------------------------------------------------------- |
| `inline`       | Displays element inline                                 |
| `block`        | Displays element as a block                             |
| `inline-block` | Inline element but can have width/height/padding/margin |
| `flex`         | Block-level flex container                              |
| `grid`         | Block-level grid container                              |
| `contents`     | Makes container disappear; children move up in DOM      |
| `none`         | Hides the element (takes no space)                      |

---

## 6. 🔒 Hiding Elements

* `display: none;` → element is hidden and **does not take space**
* `visibility: hidden;` → element is hidden but **still takes space**

**CSS Example:**

```css
h1.hidden { display: none; }
h2.hidden { visibility: hidden; }
```

**Tailwind:**

```html
<h1 class="hidden">Hidden</h1>
<h2 class="invisible">Invisible but takes space</h2>
```

**JavaScript Toggle Example:**

```html
<div id="panel" class="hidden">Content</div>
<button onclick="togglePanel()">Toggle Panel</button>
<script>
function togglePanel() {
  var x = document.getElementById('panel');
  x.classList.toggle('hidden');
}
</script>
```

---

## 7. 🔄 Override Default Display

* Change `<li>` elements to inline for horizontal menus:

```css
li { display: inline; }
```

**Tailwind:**

```html
<li class="inline">Menu Item</li>
```

* Change `<span>` or `<a>` to block:

```css
span { display: block; }
a { display: block; }
```

**Tailwind:**

```html
<span class="block">Block Span</span>
<a class="block">Block Link</a>
```

---

## 8. ❓ Interview Q&A

**Q1:** Difference between `display: none` and `visibility: hidden`?

* `none` removes element from flow; `hidden` keeps space.

**Q2:** How to create horizontal menus using CSS?

* Set `<li>` to `display: inline` or `inline-block`.

**Q3:** Can inline elements contain block elements?

* No. Setting `display: block` on inline allows some block properties but original HTML restrictions remain.

**Q4:** Tailwind equivalent of `display: flex` and `display: grid`?

* `flex` → `class="flex"`
* `grid` → `class="grid"`

**Q5:** How to toggle visibility of an element with Tailwind and JS?

* Use `classList.toggle('hidden')`.

---

## 9. ✅ Summary

* `display` controls layout of elements.
* `block` vs `inline` vs `inline-block`.
* `flex` and `grid` are for modern layouts.
* `none` vs `visibility: hidden`.
* Tailwind provides utility classes: `block`, `inline`, `inline-block`, `flex`, `grid`, `hidden`, `invisible`.

🔗 References:

* [W3Schools – CSS Display](https://www.w3schools.com/css/css_display_visibility.asp)
* [Tailwind CSS – Display](https://tailwindcss.com/docs/display)
