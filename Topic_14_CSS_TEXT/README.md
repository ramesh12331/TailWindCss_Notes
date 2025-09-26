# 📘 CSS Text Styling Guide  

This guide covers **CSS Text properties** with ✅ examples, ✍️ syntax, ⚡ Tailwind CSS equivalents, and 🎯 interview questions.  

---

## 🎨 CSS Text Color
The `color` property sets the text color.

### ✍️ Syntax:
```css
selector {
  color: value;
}
```

✅ Examples:
```css
body { color: blue; }
h1 { color: green; }
h2 { color: red; }
```

⚡ Tailwind CSS:
```html
<p class="text-blue-500">🔵 Blue text</p>
<h1 class="text-green-600">🟢 Green text</h1>
<h2 class="text-red-500">🔴 Red text</h2>
```

---

## 🧭 Text Alignment
The `text-align` property sets the horizontal alignment of text.

✍️ Syntax:
```css
selector {
  text-align: left | right | center | justify;
}
```

✅ Example:
```css
h1 { text-align: center; }
h2 { text-align: left; }
h3 { text-align: right; }
div { text-align: justify; }
```

⚡ Tailwind CSS:
```html
<h1 class="text-center">📍 Centered</h1>
<h2 class="text-left">⬅️ Left</h2>
<h3 class="text-right">➡️ Right</h3>
<div class="text-justify">📰 Justified text</div>
```

---

## ✍️ Text Decoration
The `text-decoration` property adds lines (underline, overline, strike).

✍️ Syntax:
```css
selector {
  text-decoration: line color style thickness;
}
```

✅ Example:
```css
h1 { text-decoration: underline; }
h2 { text-decoration: underline red double; }
p  { text-decoration: underline red wavy 3px; }
```

⚡ Tailwind CSS:
```html
<h1 class="underline">✒️ Underlined</h1>
<h2 class="underline decoration-red-500 decoration-double">🔴 Double underline</h2>
<p class="underline decoration-red-500 decoration-wavy decoration-2">🌊 Wavy underline</p>
```

---

## 🔠 Text Transformation
The `text-transform` property changes capitalization.

✍️ Syntax:
```css
selector {
  text-transform: uppercase | lowercase | capitalize | none;
}
```

✅ Example:
```css
p.uppercase { text-transform: uppercase; }
p.lowercase { text-transform: lowercase; }
p.capitalize { text-transform: capitalize; }
```

⚡ Tailwind CSS:
```html
<p class="uppercase">🔠 UPPERCASE</p>
<p class="lowercase">🔡 lowercase</p>
<p class="capitalize">📝 Capitalize Words</p>
```

---

## 📏 Text Spacing

1️⃣ **Indentation (text-indent)**
```css
p { text-indent: 50px; }
```
👉 Tailwind:
```html
<p class="indent-8">➡️ Indented text</p>
```

2️⃣ **Letter Spacing (letter-spacing)**
```css
h1 { letter-spacing: 5px; }
```
👉 Tailwind:
```html
<h1 class="tracking-widest">📏 Wide spacing</h1>
```

3️⃣ **Line Height (line-height)**
```css
p.big { line-height: 1.8; }
```
👉 Tailwind:
```html
<p class="leading-loose">📐 Loose line height</p>
```

4️⃣ **White Space (white-space)**
```css
p { white-space: nowrap; }
```
👉 Tailwind:
```html
<p class="whitespace-nowrap">🚫 No wrap</p>
```

---

## 🌟 Text Shadow
The `text-shadow` property adds shadows/glow.

✍️ Syntax:
```css
selector {
  text-shadow: h-shadow v-shadow blur color;
}
```

✅ Example:
```css
h1 {
  text-shadow: 2px 2px 5px red;
}
```

👉 Tailwind has no built-in shadows for text. Use custom CSS:
```css
.custom-shadow { text-shadow: 2px 2px 5px red; }
```

```html
<h1 class="text-white custom-shadow">💡 Shadow Text</h1>
```

---

## 📊 Diagram: CSS Text Properties Overview
```
+----------------------------------------------------+
|              🎨 CSS Text Styling                   |
+----------------------------------------------------+
|  🎨 Color         →  color, background-color       |
|  🧭 Alignment     →  text-align, text-align-last   |
|  ✍️ Decoration    →  underline, overline, strike   |
|  🔠 Transformation→  uppercase, lowercase, cap     |
|  📏 Spacing       →  indent, letter/word spacing   |
|  🌟 Shadow        →  text-shadow (multi effects)   |
+----------------------------------------------------+
```

---

## ❓ Interview Questions & Answers

**Q1: ✋ Difference between em, rem, and px in text styling?**  
👉 Answer:  
- 📌 px: Absolute fixed size  
- 📌 em: Relative to parent element font size  
- 📌 rem: Relative to root (html) font size  

**Q2: ✋ How to center text vertically & horizontally?**  
👉 Answer:
```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```
⚡ Tailwind:
```html
<div class="flex justify-center items-center">✨ Centered text</div>
```

**Q3: ✋ Difference between `text-align: justify` and `text-align-last: justify`?**  
👉 Answer:  
- 📖 `text-align: justify` → All lines stretched  
- 📝 `text-align-last: justify` → Only last line stretched  

**Q4: ✋ Can we add multiple text-shadow in CSS?**  
👉 Answer:  
✅ Yes! Example:
```css
text-shadow: 1px 1px red, 2px 2px blue;
```

**Q5: ✋ How to remove underline from links?**  
👉 Answer:
```css
a { text-decoration: none; }
```
⚡ Tailwind:
```html
<a href="#" class="no-underline">🔗 No underline link</a>
```

---

## ✅ Conclusion
- 🎨 Use `color` & `background-color` for contrast  
- 🧭 Use `text-align` for readability  
- ✍️ Use `text-decoration` for emphasis  
- 🔠 Use `text-transform` for capitalization  
- 🌟 Use `text-shadow` for effects  
- ⚡ In Tailwind, these are simplified with utility classes  
