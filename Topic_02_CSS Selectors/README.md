# 🎯 CSS Selectors -- Beginner to Pro

CSS selectors are used to find (select) the HTML elements you want to
style.

------------------------------------------------------------------------

## 📌 1. Categories of CSS Selectors

-   **Simple Selectors** → Based on name, id, or class.\
-   **Combinator Selectors** → Based on element relationships.\
-   **Pseudo-class Selectors** → Based on element states.\
-   **Pseudo-elements Selectors** → Style a part of an element.\
-   **Attribute Selectors** → Based on attributes & values.

This guide explains basic CSS selectors with examples.

------------------------------------------------------------------------

## 📌 2. CSS Element Selector

👉 Selects HTML elements by tag name.

``` css
p {
  text-align: center;
  color: red;
}
```

✅ Styles all `<p>` elements → red & center-aligned.

------------------------------------------------------------------------

## 📌 3. CSS ID Selector

👉 Selects element with a unique id using `#`.

``` css
#para1 {
  text-align: center;
  color: red;
}
```

✅ Styles only element with `id="para1"`.

⚠️ Note: An id must be unique per page and cannot start with a number.

------------------------------------------------------------------------

## 📌 4. CSS Class Selector

👉 Selects elements with a class attribute using `.`.

``` css
.center {
  text-align: center;
  color: red;
}
```

✅ Applies to all elements with `class="center"`.

🔹 Apply only to specific elements:

``` css
p.center {
  text-align: center;
  color: red;
}
```

🔹 Multiple classes:

``` html
<p class="center large">This paragraph refers to two classes.</p>
```

⚠️ Class names cannot start with a number.

------------------------------------------------------------------------

## 📌 5. CSS Universal Selector

👉 Selects all elements on the page using `*`.

``` css
* {
  text-align: center;
  color: blue;
}
```

✅ Affects every element.

------------------------------------------------------------------------

## 📌 6. CSS Grouping Selector

👉 Group multiple selectors using `,` to apply same styles.

``` css
h1, h2, p {
  text-align: center;
  color: red;
}
```

✅ Instead of repeating styles for each selector.

------------------------------------------------------------------------

## 📊 7. CSS Selectors Diagram

    +---------------------------+
    |  Selector   → p, #id, .class  |
    +---------------------------+
    |  Declaration Block { }     |
    |   property: value;         |
    |   property: value;         |
    +---------------------------+

------------------------------------------------------------------------

## 📌 8. CSS vs Tailwind CSS

✅ CSS Syntax:

``` css
p {
  color: red;
  text-align: center;
}
```

✅ Tailwind CSS Equivalent:

``` html
<p class="text-red-500 text-center">Hello World</p>
```

------------------------------------------------------------------------

## 📌 9. Summary Table

  ----------------------------------------------------------------------------
  Selector Type            Symbol        Example            Meaning
  ------------------------ ------------- ------------------ ------------------
  Element                  tag           `p {}`             Selects all `<p>`

  ID                       \#            `#para1 {}`        Selects element
                                                            with `id="para1"`

  Class                    .             `.center {}`       Selects all with
                                                            `class="center"`

  Universal                \*            `* {}`             Selects all
                                                            elements

  Grouping                 ,             `h1, p {}`         Groups selectors
  ----------------------------------------------------------------------------

------------------------------------------------------------------------

## 📌 10. Interview Questions & Answers

**Q1. What is a CSS Selector?**\
👉 It is a pattern used to select HTML elements to apply styles.

**Q2. Difference between ID & Class selectors?**\
👉 ID = unique, one element only.\
👉 Class = reusable, multiple elements.

**Q3. Can you apply multiple classes to an element?**\
👉 Yes, separate them with spaces → `<p class="center large">`.

**Q4. Which selector has higher specificity: ID or Class?**\
👉 ID selector has higher specificity.

**Q5. What is the Universal Selector?**\
👉 `*` applies styles to all elements on the page.

------------------------------------------------------------------------

✅ Now you have a complete guide on **CSS Selectors** with syntax,
diagrams, and interview prep 🚀
