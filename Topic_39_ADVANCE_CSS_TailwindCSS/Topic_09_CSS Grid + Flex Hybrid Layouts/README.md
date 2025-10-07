# 🧩 CSS Grid + Flex Hybrid Layouts

Learn how to **combine CSS Grid and Flexbox** to create complex, responsive, and modern layouts.  
Use **Grid for the main structure** and **Flexbox for content alignment inside grid items**.

---

## 🔹 1. Why Hybrid Layouts?

- **Grid** → Best for **2D layouts** (rows + columns).  
- **Flexbox** → Best for **1D alignment** (row OR column).  
- **Hybrid** → Grid handles the page structure, Flexbox aligns content inside grid items.

✅ Useful for dashboards, cards, galleries, and responsive sections.

---

## 🔹 2. CSS Grid Basics

### 📘 Syntax
```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 20px;
}
```

### 💻 Example
```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  grid-gap: 10px;
}
.item {
  background: #4f46e5;
  color: #fff;
  padding: 20px;
  text-align: center;
}
```

### 🪄 Tailwind CSS Example
```html
<div class="grid grid-cols-3 gap-4">
  <div class="bg-indigo-600 text-white p-4 text-center">Item 1</div>
  <div class="bg-indigo-600 text-white p-4 text-center">Item 2</div>
  <div class="bg-indigo-600 text-white p-4 text-center">Item 3</div>
</div>
```

✅ **Summary:** Grid creates rows and columns, defining the main layout.

---

## 🔹 3. Flexbox Inside Grid Items

### 📘 Syntax
```css
.item {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
```

### 💻 Example
```css
.item {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 150px;
  background: #f97316;
  color: #fff;
}
```

### 🪄 Tailwind CSS Example
```html
<div class="grid grid-cols-2 gap-4">
  <div class="flex flex-col justify-center items-center bg-orange-500 text-white h-40">
    <h2 class="text-lg font-bold">Title</h2>
    <p>Content aligned center</p>
  </div>
  <div class="flex flex-col justify-center items-center bg-orange-500 text-white h-40">
    <h2 class="text-lg font-bold">Title</h2>
    <p>Content aligned center</p>
  </div>
</div>
```

✅ **Summary:** Flexbox aligns and distributes content **inside each grid item**.

---

## 🔹 4. Complex Hybrid Layout Example

### 💻 HTML + CSS
```html
<div class="dashboard">
  <header>Header</header>
  <nav>Sidebar</nav>
  <main>
    <section class="cards">
      <div class="card">Card 1</div>
      <div class="card">Card 2</div>
      <div class="card">Card 3</div>
    </section>
  </main>
  <footer>Footer</footer>
</div>
```

```css
.dashboard {
  display: grid;
  grid-template-areas:
    "header header"
    "nav main"
    "footer footer";
  grid-template-columns: 200px 1fr;
  grid-template-rows: 60px 1fr 50px;
  gap: 10px;
}

header { grid-area: header; background: #6366f1; color: white; }
nav { grid-area: nav; background: #818cf8; color: white; }
main { grid-area: main; background: #a5b4fc; }

.cards {
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
}
.card {
  flex: 1 1 30%;
  background: #4f46e5;
  color: white;
  padding: 20px;
  text-align: center;
}
footer { grid-area: footer; background: #6366f1; color: white; text-align: center; }
```

### 🪄 Tailwind CSS Example
```html
<div class="grid grid-rows-[60px_1fr_50px] grid-cols-[200px_1fr] gap-2 h-screen">
  <header class="col-span-2 bg-indigo-600 text-white flex items-center justify-center">Header</header>
  <nav class="bg-indigo-400 text-white flex items-center justify-center">Sidebar</nav>
  <main class="bg-indigo-200 p-4">
    <div class="flex flex-wrap gap-4">
      <div class="flex-1 min-w-[30%] bg-indigo-600 text-white p-4 text-center">Card 1</div>
      <div class="flex-1 min-w-[30%] bg-indigo-600 text-white p-4 text-center">Card 2</div>
      <div class="flex-1 min-w-[30%] bg-indigo-600 text-white p-4 text-center">Card 3</div>
    </div>
  </main>
  <footer class="col-span-2 bg-indigo-600 text-white flex items-center justify-center">Footer</footer>
</div>
```

✅ **Summary:** Grid defines the **overall layout**, Flexbox distributes **cards or content inside main sections**.

---

## 🧾 5. Key Concepts

| 🔖 Concept | 🧩 Explanation | ⚡ Tailwind Example |
|------------|----------------|------------------|
| Grid | 2D layout: rows + columns | `grid grid-cols-3 gap-4` |
| Flexbox | 1D alignment inside items | `flex flex-col justify-center items-center` |
| Hybrid | Grid for layout + Flex inside | Combine `grid` + `flex` classes |
| Gap & Wrap | Spacing & responsive wrapping | `gap-4 flex-wrap` |
| Responsive | Adjust columns and flex | `sm:grid-cols-2 md:grid-cols-3` |

---

## 🧠 Pro Tips

- Use **Grid** for the **page or section layout**.  
- Use **Flexbox** for **alignment, centering, and distributing elements** inside each grid cell.  
- Combine `flex-wrap` and responsive `grid-cols-*` for mobile-friendly layouts.  
- Use Tailwind’s **arbitrary values** for custom widths or gaps: `[min-width:30%]` or `[grid-template-columns:200px_1fr]`.  

---

### 🎨 Visual Representation

```
Grid Layout (Main Structure)
┌─────────┬─────────────┐
│ Header  │ Header      │
├─────────┼─────────────┤
│ Sidebar │ Main Content│
├─────────┴─────────────┤
│ Footer                │
└───────────────────────┘

Flex Inside Grid Cells
[Card1] [Card2] [Card3] aligned using flex
```

---

**📘 Author:** Ramesh  
**💡 Topic:** CSS Grid + Flex Hybrid Layouts  
**🕹️ Level:** Beginner → Advanced
