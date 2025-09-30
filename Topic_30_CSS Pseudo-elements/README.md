# 🌐 CSS Pseudo-Elements

A **CSS pseudo-element** is used to style a specific part of an element, such as the **first letter, first line, before/after content, list markers, or selected text**.  

They are written with a **double colon (::)** followed by the pseudo-element name.  

---

## 📝 Syntax

```css
selector::pseudo-element {
  property: value;
}
```

---

## 📘 Common Pseudo-Elements

### 1. ::first-line  
Styles the first line of text in a block element.  
```css
p::first-line {
  color: red;
  font-variant: small-caps;
}
```

**Diagram:**  
```
Paragraph: [First line styled ✅] 
           [Rest normal ❌]
```

---

### 2. ::first-letter  
Styles the first letter of a block element.  
```css
p::first-letter {
  font-size: 2em;
  color: blue;
}
```

**Diagram:**  
```
P ✅ styled rest normal
```

---

### 3. ::before  
Inserts content before the element’s content.  
```css
h3::before {
  content: "👉 ";
  color: green;
}
```

**Diagram:**  
```
👉 Heading Text
```

---

### 4. ::after  
Inserts content after the element’s content.  
```css
h3::after {
  content: " ✅";
}
```

**Diagram:**  
```
Heading Text ✅
```

---

### 5. ::marker  
Styles list item markers.  
```css
li::marker {
  color: red;
  font-size: 20px;
}
```

---

### 6. ::selection  
Styles user-selected text.  
```css
::selection {
  color: white;
  background: blue;
}
```

---

### 7. ::backdrop  
Styles the background behind a `<dialog>` or `<popover>`.  
```css
dialog::backdrop {
  background-color: rgba(0,0,0,0.5);
}
```

---

### 8. Multiple Pseudo-Elements  
```css
p::first-letter {
  color: red;
  font-size: xx-large;
}

p::first-line {
  color: blue;
  font-variant: small-caps;
}
```

✅ First letter styled,  
✅ Rest of first line styled differently.  

---

## 🎨 Tailwind CSS Equivalent  

Tailwind does not directly support pseudo-elements, but you can **extend via @layer utilities**.

```css
@layer utilities {
  .first-line p::first-line {
    @apply text-red-500 font-bold;
  }

  .first-letter p::first-letter {
    @apply text-2xl text-blue-600;
  }

  .before-h3 h3::before {
    content: "👉 ";
    @apply text-green-500;
  }

  .after-h3 h3::after {
    content: " ✅";
    @apply text-green-600;
  }

  .list-marker li::marker {
    @apply text-pink-500;
  }

  .custom-selection::selection {
    @apply bg-yellow-400 text-black;
  }
}
```

Usage in HTML:
```html
<p class="first-line first-letter">This is a styled paragraph</p>
<h3 class="before-h3 after-h3">Heading</h3>
<ul class="list-marker">
  <li>Item</li>
</ul>
```

---

## ✋ Interview Questions & Answers  

**🙋 Q1: Difference between pseudo-class and pseudo-element?**  
👉 Pseudo-class (`:hover`) defines *state*, pseudo-element (`::before`) styles a *part of element*.  

**🙋 Q2: Can an element have multiple pseudo-elements?**  
👉 Yes, but only one of each type (`::before`, `::after`, `::first-letter`, etc.). You can combine different ones.  

**🙋 Q3: Why use ::before and ::after?**  
👉 For adding decorative content/icons without modifying HTML.  

**🙋 Q4: Is ::selection supported in all browsers?**  
👉 Mostly yes, but some old browsers have partial support.  

---

## ✅ Best Practices
- Use **pseudo-elements** for **decoration**, not essential content.  
- Combine with **Tailwind utilities** for maintainable styling.  
- Prefer **::before** & **::after** for icons, separators, tooltips.  
