# CSS Links Guide 🖇️

Learn how to style links in CSS with examples, states, buttons, cursors, and Tailwind CSS syntax.

---

## 1. CSS Styling Links 🎨

HTML links can be styled using CSS properties like `color`, `text-decoration`, `background-color`, `font-size`, `font-weight`, `font-family`, etc.

**Example:**

```css
/* Style a link with color, background, and bold font */
a {
  color: hotpink; /* 🌸 Text color */
  background-color: yellow; /* 💛 Background */
  font-weight: bold; /* 💪 Bold text */
}
```

---

## 2. Styling Links Depending on State 🟢🔵

Four link states:

* `:link` - Normal, unvisited link 🔗
* `:visited` - Visited link 👀
* `:hover` - Mouse over link 🖱️
* `:active` - Clicked link ✋

**Order rules:**

* `:hover` must come after `:link` and `:visited`
* `:active` must come after `:hover`

**Example:**

```css
/* Unvisited link 🔗 */
a:link { color: red; }

/* Visited link 👀 */
a:visited { color: green; }

/* Hover effect 🖱️ */
a:hover { color: hotpink; }

/* Active/Clicked ✋ */
a:active { color: blue; }
```

---

## 3. CSS Links - Text Decoration ✏️

Remove or add underline for links:

```css
a:link, a:visited { text-decoration: none; }
a:hover, a:active { text-decoration: underline; }
```

---

## 4. CSS Links - Background Color 🖌️

```css
a:link { background-color: yellow; }
a:visited { background-color: cyan; }
a:hover { background-color: lightgreen; }
a:active { background-color: hotpink; }
```

---

## 5. CSS Link Buttons 🔘

```css
/* Button style for links */
a:link, a:visited {
  background-color: #f44336; /* 🔴 Red background */
  color: white; /* ⚪ White text */
  padding: 14px 25px; /* 📏 Padding */
  text-align: center; /* 🖼️ Center text */
  text-decoration: none; /* ❌ Remove underline */
  display: inline-block;
}
a:hover, a:active {
  background-color: red; /* 🔴 Darker on hover */
}
```

**Alternative Button Style:**

```css
a:link, a:visited {
  background-color: white;
  color: black;
  border: 2px solid green; /* 🟢 Border */
  padding: 10px 20px;
}
a:hover, a:active {
  background-color: green; /* 🟢 Hover */
  color: white;
}
```

---

## 6. More Examples ✨

```css
/* Hover text color change */
a.one:hover { color: orange; }
/* Hover font-size increase */
a.two:hover { font-size: 150%; }
/* Hover background change */
a.three:hover { background: lightgreen; }
/* Hover font family change */
a.four:hover { font-family: monospace; }
/* Hover underline */
a.five:hover { text-decoration: underline; }
```

---

## 7. CSS Link Cursors 🖱️

```html
<span style="cursor: auto">auto</span>
<span style="cursor: crosshair">crosshair</span>
<span style="cursor: pointer">pointer 👆</span>
<span style="cursor: help">help ❓</span>
<span style="cursor: wait">wait ⏳</span>
```

Other cursor types: `default`, `move`, `text`, `n-resize`, `e-resize`, `s-resize`, `w-resize`, `ne-resize`, `nw-resize`, `se-resize`, `sw-resize`, `progress`.

---

## 8. Tailwind CSS Link Examples 🐦

```html
<!-- Text link -->
<a href="#" class="text-red-500 hover:text-pink-500">Link</a>

<!-- Button link -->
<a href="#" class="bg-red-500 text-white px-4 py-2 hover:bg-red-700">Button Link</a>
```

---

## 9. Interview Questions & Answers ❓💡

**Q1:** What are the four link states in CSS?

* 👆 Answer: `:link`, `:visited`, `:hover`, `:active`

**Q2:** How do you remove underline from links?

* 👆 Answer: Use `text-decoration: none;` in CSS

**Q3:** How do you make links look like buttons?

* 👆 Answer: Add `background-color`, `padding`, `text-align: center`, `display: inline-block`, and `text-decoration: none`

**Q4:** How do you change cursor for links?

* 👆 Answer: Use `cursor` property, e.g., `cursor: pointer;`

**Q5:** How do you write Tailwind CSS for links?

* 👆 Answer: Use utility classes like `text-color`, `hover:text-color`, `bg-color`, `hover:bg-color`, `px`, `py`, etc.

---

## 10. Diagram 🖼️

```
Link States Diagram:

:link  ---> Normal (🔗)
:visited ---> Visited (👀)
:hover ---> Hover (🖱️)
:active ---> Active/Clicked (✋)
```

---

**End of CSS Links Guide 🏁**
