# 📘 Complete CSS Cheat Sheet (37 Topics)

Quick reference: definition, syntax, short example (shorthand where useful), and a 1-line summary.

---

## Topic 01 – CSS Syntax

📌 **Definition:** CSS syntax is rules made of a selector and declaration block.

💻 **Syntax:**
```css
selector { property: value; }
```

📝 **Example:**
```css
p { color: red; font-size: 16px; }
```

📖 **Summary:** Defines how CSS rules are written.

---

## Topic 02 – CSS Selectors

📌 **Definition:** Selectors target HTML elements to apply styles (tag, class, id, attribute).

💻 **Syntax:**
```css
selector { property: value; }
```

📝 **Example:**
```css
h1 { color: blue; }
```

📖 **Summary:** Choose elements to style.

---

## Topic 03 – How to Add CSS

📌 **Definition:** Add CSS inline, internal (<style>), or external (<link>).

💻 **Syntax:**
```css
Inline, <style>, <link rel="stylesheet">
```

📝 **Example:**
```css
<p style="color:red;">Text</p>
```

📖 **Summary:** Three ways to attach CSS to HTML.

---

## Topic 04 – CSS Comments

📌 **Definition:** Comments document code and are ignored by browsers.

💻 **Syntax:**
```css
/* comment */
```

📝 **Example:**
```css
p { color: red; /* makes text red */ }
```

📖 **Summary:** Use comments to explain CSS.

---

## Topic 05 – CSS Errors

📌 **Definition:** Errors come from typos or invalid syntax; browsers skip invalid declarations.

💻 **Syntax:**
```css
property: value;
```

📝 **Example:**
```css
p { colr: red; } /* typo */
```

📖 **Summary:** Fix syntax to prevent errors.

---

## Topic 06 – CSS Colors

📌 **Definition:** Colors via names, HEX, RGB(A), HSL(A).

💻 **Syntax:**
```css
color: name|#hex|rgb()|hsl();
```

📝 **Example:**
```css
h1 { color: #ff0000; }
```

📖 **Summary:** Use suitable color formats for needs.

---

## Topic 07 – CSS Backgrounds

📌 **Definition:** Backgrounds include color, image, position, repeat and shorthand.

💻 **Syntax:**
```css
background: color image repeat position / size;
```

📝 **Example:**
```css
body { background: #fff url('img_tree.png') no-repeat right top; }
```

📖 **Summary:** Set element background using shorthand.

---

## Topic 08 – CSS Borders

📌 **Definition:** Borders set width, style, color; shorthand available.

💻 **Syntax:**
```css
border: width style color;
```

📝 **Example:**
```css
p { border: 2px solid #000; }
```

📖 **Summary:** Add visible edge around elements.

---

## Topic 09 – CSS Margins

📌 **Definition:** Margins create outer space outside an element.

💻 **Syntax:**
```css
margin: top right bottom left;
```

📝 **Example:**
```css
div { margin: 10px 20px; }
```

📖 **Summary:** Controls spacing between elements.

---

## Topic 10 – CSS Padding

📌 **Definition:** Padding creates inner space between content and border.

💻 **Syntax:**
```css
padding: top right bottom left;
```

📝 **Example:**
```css
div { padding: 10px 20px; }
```

📖 **Summary:** Controls inner spacing of elements.

---

## Topic 11 – Height, Width & Max-width

📌 **Definition:** Set element dimensions and limit growth using max-width.

💻 **Syntax:**
```css
width: value; height: value; max-width: value;
```

📝 **Example:**
```css
img { width:100px; height:auto; max-width:100%; }
```

📖 **Summary:** Define and constrain element size.

---

## Topic 12 – CSS Box Model

📌 **Definition:** Box model = content + padding + border + margin; box-sizing alters calculations.

💻 **Syntax:**
```css
content + padding + border + margin
```

📝 **Example:**
```css
div { box-sizing: border-box; width: 200px; padding: 10px; }
```

📖 **Summary:** Explains sizing and spacing of elements.

---

## Topic 13 – CSS Outline

📌 **Definition:** Outline is drawn outside the border and doesn't affect layout.

💻 **Syntax:**
```css
outline: width style color;
```

📝 **Example:**
```css
button:focus { outline: 3px solid orange; }
```

📖 **Summary:** Highlight elements without changing layout.

---

## Topic 14 – CSS Text

📌 **Definition:** Text properties control alignment, decoration, spacing and transform.

💻 **Syntax:**
```css
color, text-align, text-decoration, letter-spacing;
```

📝 **Example:**
```css
p { text-align:center; text-decoration: underline; }
```

📖 **Summary:** Style textual content.

---

## Topic 15 – CSS Fonts

📌 **Definition:** Fonts set family, weight, style, size and fallbacks.

💻 **Syntax:**
```css
font-family: value; font-size: value; font-weight: value;
```

📝 **Example:**
```css
p { font: 16px/1.5 'Arial', sans-serif; }
```

📖 **Summary:** Control typography appearance.

---

## Topic 16 – CSS Icons

📌 **Definition:** Icons via icon fonts (Font Awesome) or SVGs and background images.

💻 **Syntax:**
```css
use <i> or SVG or background-image
```

📝 **Example:**
```css
<i class='fa fa-user'></i>
```

📖 **Summary:** Use scalable icons for UI.

---

## Topic 17 – CSS Links

📌 **Definition:** Style link states: normal, visited, hover, active, focus.

💻 **Syntax:**
```css
a:link, a:visited, a:hover, a:active, a:focus
```

📝 **Example:**
```css
a:hover { color: red; }
```

📖 **Summary:** Differentiate link interaction states.

---

## Topic 18 – CSS Lists

📌 **Definition:** Style bullets, numbers and list layout.

💻 **Syntax:**
```css
list-style-type: value; list-style-position: value;
```

📝 **Example:**
```css
ul { list-style-type: square; }
```

📖 **Summary:** Control list markers and spacing.

---

## Topic 19 – CSS Tables

📌 **Definition:** Style table borders, spacing, and layout.

💻 **Syntax:**
```css
border-collapse: value; border-spacing: value;
```

📝 **Example:**
```css
table { border-collapse: collapse; }
```

📖 **Summary:** Customize table appearance.

---

## Topic 20 – CSS Display

📌 **Definition:** Display property defines how an element is displayed in the flow.

💻 **Syntax:**
```css
display: block|inline|inline-block|flex|grid|none;
```

📝 **Example:**
```css
div { display: flex; }
```

📖 **Summary:** Determines layout model for elements.

---

## Topic 21 – CSS Max-width

📌 **Definition:** Max-width limits element width for responsive layouts.

💻 **Syntax:**
```css
max-width: value;
```

📝 **Example:**
```css
.container { max-width: 1200px; width: 100%; }
```

📖 **Summary:** Keeps layout within readable width.

---

## Topic 22 – CSS Positioning

📌 **Definition:** Position controls how elements are placed on the page.

💻 **Syntax:**
```css
position: static|relative|absolute|fixed|sticky;
```

📝 **Example:**
```css
div { position: absolute; top:10px; left:20px; }
```

📖 **Summary:** Controls placement and stacking.

---

## Topic 23 – CSS z-index

📌 **Definition:** z-index sets stacking order of positioned elements.

💻 **Syntax:**
```css
z-index: integer;
```

📝 **Example:**
```css
.modal { position: fixed; z-index: 9999; }
```

📖 **Summary:** Manage which elements sit on top.

---

## Topic 24 – CSS Overflow

📌 **Definition:** Overflow handles content outside an element's box.

💻 **Syntax:**
```css
overflow: visible|hidden|scroll|auto;
```

📝 **Example:**
```css
div { overflow: auto; }
```

📖 **Summary:** Controls scrollbars and clipping.

---

## Topic 25 – CSS Float

📌 **Definition:** Float moves elements left or right and allows text wrap.

💻 **Syntax:**
```css
float: left|right|none;
```

📝 **Example:**
```css
img { float: right; margin: 0 0 10px 10px; }
```

📖 **Summary:** Wrap text around elements.

---

## Topic 26 – CSS Inline-Block

📌 **Definition:** inline-block flows inline but accepts width/height.

💻 **Syntax:**
```css
display: inline-block;
```

📝 **Example:**
```css
div { display: inline-block; width: 200px; }
```

📖 **Summary:** Useful for horizontal layout of blocks.

---

## Topic 27 – CSS Align

📌 **Definition:** Alignment via text-align, vertical-align, or flex/grid properties.

💻 **Syntax:**
```css
text-align:center; align-items:center; justify-content:center;
```

📝 **Example:**
```css
.center { text-align:center; } .flex { display:flex; align-items:center; justify-content:center; }
```

📖 **Summary:** Align items horizontally/vertically.

---

## Topic 28 – CSS Combinators

📌 **Definition:** Combinators describe relationships between selectors.

💻 **Syntax:**
```css
A B, A > B, A + B, A ~ B
```

📝 **Example:**
```css
div > p { color: red; }
```

📖 **Summary:** Style elements based on hierarchy.

---

## Topic 29 – CSS Pseudo-classes

📌 **Definition:** Pseudo-classes target element states or structural positions.

💻 **Syntax:**
```css
:hover, :focus, :first-child, :nth-child()
```

📝 **Example:**
```css
li:nth-child(2) { color: red; }
```

📖 **Summary:** Apply styles based on state or position.

---

## Topic 30 – CSS Pseudo-elements

📌 **Definition:** Pseudo-elements style parts of elements or insert content.

💻 **Syntax:**
```css
::before, ::after, ::first-line, ::first-letter
```

📝 **Example:**
```css
p::before { content: 'Note: '; }
```

📖 **Summary:** Target sub-parts of an element.

---

## Topic 31 – CSS Opacity

📌 **Definition:** Opacity sets element transparency between 0 (transparent) and 1 (opaque).

💻 **Syntax:**
```css
opacity: 0..1;
```

📝 **Example:**
```css
img { opacity: 0.6; }
```

📖 **Summary:** Control transparency and layering effects.

---

## Topic 32 – CSS Units

📌 **Definition:** Units measure lengths: absolute (px, cm) and relative (em, rem, %, vw, vh).

💻 **Syntax:**
```css
px, em, rem, %, vw, vh, vmin, vmax
```

📝 **Example:**
```css
h1 { font-size: 2rem; } div { width: 50%; }
```

📖 **Summary:** Pick units for responsiveness.

---

## Topic 33 – CSS !important

📌 **Definition:** Forces a declaration to have highest priority; use sparingly.

💻 **Syntax:**
```css
property: value !important;
```

📝 **Example:**
```css
p { color: red !important; }
```

📖 **Summary:** Overrides other rules; avoid overuse.

---

## Topic 34 – CSS Math Functions

📌 **Definition:** calc(), min(), max(), clamp() let you compute values in CSS.

💻 **Syntax:**
```css
calc(expr), min(...), max(...), clamp(min, val, max)
```

📝 **Example:**
```css
div { width: calc(100% - 50px); }
```

📖 **Summary:** Create dynamic, calculated values.

---

## Topic 35 – CSS Math Functions (advanced)

📌 **Definition:** Use clamp/min/max for fluid typography and responsive sizing.

💻 **Syntax:**
```css
clamp(min, preferred, max)
```

📝 **Example:**
```css
h1 { font-size: clamp(1.5rem, 3vw, 3rem); }
```

📖 **Summary:** Bound responsive values between limits.

---

## Topic 36 – Optimizing CSS

📌 **Definition:** Reduce file size and improve performance (minify, combine, use shorthand).

💻 **Syntax:**
```css
minify, combine, use shorthand properties
```

📝 **Example:**
```css
/* shorthand */ margin:10px 20px; /* combine files & cache */
```

📖 **Summary:** Faster load times and better UX.

---

## Topic 37 – CSS Accessibility Styling

📌 **Definition:** Design for readability and inclusive UX: contrast, focus, reduced motion.

💻 **Syntax:**
```css
high-contrast colors, focus outlines, prefers-reduced-motion
```

📝 **Example:**
```css
button:focus { outline: 3px solid #ff9800; }
```

📖 **Summary:** Make sites usable for all users.

---

