# 🖌️ CSS Dimensions (Height & Width)

CSS dimensions are used to control the size of HTML elements. This includes **height, width, min-height, min-width, max-height, max-width**.

---

## 📐 CSS Properties

| Property     | Description                           |
| ------------ | ------------------------------------- |
| `height`     | Sets the height of an element         |
| `width`      | Sets the width of an element          |
| `max-height` | Sets the maximum height of an element |
| `max-width`  | Sets the maximum width of an element  |
| `min-height` | Sets the minimum height of an element |
| `min-width`  | Sets the minimum width of an element  |

---

## 🖊️ Syntax

```css
/* Height & Width */
selector {
  height: 200px;   /* or %, auto, inherit */
  width: 50%;      /* or px, %, auto */
}

/* Max & Min */
selector {
  max-width: 600px;
  min-width: 300px;
  max-height: 400px;
  min-height: 100px;
}
```

## 🖼️ Examples

1️⃣ Height & Width

```css
div {
  height: 200px;
  width: 50%;
  background-color: powderblue;
}
```

2️⃣ Fixed Pixel Dimensions

```css
div {
  height: 100px;
  width: 500px;
  background-color: powderblue;
}
```

3️⃣ Max-width Example

```css
.div1 {
  max-width: 500px;
  background-color: powderblue;
}

.div2 {
  width: 500px;
  background-color: powderblue;
}
```

4️⃣ Width + Max-width

```css
.div1 {
  width: 100%;
  max-width: 900px;
  background-color: powderblue;
}
```

🔧 Tailwind CSS Equivalents

| CSS Property | Tailwind Class                                     |
| ------------ | -------------------------------------------------- |
| height       | h-16, h-64, h-full, h-screen                       |
| width        | w-16, w-64, w-full, w-screen                       |
| max-width    | max-w-xs, max-w-sm, max-w-md, max-w-lg, max-w-full |
| min-width    | min-w-0, min-w-full                                |
| max-height   | max-h-0, max-h-full                                |
| min-height   | min-h-0, min-h-full                                |

Example: Tailwind CSS

```html
<div class="w-1/2 h-64 bg-blue-200 max-w-lg">
  Tailwind width & height example
</div>
```

❓ Interview Questions & Answers

**Q1:** What is the difference between width and max-width?
**👉** width sets a fixed width, max-width limits the maximum width the element can grow.

**Q2:** What happens if width > max-width?
**👉** The max-width value will be applied.

**Q3:** Can height and width accept percentage values?
**👉** ✅ Yes, percentages are relative to the parent element.

**Q4:** How to maintain a responsive element?
**👉** Use max-width: 100% or Tailwind max-w-full to scale elements responsively.

**Q5:** How to set both min and max sizes?
**👉** Use min-width, max-width, min-height, max-height to restrict element size.

**Q6:** Tailwind equivalent of width: 50%?
**👉** w-1/2

📊 Diagram - CSS Box Model with Dimensions

```text
+---------------------------+
|         Margin            |
|  +---------------------+  |
|  |       Border        |  |
|  |  +---------------+  |  |
|  |  |   Padding     |  |  |
|  |  |  +---------+  |  |  |
|  |  |  | Content |  |  |  |
|  |  |  +---------+  |  |  |
|  |  +---------------+  |  |
|  +---------------------+  |
+---------------------------+
```

Width/Height → Content area
Padding → Inside content area
Border → Surrounds content + padding
Margin → Outside the border

📝 Notes

* Always consider box-sizing (content-box vs border-box) to control total element size.
* Percentages are relative to parent dimensions.
* Use max-width and min-width for responsive layouts.
