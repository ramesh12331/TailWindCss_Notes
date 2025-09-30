# 📊 CSS Tables – Complete Guide

Tables in CSS can be styled using properties such as **borders, spacing, padding, alignment, colors, and responsiveness**.

This guide covers **syntax, examples, diagrams, Tailwind usage, and interview questions**.

---

## 1. 🛠 Table Borders

### Syntax

```css
table, th, td {
  border: 1px solid black;
}
```

### Example

| Firstname | Lastname |
| --------- | -------- |
| Peter     | Griffin  |
| Lois      | Griffin  |

### Tailwind Equivalent

```html
<table class="border border-gray-500">
  <tr>
    <th class="border px-4 py-2">Firstname</th>
    <th class="border px-4 py-2">Lastname</th>
  </tr>
  <tr>
    <td class="border px-4 py-2">Peter</td>
    <td class="border px-4 py-2">Griffin</td>
  </tr>
</table>
```

## 2. 🎯 Border Collapse vs Separate

```css
table {
  border-collapse: collapse; /* single border */
}
```

* **collapse** → Merges borders into a single line
* **separate** (default) → Each cell shows its own border

✅ Tailwind: `border-collapse` / `border-separate`

## 3. 📐 Padding & Spacing

```css
th, td {
  padding: 10px;
}
table {
  border-spacing: 15px; /* only with border-separate */
}
```

Tailwind:

```html
<th class="px-4 py-2">Name</th>
<td class="px-4 py-2">Value</td>
<table class="border-separate border-spacing-4"> ... </table>
```

## 4. 📏 Width & Height

```css
table { width: 100%; }
th { height: 70px; }
```

Tailwind:

```html
<table class="w-full">
  <th class="h-[70px]">Heading</th>
</table>
```

## 5. 📝 Text Alignment

```css
td { text-align: center; }
th { text-align: left; }
```

Tailwind:

```html
<td class="text-center">Center</td>
<th class="text-left">Left</th>
```

## 6. 📊 Vertical Alignment

```css
td {
  height: 50px;
  vertical-align: bottom;
}
```

✅ Tailwind: `align-top`, `align-middle`, `align-bottom`

```html
<td class="h-[50px] align-bottom">Bottom aligned</td>
```

## 7. 🎨 Table Colors & Styling

**Zebra Stripes**

```css
tr:nth-child(even) {
  background-color: #f2f2f2;
}
```

Tailwind:

```html
<tr class="even:bg-gray-100">
```

**Hover Effect**

```css
tr:hover { background-color: coral; }
```

Tailwind:

```html
<tr class="hover:bg-orange-300">
```

**Header Colors**

```css
th {
  background-color: #04AA6D;
  color: white;
}
```

Tailwind:

```html
<th class="bg-green-600 text-white">Heading</th>
```

## 8. 📱 Responsive Tables

```css
div.tablecontainer {
  overflow-x: auto;
}
```

Tailwind:

```html
<div class="overflow-x-auto">
  <table class="table-auto"> ... </table>
</div>
```

## 9. 🖼 Diagram – CSS Table Styling

```
+-------------------+
|    <table>        |
| +---------------+ |
| | <th> Heading | |
| +---------------+ |
| | <td> Data    | |
| +---------------+ |
+-------------------+
 ↑ Border / Padding
```

## 10. ❓ Interview Q&A

**Q1:** How do you remove double borders in CSS tables?

* Use `border-collapse: collapse;`

**Q2:** Difference between `collapse` and `separate`?

* collapse merges borders, separate keeps each cell’s borders.

**Q3:** How do you create zebra-striped tables?

* Use `tr:nth-child(even)` or Tailwind’s `even:bg-gray-100`.

**Q4:** How do you make tables responsive?

* Wrap in a container with `overflow-x: auto`.

**Q5:** How do you align table text vertically?

* CSS: `vertical-align: top/middle/bottom`
* Tailwind: `align-top`, `align-middle`, `align-bottom`

## 11. ✅ Summary

* **Borders:** border, border-collapse
* **Spacing:** padding, border-spacing
* **Size:** width, height
* **Alignment:** text-align, vertical-align
* **Styling:** Zebra stripes, hover effects, colors
* **Responsive:** overflow-x: auto

📌 Tailwind makes table styling faster with utility classes.

🔗 References:

* W3Schools – CSS Tables
* Tailwind CSS Tables
