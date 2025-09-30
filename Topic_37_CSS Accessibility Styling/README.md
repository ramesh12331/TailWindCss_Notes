# ♿ CSS Accessibility Styling Guide

Design websites that are **accessible to everyone**, including users with disabilities.  
CSS accessibility styling improves **readability, navigation, and user experience**.

---

## 📌 Key Accessibility Tips

### 1️⃣ Provide High Color Contrast
Text should be easily readable against its background.  
Especially important for users with **visual impairments or color blindness**.

**Good Example:**
```css
body {
  background-color: #ffffff;
  color: #000000;
}
Bad Example:

body {
  background-color: #eeeeee;
  color: #cccccc;
}

2️⃣ Use Readable Fonts, Font Size & Line Height
Use simple fonts, proper font size, and sufficient line height.
Use relative units like rem for scaling.

Good Example:

css
Copy code
body {
  font-family: Arial, sans-serif;
  font-size: 1rem;
  line-height: 1.6;
}
Bad Example:

css
Copy code
body {
  font-family: Georgia, serif;
  font-size: 12px;
  font-style: italic;
  font-variant: small-caps;
  line-height: 90%;
}
3️⃣ Have Visible Focus Indicators
Interactive elements like links, buttons, and inputs should have clear focus outlines.

css
Copy code
a:focus,
button:focus,
input:focus {
  outline: 2px solid orange;
}
4️⃣ Avoid Hiding Focus
Never remove focus outlines without replacement.

❌ Bad Example:

css
Copy code
button:focus {
  outline: none;
}
✅ Good Example:

css
Copy code
button:focus {
  outline: 2px solid orange;
}
5️⃣ Use CSS + Semantic HTML
Use CSS for styling and semantic HTML for structure.

css
Copy code
nav {
  background-color: #333333;
  color: white;
}

aside {
  background-color: #333333;
  color: white;
}
Semantic HTML elements:
<header>, <nav>, <main>, <footer>, <section>, <article>, <aside>

6️⃣ Respect User Preferences
Some users prefer reduced motion. Use prefers-reduced-motion media query.

css
Copy code
@media (prefers-reduced-motion: reduce) {
  * {
    animation: none !important;
    transition: none !important;
  }
}
📊 Diagram (Summary)
High contrast text → easier to read

Readable fonts → better UX

Focus outlines → keyboard navigation

Semantic HTML → clear structure

Reduced motion → respects user preference

✨ Tailwind CSS Examples
High contrast text:

html
Copy code
<p class="text-black bg-white">High contrast text</p>
Focus outline:

html
Copy code
<button class="focus:outline-orange-500 focus:outline-2">Click Me</button>
Readable font & line height:

html
Copy code
<p class="font-sans text-base leading-relaxed">Accessible paragraph</p>
Reduced motion:

html
Copy code
<div class="motion-safe:animate-bounce motion-reduce:animate-none">Bounce Box</div>
✋ Interview Q&A
🙋 Q1: Why is CSS accessibility important?
👉 A1: Ensures websites are usable by everyone, including users with disabilities.

🙋 Q2: What is good color contrast?
👉 A2: Text and background colors should differ enough to be readable.

🙋 Q3: Why use :focus styles?
👉 A3: Helps keyboard and screen-reader users know which element is active.

🙋 Q4: What is prefers-reduced-motion?
👉 A4: A media query to respect users who prefer less animation.

🙋 Q5: Why use semantic HTML?
👉 A5: Provides better structure and accessibility for assistive technologies.

✅ Best Practices
High contrast text for readability

Easily readable fonts, font size, and line height

Keep focus outlines visible

Use semantic HTML

Respect user motion preferences