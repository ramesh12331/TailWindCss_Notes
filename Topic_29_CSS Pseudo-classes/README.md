# CSS Pseudo-Classes

## 📖 Overview
A **CSS pseudo-class** is a keyword that can be added to a selector to define a style for a special state of an element.

---

## ✨ Common Use Cases
- Style an element when a user **hovers** over it
- Style **visited/unvisited** links differently
- Style an element when it **gets focus**
- Style **form states** (valid, invalid, required, optional)
- Style an element if it’s the **first or last child**

---

## 📝 Syntax
```css
selector:pseudo-class-name {
  property: value;
}
```

Example:
```css
button:hover {
  background-color: blue;
  color: white;
}
```

---

## 🎯 Examples

### 🔗 Link States
```css
a:link { color: red; }       /* Unvisited */
a:visited { color: green; }  /* Visited */
a:hover { color: magenta; }  /* Hover */
a:active { color: blue; }    /* Active */
```

📌 Note:  
Order matters → `:hover` must come **after** `:link` and `:visited`.  
`:active` must come **after** `:hover`.

---

### 🖱️ Hover on `<div>`
```css
div:hover {
  background-color: lightblue;
}
```

---

### 🎹 Focus on `<input>`
```css
input:focus {
  background-color: yellow;
  border: 2px solid red;
}
```

---

### 👶 First Child
```css
p:first-child {
  color: blue;
}
```

Diagram:

```
<div>
 ├── <p> First child ✅ styled
 ├── <p> Second child ❌ not styled
</div>
```

---

### 🌍 Language-specific (`:lang`)
```css
q:lang(no) {
  quotes: "~" "~";
}
```

---

## 🎨 Pseudo-classes + Classes
```css
a.highlight:hover {
  color: red;
  font-weight: bold;
}
```

---

## ⚡ Tooltip Hover Example
```css
p { display: none; }
div:hover p {
  display: block;
  background: yellow;
  padding: 10px;
}
```

Diagram:
```
[Hover on DIV] → Shows hidden P element like a tooltip
```

---

## 🎯 Tailwind CSS Equivalents

✅ `:hover`
```html
<button class="bg-blue-500 hover:bg-blue-700 text-white px-4 py-2">
  Hover Me
</button>
```

✅ `:focus`
```html
<input class="border border-gray-300 focus:border-blue-500 focus:ring-2 focus:ring-blue-300" />
```

✅ `:first-child`
Tailwind doesn’t have direct `:first-child` but supports `first:` modifier:
```html
<ul>
  <li class="first:text-blue-500">First Item</li>
  <li>Second Item</li>
</ul>
```

✅ `:lang()` (Tailwind doesn’t directly support it, needs custom CSS).

---

## 🙋 Interview Q&A

✋ **Q1: Difference between pseudo-class and pseudo-element?**  
🤚 **A1:** Pseudo-class (`:hover`) defines a state, pseudo-element (`::before`) styles a part of an element.

✋ **Q2: Why does order matter in link pseudo-classes?**  
🤚 **A2:** Because browsers cascade rules in the order: `:link`, `:visited`, `:hover`, `:active` (LVHA order).

✋ **Q3: How do you style the first child with Tailwind CSS?**  
🤚 **A3:** Use the `first:` variant, e.g., `first:bg-red-200`.

✋ **Q4: Can pseudo-classes be combined with classes?**  
🤚 **A4:** Yes, e.g., `.btn:hover` or `a.highlight:visited`.

---

## ✅ Best Practices
- Use `:hover` for better UX feedback.  
- Always consider **accessibility** (e.g., don’t rely on hover alone for tooltips).  
- Follow the **LVHA** order for links.  
- Use Tailwind variants (`hover:`, `focus:`, `first:`, `last:`) whenever possible.

---
