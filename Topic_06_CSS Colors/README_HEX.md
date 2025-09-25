# 🎨 CSS HEX Colors Guide

HEX colors are a way to represent colors in CSS using **hexadecimal values**. They define colors with the format **#RRGGBB**, where **RR, GG, BB** represent red, green, and blue components (0–255 in decimal, 00–FF in hex).

---

## 📌 Table of Contents

1. ⚡ [HEX Color Syntax](#hex-color-syntax)
2. 💡 [Examples](#examples)
3. 🎨 [Shades of Gray](#shades-of-gray)
4. ✂️ [3-Digit HEX Shorthand](#3-digit-hex-shorthand)
5. ⚡ [Tailwind CSS Syntax](#tailwind-css-syntax)
6. ❓ [Interview Questions & Answers](#interview-questions--answers)
7. 📊 [Diagram](#diagram)

---

## ⚡ HEX Color Syntax

```css
/* 6-digit HEX */
#RRGGBB
🔴 RR → Red (00–FF)
🟢 GG → Green (00–FF)
🔵 BB → Blue (00–FF)
```

**Examples:**

```css
#ff0000  /* 🔴 Red */
#00ff00  /* 🟢 Green */
#0000ff  /* 🔵 Blue */
#000000  /* ⚫ Black */
#ffffff  /* ⚪ White */
```

## 💡 Examples in HTML

```html
<h1 style="color:#ff0000;">🔴 Red Text</h1>
<h1 style="color:#0000ff;">🔵 Blue Text</h1>
<h1 style="color:#3cb371;">🟢 MediumSeaGreen Text</h1>
<h1 style="color:#ee82ee;">💜 Violet Text</h1>
<h1 style="color:#ffa500;">🟠 Orange Text</h1>
<h1 style="color:#6a5acd;">🔵 SlateBlue Text</h1>
```

## 🎨 Shades of Gray

Shades of gray use equal values for R, G, and B:

```html
<div style="background-color:#3c3c3c;">⬛ Dark Gray</div>
<div style="background-color:#616161;">⬛ Gray</div>
<div style="background-color:#787878;">⬛ Medium Gray</div>
<div style="background-color:#b4b4b4;">⬜ Light Gray</div>
<div style="background-color:#f0f0f0;">⬜ Lighter Gray</div>
<div style="background-color:#f9f9f9;">⬜ Almost White</div>
```

## ✂️ 3-Digit HEX Shorthand

Format: `#rgb` — Each digit is repeated to form the 6-digit equivalent.

**Example:**

```css
body {
  background-color: #fc9; /* 🟠 same as #ffcc99 */
}

h1 {
  color: #f0f; /* 💜 same as #ff00ff */
}

p {
  color: #b58; /* 🟣 same as #bb5588 */
}
```

## ⚡ Tailwind CSS Syntax

Tailwind uses predefined color classes or custom HEX codes.

| 🎨 CSS HEX | 🏷 Tailwind Class    |
| ---------- | -------------------- |
| #ff0000    | text-red-500         |
| #00ff00    | text-green-500       |
| #0000ff    | text-blue-500        |
| #3cb371    | text-green-400       |
| #f0f0f0    | bg-gray-100          |
| #fc9       | Custom: bg-[#ffcc99] |

**HTML Example:**

```html
<h1 class="text-red-500">🔴 Red Text</h1>
<h1 class="text-green-500">🟢 Green Text</h1>
<h1 class="text-blue-500">🔵 Blue Text</h1>
<div class="bg-[#ffcc99] p-4">🟠 Background Color</div>
```

## ❓ Interview Questions & Answers

**Q1:** What does #RRGGBB mean in HEX?

* A: It represents Red, Green, Blue components in hexadecimal (00–FF).

**Q2:** How do you write white and black in HEX?

* ⚪ White: #ffffff
* ⚫ Black: #000000

**Q3:** What is a 3-digit HEX code?

* A: ✂️ It's a shorthand for 6-digit HEX codes when each pair has identical digits. Example: #fc9 → #ffcc99.

**Q4:** Can Tailwind use HEX colors?

* A: ✅ Yes, either predefined classes (text-red-500) or custom HEX (text-[#ff6347]).

## 📊 Diagram

```
       HEX Color Model
 ┌───────────────────────────┐
 │ 🔴 RR (00-FF) Red         │
 │ 🟢 GG (00-FF) Green       │
 │ 🔵 BB (00-FF) Blue        │
 └───────────┬───────────────┘
             ▼
       Combine values
             ▼
    Create desired color 🎨
```

## ✅ Summary

* HEX values are #RRGGBB or #rgb (shorthand).
* Each component ranges from 00–FF (0–255 decimal).
* Tailwind can use predefined classes or custom HEX colors.
* Useful for precise colors, shades, and gradients.

## ❓ Exercise

**Question:** Which HEX value represents white?

* #000000
* #ff0000
* ✅ #ffffff
* #00ff00
