echo "# 🌐 CSS Units

CSS uses **units** to define lengths like width, margin, padding, font-size, etc.
A **length value** is a number followed by a unit: px, em, rem, %, etc.

CSS units are divided into **two types**:  
1. 📏 **Absolute Units** – fixed, do not scale  
2. 📐 **Relative Units** – scale with parent, root, or viewport

---

## 📘 Syntax

\`\`\`css
selector {
  property: length; /* e.g., 16px, 2em, 1.5rem */
}
\`\`\`

---

## 📏 Absolute Units

Absolute units **do not change** with screen size. Mostly used for print or fixed layouts.

| Unit | Description |
|------|-------------|
| px   | Pixels (1px = 1/96th of 1in) |
| cm   | Centimeters |
| mm   | Millimeters |
| in   | Inches (1in = 96px = 2.54cm) |
| pt   | Points (1pt = 1/72 of 1in) |
| pc   | Picas (1pc = 12pt) |

**Example – Font size with px**:

\`\`\`css
h1 { font-size: 40px; }
h2 { font-size: 30px; }
p  { font-size: 16px; }
\`\`\`

⚠️ **Note:** No space between the number and the unit. 0 can omit the unit.

---

## 📐 Relative Units

Relative units **scale** according to parent, root, or viewport. Best for responsive design.

| Unit  | Description |
|-------|-------------|
| em    | Relative to **parent** font-size |
| rem   | Relative to **root <html>** font-size |
| %     | Relative to parent element |
| vw    | 1% of viewport width |
| vh    | 1% of viewport height |
| vmin  | 1% of smaller viewport dimension |
| vmax  | 1% of larger viewport dimension |
| ex    | Relative to x-height of font (rare) |
| ch    | Relative to width of 0 |
| fr    | Fractional unit in Grid layout |

💡 **Tip:** Use em and rem for **scalable, responsive websites**.

---

### Example – Font size with em

\`\`\`css
body { font-size: 16px; } /* base font size */

h1 { font-size: 2.5em; }  /* 2.5 * 16 = 40px */
h2 { font-size: 1.875em;} /* 1.875 * 16 = 30px */
p  { font-size: 1em; }    /* 1 * 16 = 16px */
\`\`\`

📊 **Diagram:**

Parent font-size = 16px
  ├─ h1 = 2.5em → 40px
  ├─ h2 = 1.875em → 30px
  └─ p = 1em → 16px

---

### Example – Font size with rem

\`\`\`css
html { font-size: 16px; } /* root font size */

h1 { font-size: 2.5rem; }  /* 2.5 * 16 = 40px */
h2 { font-size: 1.875rem;} /* 1.875 * 16 = 30px */
p  { font-size: 1rem; }    /* 1 * 16 = 16px */
\`\`\`

📊 **Diagram:**

Root font-size = 16px
  ├─ h1 = 2.5rem → 40px
  ├─ h2 = 1.875rem → 30px
  └─ p = 1rem → 16px

---

## ✨ Tailwind CSS Equivalents

| CSS | Tailwind |
|-----|----------|
| font-size: 16px | text-base |
| font-size: 30px | text-2xl |
| font-size: 40px | text-4xl |

**Example:**

\`\`\`html
<h1 class=\"text-4xl\">Heading 1</h1>
<h2 class=\"text-2xl\">Heading 2</h2>
<p class=\"text-base\">Paragraph text</p>
\`\`\`

---

## ✋ Interview Q&A

🙋 **Q1:** What is the difference between px, em, and rem?  
👉 **A1:**  
- px = fixed, does not scale  
- em = relative to **parent** font-size  
- rem = relative to **root <html>** font-size  

🙋 **Q2:** Which unit is better for responsive designs?  
👉 **A2:** em and rem because they scale with parent or root font-size  

🙋 **Q3:** Can you mix absolute and relative units?  
👉 **A3:** Yes, but for responsive layouts, prefer **relative units**  

🙋 **Q4:** How does % work in CSS?  
👉 **A4:** % is relative to the **parent element’s** corresponding dimension  

🙋 **Q5:** What are viewport units (vw, vh) used for?  
👉 **A5:** To size elements relative to the **browser window**, great for responsive layouts  

---

✅ **Best Practices**

- Use **relative units** (em, rem, %, vw, vh) for **responsive websites**  
- Use **absolute units** (px, cm) only for **fixed-size designs or print**  
- Use rem for global consistency, em for nested scaling  
- Avoid mixing too many units; maintain readability and scalability
" > README.md
