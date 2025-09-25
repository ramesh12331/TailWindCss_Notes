# 🟦 CSS Borders Guide

CSS **border properties** allow you to set the **style, width, and color** of an element's border, including **rounded corners**.

---

## 📌 Table of Contents

1. 🎨 [Border Style](#border-style)
2. 📏 [Border Width](#border-width)
3. 🌈 [Border Color](#border-color)
4. 🔄 [Individual Sides](#individual-sides)
5. ⚡ [Border Shorthand](#border-shorthand)
6. ⭕ [Border Radius (Rounded Borders)](#border-radius-rounded-borders)
7. ⚡ [Tailwind CSS Syntax](#tailwind-css-syntax)
8. ❓ [Interview Questions & Answers](#interview-questions--answers)
9. 📊 [Diagram](#diagram)
10. ✅ [Summary](#summary)

---

## 🎨 Border Style

The `border-style` property defines **what kind of border** to display:

| Style    | Description         |
| -------- | ------------------- |
| `dotted` | Dotted border ⚫⚫⚫   |
| `dashed` | Dashed border ─ ─ ─ |
| `solid`  | Solid border ─────  |
| `double` | Double border ═ ═ ═ |
| `groove` | 3D grooved border   |
| `ridge`  | 3D ridged border    |
| `inset`  | 3D inset border     |
| `outset` | 3D outset border    |
| `none`   | No border ❌         |
| `hidden` | Hidden border       |

**Example:**

```css
p.dotted { border-style: dotted; }
p.dashed { border-style: dashed; }
p.solid { border-style: solid; }
p.double { border-style: double; }
p.groove { border-style: groove; }
p.ridge { border-style: ridge; }
```

Multiple values for top, right, bottom, left:

```css
p {
  border-style: dotted solid double dashed;
}
```

## 📏 Border Width

```css
p.one { border-style: solid; border-width: 5px; }
p.two { border-style: solid; border-width: medium; }
p.three { border-style: dotted; border-width: 2px; }
p.four { border-style: dotted; border-width: thick; }
```

Specific sides:

```css
p.one { border-width: 5px 20px; }       /* top/bottom 5px, sides 20px */
p.two { border-width: 20px 5px; }       /* top/bottom 20px, sides 5px */
p.three { border-width: 25px 10px 4px 35px; } /* top, right, bottom, left */
```

## 🌈 Border Color

```css
p.one { border-style: solid; border-color: red; }
p.two { border-style: solid; border-color: green; }
p.three { border-style: dotted; border-color: blue; }
```

Multiple sides:

```css
p.one { border-color: red green blue yellow; } /* top, right, bottom, left */
```

HEX, RGB, HSL values:

```css
border-color: #ff0000;        /* HEX */
border-color: rgb(255,0,0);   /* RGB */
border-color: hsl(0,100%,50%);/* HSL */
```

## 🔄 Individual Sides

```css
p {
  border-top-style: dotted;
  border-right-style: solid;
  border-bottom-style: dotted;
  border-left-style: solid;
}
```

Shorthand border-style can replace individual sides:

```css
/* 4 values */
border-style: dotted solid double dashed;
/* 3 values */
border-style: dotted solid double;
/* 2 values */
border-style: dotted solid;
/* 1 value */
border-style: dotted;
```

## ⚡ Border Shorthand

```css
p { border: 5px solid red; }
p { border-left: 6px solid blue; }
p { border-bottom: 4px dashed green; }
```

## ⭕ Border Radius (Rounded Borders)

```css
p {
  border: 2px solid red;
  border-radius: 5px; /* small round */
}

p.round { border-radius: 10px; }
p.rounder { border-radius: 20px; }
p.roundest { border-radius: 50px; }
```

## ⚡ Tailwind CSS Syntax

**Border Style:**

```html
<div class="border border-solid border-red-500 p-4">
  Solid Red Border
</div>
```

**Border Width:**

```html
<div class="border-2 border-blue-500 p-4">
  2px Blue Border
</div>
```

**Individual Sides:**

```html
<div class="border-t-4 border-b-2 border-red-500 p-4">
  Top 4px, Bottom 2px
</div>
```

**Border Radius:**

```html
<div class="rounded-md border border-green-500 p-4">
  Rounded Border
</div>
<div class="rounded-full border border-blue-500 p-4">
  Fully Rounded
</div>
```

## ❓ Interview Questions & Answers

**Q1:** How do you set the border of an element?

* A: Using `border: width style color;`

**Q2:** What are the different border-style options?

* A: solid, dotted, dashed, double, groove, ridge, inset, outset, none, hidden

**Q3:** How do you set different borders for each side?

* A: Use border-top, border-right, border-bottom, border-left or border-style with 2–4 values

**Q4:** How do you make a border rounded?

* A: Use `border-radius: value;`

**Q5:** How do you set the color using HSL or HEX?

* A: `border-color: #ff0000;` or `border-color: hsl(0,100%,50%);`

## 📊 Diagram

```
CSS Borders
 ┌───────────────┐
 │ border-style   │ dotted, solid, dashed...
 │ border-width   │ px, thin, medium, thick
 │ border-color   │ name, HEX, RGB, HSL
 │ border-radius  │ rounded corners
 └───────────────┘
 └───────▶ Combine properties or use shorthand
```

## ✅ Summary

* `border-style` → type of border
* `border-width` → thickness
* `border-color` → color
* `border-radius` → rounded corners
* Individual sides can be styled separately
* Shorthand border combines width, style, color
* Tailwind provides utility classes for all border properties

## 🏁 Exercise

**Question:** How do you create a blue, dashed, 3px border on the bottom of a div with rounded corners?

* a) `border: 3px dashed blue; border-bottom: 3px; border-radius: 5px;` ✅
* b) `border-style: solid;`
* c) `border-radius: 0;`
* d) `border-width: 5px;`
