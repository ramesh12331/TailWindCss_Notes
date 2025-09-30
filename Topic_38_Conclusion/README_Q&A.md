# 📘 CSS & Tailwind Interview Q&A (All 37 Topics)

Quick reference with **questions and answers** for CSS and Tailwind, including icons for readability.

---

## Topic 01 – CSS Syntax ✍️

1️⃣ 👆 **Q:** What is CSS syntax?

✋ CSS syntax consists of a selector and a declaration block: `selector { property: value; }`

2️⃣ 👆 **Q:** Tailwind equivalent?

✋ Apply utility classes directly on HTML elements, e.g., `<p class="text-red-500 text-base">Hello</p>`

---

## Topic 02 – CSS Selectors 🎯

1️⃣ 👆 **Q:** What are CSS selectors?

✋ Selectors target HTML elements to apply styling (tag, class, id, attribute).

2️⃣ 👆 **Q:** Tailwind approach?

✋ Tailwind uses classes as selectors: `<h1 class="text-blue-500">Heading</h1>`

---

## Topic 03 – How to Add CSS 🔗

1️⃣ 👆 **Q:** Ways to add CSS?

✋ Inline, internal (`<style>`), or external (`<link>`).

2️⃣ 👆 **Q:** Tailwind approach?

✋ Add classes directly to elements: `<p class="text-red-500">Text</p>`

---

## Topic 04 – CSS Comments 💬

1️⃣ 👆 **Q:** How do you write comments?

✋ `/* comment */` in CSS, `<!-- comment -->` in HTML.

2️⃣ 👆 **Q:** Tailwind comments?

✋ Use HTML comments since Tailwind is class-based.

---

## Topic 05 – CSS Errors ⚠️

1️⃣ 👆 **Q:** Common CSS errors?

✋ Typos, invalid properties, missing semicolons; browsers skip them.

2️⃣ 👆 **Q:** Tailwind invalid class?

✋ Classes not matching Tailwind config are ignored.

---

## Topic 06 – CSS Colors 🌈

1️⃣ 👆 **Q:** How to define colors in CSS?

✋ Names, HEX, RGB(A), HSL(A).

2️⃣ 👆 **Q:** Tailwind color classes?

✋ `text-red-500`, `bg-blue-200`, `border-green-700`.

---

## Topic 07 – CSS Backgrounds 🖼️

1️⃣ 👆 **Q:** CSS background shorthand?

✋ `background: color image repeat position / size;`

2️⃣ 👆 **Q:** Tailwind background classes?

✋ `bg-white`, `bg-no-repeat`, `bg-right-top`.

---

## Topic 08 – CSS Borders 📦

1️⃣ 👆 **Q:** CSS border shorthand?

✋ `border: width style color;`

2️⃣ 👆 **Q:** Tailwind border classes?

✋ `border-2`, `border-black`, `rounded-lg`.

---

## Topic 09 – CSS Margins ↔️

1️⃣ 👆 **Q:** Margin usage?

✋ Outer spacing around elements.

2️⃣ 👆 **Q:** Tailwind margins?

✋ `m-4`, `mx-5`, `my-2`.

---

## Topic 10 – CSS Padding 📏

1️⃣ 👆 **Q:** Padding usage?

✋ Inner spacing between content and border.

2️⃣ 👆 **Q:** Tailwind padding?

✋ `p-4`, `px-5`, `py-2`.

---

## Topic 11 – Height, Width & Max-width 📐

1️⃣ 👆 **Q:** CSS sizing?

✋ `width: value; height: value; max-width: value;`

2️⃣ 👆 **Q:** Tailwind sizing?

✋ `w-24`, `h-auto`, `max-w-full`.

---

## Topic 12 – CSS Box Model 📦

1️⃣ 👆 **Q:** Components of box model?

✋ Content + Padding + Border + Margin.

2️⃣ 👆 **Q:** Tailwind box sizing?

✋ `box-border`, `box-content`.

---

## Topic 13 – CSS Outline ✒️

1️⃣ 👆 **Q:** Purpose of outline?

✋ Highlight elements without affecting layout.

2️⃣ 👆 **Q:** Tailwind outline classes?

✋ `focus:outline-orange-500`, `focus:outline-4`.

---

## Topic 14 – CSS Text 📝

1️⃣ 👆 **Q:** Common text properties?

✋ `color`, `text-align`, `text-decoration`, `letter-spacing`

2️⃣ 👆 **Q:** Tailwind text classes?

✋ `text-center`, `underline`, `tracking-wide`.

---

## Topic 15 – CSS Fonts 🔤

1️⃣ 👆 **Q:** CSS font properties?

✋ `font-family`, `font-size`, `font-weight`, `line-height`

2️⃣ 👆 **Q:** Tailwind font classes?

✋ `font-sans`, `text-base`, `font-bold`, `leading-loose`.

---

## Topic 16 – CSS Icons 🎨

1️⃣ 👆 **Q:** Ways to add icons?

✋ Font icons (Font Awesome), SVG, or background images.

2️⃣ 👆 **Q:** Tailwind SVG icon?

✋ `<svg class="w-6 h-6 text-gray-500"></svg>`

---

## Topic 17 – CSS Links 🔗

1️⃣ 👆 **Q:** CSS link states?

✋ `:link`, `:visited`, `:hover`, `:active`, `:focus`

2️⃣ 👆 **Q:** Tailwind link hover?

✋ `hover:text-red-500`, `focus:text-blue-500`.

---

## Topic 18 – CSS Lists 📋

1️⃣ 👆 **Q:** List properties?

✋ `list-style-type`, `list-style-position`

2️⃣ 👆 **Q:** Tailwind lists?

✋ `list-disc`, `list-decimal`, `list-inside`, `list-outside`.

---

## Topic 19 – CSS Tables 📊

1️⃣ 👆 **Q:** CSS table properties?

✋ `border-collapse`, `border-spacing`, `text-align`, `vertical-align`

2️⃣ 👆 **Q:** Tailwind tables?

✋ `border-collapse`, `border`, `border-gray-400`, `text-left`.

---

## Topic 20 – CSS Display 📐

1️⃣ 👆 **Q:** Display types?

✋ `block`, `inline`, `inline-block`, `flex`, `grid`, `none`

2️⃣ 👆 **Q:** Tailwind display?

✋ `block`, `inline`, `inline-block`, `flex`, `grid`, `hidden`

---

## Topic 21 – CSS Max-width 📏

1️⃣ 👆 **Q:** Purpose of max-width?

✋ Limit element width for responsive design.

2️⃣ 👆 **Q:** Tailwind max-width?

✋ `max-w-xs`, `max-w-md`, `max-w-screen-lg`.

---

## Topic 22 – CSS Positioning 📍

1️⃣ 👆 **Q:** Position values?

✋ `static`, `relative`, `absolute`, `fixed`, `sticky`

2️⃣ 👆 **Q:** Tailwind positioning?

✋ `relative`, `absolute`, `fixed`, `sticky`, `top-0`, `left-4`

---

## Topic 23 – CSS z-index 🔝

1️⃣ 👆 **Q:** What is z-index?

✋ Controls stacking order of positioned elements.

2️⃣ 👆 **Q:** Tailwind z-index?

✋ `z-10`, `z-50`, `z-auto`.

---

## Topic 24 – CSS Overflow 📜

1️⃣ 👆 **Q:** Overflow properties?

✋ `visible`, `hidden`, `scroll`, `auto`

2️⃣ 👆 **Q:** Tailwind overflow?

✋ `overflow-auto`, `overflow-scroll`, `overflow-hidden`, `overflow-x-auto`

---

## Topic 25 – CSS Float ↔️

1️⃣ 👆 **Q:** Float usage?

✋ Move elements left or right and wrap text.

2️⃣ 👆 **Q:** Tailwind float?

✋ `float-left`, `float-right`, `float-none`

---

## Topic 26 – CSS Inline-Block 📦

1️⃣ 👆 **Q:** Inline-block usage?

✋ Flows inline but accepts width/height.

2️⃣ 👆 **Q:** Tailwind inline-block?

✋ `inline-block w-24 h-10`

---

## Topic 27 – CSS Align 🎯

1️⃣ 👆 **Q:** Alignment properties?

✋ `text-align`, `align-items`, `justify-content`

2️⃣ 👆 **Q:** Tailwind alignment?

✋ `text-center`, `items-center`, `justify-center`

---

## Topic 28 – CSS Combinators 🔗

1️⃣ 👆 **Q:** Types of combinators?

✋ Descendant (`A B`), Child (`A > B`), Adjacent sibling (`A + B`), General sibling (`A ~ B`).

2️⃣ 👆 **Q:** Tailwind equivalent?

✋ Use `group` and `group-hover` for nested hover styles.

---

## Topic 29 – CSS Pseudo-classes 🧩

1️⃣ 👆 **Q:** What are pseudo-classes?

✋ Target element states like `hover`, `focus`, `first-child`, `nth-child`.

2️⃣ 👆 **Q:** Tailwind pseudo-class usage?

✋ `hover:text-red-500`, `focus:text-blue-500`, `first:font-bold`

---

## Topic 30 – CSS Pseudo-elements 🎭

1️⃣ 👆 **Q:** What are pseudo-elements?

✋ Style parts of elements or insert content (`::before`, `::after`, `::first-line`).

2️⃣ 👆 **Q:** Tailwind pseudo-elements?

✋ `before:content-['Note:_']`, `before:text-red-500`

---

## Topic 31 – CSS Opacity 🌫️

1️⃣ 👆 **Q:** Opacity values?

✋ `0` = invisible, `1` = fully visible.

2️⃣ 👆 **Q:** Tailwind opacity?

✋ `opacity-60`, `opacity-100`

---

## Topic 32 – CSS Units 📏

1️⃣ 👆 **Q:** Types of CSS units?

✋ Absolute (`px`, `cm`), Relative (`em`, `rem`, `%`, `vw`, `vh`, `vmin`, `vmax`).

2️⃣ 👆 **Q:** Tailwind units?

✋ `w-1/2`, `text-2xl`, `h-32`

---

## Topic 33 – CSS !important ❗

1️⃣ 👆 **Q:** What does !important do?

✋ Forces a CSS rule to override others; use sparingly.

2️⃣ 👆 **Q:** Tailwind important?

✋ `!text-red-500`

---

## Topic 34 – CSS Math Functions ➗

1️⃣ 👆 **Q:** Common math functions?

✋ `calc()`, `min()`, `max()`, `clamp()`

2️⃣ 👆 **Q:** Tailwind math functions?

✋ `w-[calc(100%-50px)]`, `text-[clamp(1.5rem,3vw,3rem)]`

---

## Topic 35 – CSS Math Functions (Advanced) 🧮

1️⃣ 👆 **Q:** Usage of clamp?

✋ Bound responsive values between min and max.

2️⃣ 👆 **Q:** Tailwind advanced math?

✋ `text-[clamp(1.5rem,3vw,3rem)]`, `w-[max(200px,50%)]`

---

## Topic 36 – Optimizing CSS ⚡

1️⃣ 👆 **Q:** Ways to optimize CSS?

✋ Minify, use shorthand, combine files, remove unused styles.

2️⃣ 👆 **Q:** Tailwind optimization?

✋ Use utility classes efficiently, purge unused classes.

---

## Topic 37 – CSS Accessibility Styling ♿

1️⃣ 👆 **Q:** What is CSS accessibility?

✋ Design for readability, focus visibility, and inclusive UX.

2️⃣ 👆 **Q:** Tailwind accessibility classes?

✋ `focus:outline-4`, `focus:outline-orange-500`, `motion-reduce:transition-none`

3️⃣ 👆 **Q:** Best practices?

✋ High contrast, clear focus, reduce motion, responsive text.
