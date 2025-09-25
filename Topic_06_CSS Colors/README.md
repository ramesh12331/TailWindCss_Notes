# 🎨 CSS Colors Guide

In CSS, colors are used to style HTML elements. You can define colors using **predefined color names** or values like **RGB, HEX, HSL, RGBA, HSLA**.

---

## 📌 Table of Contents

1. 🎨 [CSS Color Names](#css-color-names)
2. 🖌️ [CSS Background Color](#css-background-color)
3. 📝 [CSS Text Color](#css-text-color)
4. 🖍️ [CSS Border Color](#css-border-color)
5. 🌈 [CSS Color Values](#css-color-values)
6. ⚡ [Tailwind CSS Syntax](#tailwind-css-syntax)
7. ❓ [Exercise](#exercise)

---

## 🎨 CSS Color Names

CSS supports **140 standard color names**. Some examples:

* 🍅 Tomato
* 🟠 Orange
* 🔵 DodgerBlue
* 🟢 MediumSeaGreen
* ⚪ Gray
* 🟣 SlateBlue
* 💜 Violet
* ⚪ LightGray

**Example:**

```html
<h1 style="color:Tomato;">🍅 Hello World</h1>
<p style="color:DodgerBlue;">🔵 Lorem ipsum...</p>
<p style="color:MediumSeaGreen;">🟢 Ut wisi enim...</p>
```

## 🖌️ CSS Background Color

You can set the background color for elements.

**Example:**

```html
<h1 style="background-color:DodgerBlue;">🔵 Hello World</h1>
<p style="background-color:Tomato;">🍅 Lorem ipsum dolor sit amet...</p>
```

## 📝 CSS Text Color

Change the text color of elements:

**Example:**

```html
<h1 style="color:Tomato;">🍅 Hello World</h1>
<p style="color:DodgerBlue;">🔵 Lorem ipsum...</p>
<p style="color:MediumSeaGreen;">🟢 Ut wisi enim...</p>
```

## 🖍️ CSS Border Color

You can style the border color of elements:

**Example:**

```html
<h1 style="border:2px solid Tomato;">🍅 Hello World</h1>
<h1 style="border:2px solid DodgerBlue;">🔵 Hello World</h1>
<h1 style="border:2px solid Violet;">💜 Hello World</h1>
```

## 🌈 CSS Color Values

Colors can also be specified with RGB, HEX, HSL, RGBA, HSLA:

**Same as "Tomato":**

```css
rgb(255, 99, 71);  /* 🍅 */
#ff6347;            /* 🍅 */
hsl(9, 100%, 64%);   /* 🍅 */
```

**50% transparent version of "Tomato":**

```css
rgba(255, 99, 71, 0.5);  /* 🍅 */
hsla(9, 100%, 64%, 0.5); /* 🍅 */
```

**Example in HTML:**

```html
<h1 style="background-color:rgb(255, 99, 71);">🍅 RGB</h1>
<h1 style="background-color:#ff6347;">🍅 HEX</h1>
<h1 style="background-color:hsl(9, 100%, 64%);">🍅 HSL</h1>
<h1 style="background-color:rgba(255, 99, 71, 0.5);">🍅 RGBA</h1>
<h1 style="background-color:hsla(9, 100%, 64%, 0.5);">🍅 HSLA</h1>
```

## ⚡ Tailwind CSS Syntax

Tailwind uses utility classes for colors:

| 🔹 Property      | CSS Example                   | Tailwind Class    |
| ---------------- | ----------------------------- | ----------------- |
| 📝 Text color    | color: Tomato;                | text-red-500      |
| 🖌️ Background   | background-color: DodgerBlue; | bg-blue-500       |
| 🖍️ Border color | border: 2px solid Violet;     | border-purple-500 |

**Example:**

```html
<button class="bg-red-500 text-white border-2 border-purple-500 px-4 py-2 rounded">
  🖌️ Click Me
</button>
```

## ❓ Exercise

**Question:** Which of the following is a predefined color name in CSS?

* 🔴 RedGreenBlue
* ✅ 🔵 blue
* RGB
* HEX

**Answer:** ✅ 🔵 blue

## ✅ Summary

* CSS supports predefined color names and value-based colors (RGB, HEX, HSL, RGBA, HSLA).
* Background, text, and borders can all use colors.
* Tailwind CSS simplifies color styling using utility classes.
* Always test colors in your design for readability and contrast.
