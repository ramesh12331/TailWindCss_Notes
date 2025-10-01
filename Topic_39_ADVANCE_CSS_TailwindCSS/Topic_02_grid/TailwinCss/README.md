# 📘 Tailwind CSS Grid Examples (Beginner ➔ Advanced)

This guide covers **basic to advanced Tailwind CSS grid layouts** with definitions, examples, and summaries for beginners.

---

## 1️⃣ Basic Grid (3 Columns)

📌 **Definition:** A grid with a fixed number of columns.
💻 **Code:**

```html
<div class="grid grid-cols-3 gap-4">
  <div class="bg-red-300 p-4 text-center">1</div>
  <div class="bg-green-300 p-4 text-center">2</div>
  <div class="bg-blue-300 p-4 text-center">3</div>
</div>
```

✅ **Summary:** Creates a simple 3-column grid with equal width items.

---

## 2️⃣ Fixed Columns (2 Columns)

📌 **Definition:** Grid with a fixed number of 2 columns.
💻 **Code:**

```html
<div class="grid grid-cols-2 gap-4">
  <div class="bg-yellow-300 p-4 text-center">A</div>
  <div class="bg-pink-300 p-4 text-center">B</div>
  <div class="bg-purple-300 p-4 text-center">C</div>
  <div class="bg-gray-300 p-4 text-center">D</div>
</div>
```

✅ **Summary:** Always displays items in 2 columns, wrapping when needed.

---

## 3️⃣ Responsive Grid

📌 **Definition:** Grid that adjusts columns based on screen size breakpoints.
💻 **Code:**

```html
<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
  <div class="bg-red-300 p-4 text-center">1</div>
  <div class="bg-green-300 p-4 text-center">2</div>
  <div class="bg-blue-300 p-4 text-center">3</div>
  <div class="bg-yellow-300 p-4 text-center">4</div>
</div>
```

✅ **Summary:** Dynamically changes the number of columns at different screen sizes.

---

## 4️⃣ Column Span

📌 **Definition:** Allows an item to span across multiple columns.
💻 **Code:**

```html
<div class="grid grid-cols-4 gap-4">
  <div class="col-span-2 bg-red-300 p-4 text-center">Span 2 Columns</div>
  <div class="bg-green-300 p-4 text-center">B</div>
  <div class="bg-blue-300 p-4 text-center">C</div>
</div>
```

✅ **Summary:** Item 1 spans across 2 columns, while others occupy 1 column each.

---

## 5️⃣ Row Span

📌 **Definition:** Allows an item to span across multiple rows.
💻 **Code:**

```html
<div class="grid grid-cols-3 gap-4">
  <div class="row-span-2 bg-yellow-300 p-4 text-center">Row Span 2</div>
  <div class="bg-pink-300 p-4 text-center">B</div>
  <div class="bg-purple-300 p-4 text-center">C</div>
  <div class="bg-gray-300 p-4 text-center">D</div>
</div>
```

✅ **Summary:** First item spans 2 rows, creating a taller grid cell.

---

## 6️⃣ Nested Grid

📌 **Definition:** Grid inside another grid (parent-child structure).
💻 **Code:**

```html
<div class="grid grid-cols-2 gap-4">
  <div class="bg-red-200 p-4">
    Parent 1
    <div class="grid grid-cols-2 gap-2 mt-2">
      <div class="bg-red-400 p-2">1a</div>
      <div class="bg-red-500 p-2">1b</div>
    </div>
  </div>
  <div class="bg-green-200 p-4">
    Parent 2
    <div class="grid grid-cols-2 gap-2 mt-2">
      <div class="bg-green-400 p-2">2a</div>
      <div class="bg-green-500 p-2">2b</div>
    </div>
  </div>
</div>
```

✅ **Summary:** Demonstrates how to place grids inside grid items.

---

## 7️⃣ Auto-fit / Auto-fill with `minmax()`

📌 **Definition:** Auto-adjusts columns based on available space.
💻 **Code:**

```html
<div class="grid grid-cols-[repeat(auto-fit,minmax(150px,1fr))] gap-4">
  <div class="bg-blue-300 p-4 text-center">1</div>
  <div class="bg-blue-400 p-4 text-center">2</div>
  <div class="bg-blue-500 p-4 text-center">3</div>
  <div class="bg-blue-600 p-4 text-center">4</div>
  <div class="bg-blue-700 p-4 text-center">5</div>
</div>
```

✅ **Summary:** Columns expand/shrink automatically but stay at least `150px` wide.

---

## 8️⃣ Advanced Layout (Dashboard Example)

📌 **Definition:** Real-world layout combining column/row spans.
💻 **Code:**

```html
<div class="grid grid-cols-4 grid-rows-3 gap-4">
  <div class="col-span-4 bg-gray-300 p-4 text-center">Header</div>
  <div class="row-span-2 bg-gray-400 p-4 text-center">Sidebar</div>
  <div class="col-span-3 bg-gray-200 p-4 text-center">Main Content</div>
  <div class="col-span-3 bg-gray-500 p-4 text-center">Footer</div>
</div>
```

✅ **Summary:** Creates a **dashboard-style layout** with header, sidebar, main content, and footer.

---

# 📌 Final Summary

* **Basic Grid:** Equal columns.
* **Fixed Columns:** Always same number of columns.
* **Responsive Grid:** Adjusts per screen size.
* **Column Span:** Items stretch across multiple columns.
* **Row Span:** Items stretch across multiple rows.
* **Nested Grid:** Grid inside another grid.
* **Auto-fit / Auto-fill:** Flexible grids with min/max sizes.
* **Dashboard Layout:** Real-world multi-area design.
