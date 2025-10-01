# 📘 Tailwind CSS Media Query Guide

This guide explains **Media Queries** in CSS and their **Tailwind CSS equivalents** with examples, diagrams, and interview questions.

---

## 📌 What is a Media Query?

👉 Media queries allow you to apply CSS styles based on device conditions such as **screen width, height, or orientation**.

Example in plain CSS:

```css
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

Equivalent in **Tailwind CSS**:

```html
<div class="max-sm:bg-blue-200 sm:bg-white">Hello</div>
```

---

## 📐 Tailwind CSS Breakpoints

| Breakpoint | CSS Equivalent | Tailwind Prefix | Typical Device |
|------------|---------------|----------------|----------------|
| `max-sm`   | `@media (max-width: 639px)` | `max-sm:` | Extra small devices (phones) |
| `sm`       | `@media (min-width: 640px)` | `sm:` | Small devices (≥640px) |
| `md`       | `@media (min-width: 768px)` | `md:` | Tablets (≥768px) |
| `lg`       | `@media (min-width: 1024px)` | `lg:` | Laptops (≥1024px) |
| `xl`       | `@media (min-width: 1280px)` | `xl:` | Desktops (≥1280px) |
| `2xl`      | `@media (min-width: 1536px)` | `2xl:` | Large Desktops (≥1536px) |

---

## 📊 Examples

### 1️⃣ Background Change on Small Screen
```html
<div class="w-full h-32 bg-white sm:bg-white max-sm:bg-blue-200">
  Resize window to ≤600px → background turns lightblue
</div>
```

---

### 2️⃣ Responsive Grid with Breakpoints
```html
<div class="grid grid-cols-6 gap-2">
  <div class="col-span-6 sm:col-span-6 md:col-span-6">Item 1</div>
  <div class="col-span-6 sm:col-span-1 md:col-span-1">Item 2</div>
  <div class="col-span-6 sm:col-span-4 md:col-span-4">Item 3</div>
  <div class="col-span-6 sm:col-span-6 md:col-span-1">Item 4</div>
  <div class="col-span-6 sm:col-span-6 md:col-span-6">Item 5</div>
</div>
```

---

### 3️⃣ Typical Device Breakpoints
```html
<div class="w-full h-24 text-center flex items-center justify-center
            max-sm:bg-red-300 
            sm:bg-green-300 
            md:bg-yellow-300 
            lg:bg-blue-300 
            xl:bg-purple-300">
  Resize to see color changes per device breakpoint
</div>
```

---

### 4️⃣ Orientation Example
```html
<div class="w-full h-24 flex items-center justify-center 
            md:landscape:bg-blue-200 md:portrait:bg-pink-200">
  Changes color based on orientation
</div>
```

---

### 5️⃣ Hide Elements Example
```html
<div class="bg-gray-400 text-white p-4 sm:block max-sm:hidden">
  I will be hidden on small screens (≤600px).
</div>
```

---

### 6️⃣ Change Font Size
```html
<div class="text-center font-bold max-sm:text-[30px] sm:text-[80px]">
  Variable Font Size
</div>
```

---

## 📝 Conversion Summary

| CSS Media Query | Tailwind Equivalent |
|------------------|----------------------|
| `@media (max-width: 600px)` | `max-sm:` |
| `@media (min-width: 600px)` | `sm:` |
| `@media (min-width: 768px)` | `md:` |
| `@media (min-width: 992px)` | `lg:` |
| `@media (min-width: 1200px)` | `xl:` |
| `@media (orientation: landscape)` | `landscape:` |
| `@media (orientation: portrait)` | `portrait:` |
| `display: none on small screens` | `max-sm:hidden sm:block` |
| `font-size change` | `max-sm:text-[30px] sm:text-[80px]` |

---

## ❓ Interview Questions

👉 **Q1: What is a Media Query in CSS?**  
✋ **A:** Media Query is a CSS technique that applies styles conditionally based on device properties like width, height, or orientation.

👉 **Q2: How do Tailwind breakpoints work?**  
✋ **A:** Tailwind uses mobile-first breakpoints like `sm:`, `md:`, `lg:`, etc. By default, styles apply to smaller screens, and larger breakpoints override them.

👉 **Q3: Difference between `max-sm` and `sm` in Tailwind?**  
✋ **A:** `sm:` applies when screen width is **≥640px**, while `max-sm:` applies when screen width is **≤639px**.

👉 **Q4: Can Tailwind handle orientation (landscape/portrait)?**  
✋ **A:** Yes, with `landscape:` and `portrait:` prefixes.

---

## ✅ Summary
- Media Queries help in responsive design.  
- Tailwind provides **utility-based media query classes** like `sm:`, `md:`, `lg:`.  
- Supports **orientation-based styling**.  
- Helps build **mobile-first responsive layouts** easily.  

