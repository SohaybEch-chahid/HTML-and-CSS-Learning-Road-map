# CSS Borders

Borders are used to create outlines around elements.

They help separate content, improve design, and make layouts easier to understand.

---

# What is a Border?

A border sits between the margin and padding.

```text
Margin
  Border
    Padding
      Content
```

Example:

```css
div {
  border: 2px solid black;
}
```

Result:

A 2-pixel black border around the element.

---

# Border Syntax

A border consists of:

```css
border: width style color;
```

Example:

```css
border: 3px solid red;
```

Where:

- 3px = width
- solid = style
- red = color

---

# Border Width

Controls thickness.

```css
border-width: 5px;
```

Examples:

```css
border-width: 1px;
border-width: 2px;
border-width: 5px;
border-width: 10px;
```

---

# Border Style

Defines how the border looks.

```css
border-style: solid;
```

Available styles:

```css
solid
dashed
dotted
double
groove
ridge
inset
outset
none
hidden
```

Example:

```css
border-style: dashed;
```

---

# Border Color

Defines the border color.

```css
border-color: blue;
```

Examples:

```css
border-color: red;
border-color: #2563eb;
border-color: rgb(255, 0, 0);
```

---

# Individual Borders

Top:

```css
border-top: 2px solid red;
```

Right:

```css
border-right: 2px solid blue;
```

Bottom:

```css
border-bottom: 2px solid green;
```

Left:

```css
border-left: 2px solid orange;
```

---

# Border Radius

Creates rounded corners.

Example:

```css
border-radius: 10px;
```

Result:

Rounded corners instead of sharp edges.

---

# More Border Radius Examples

Small radius:

```css
border-radius: 5px;
```

Medium radius:

```css
border-radius: 10px;
```

Large radius:

```css
border-radius: 20px;
```

---

# Circle

Create a perfect circle.

HTML:

```html
<div class="circle"></div>
```

CSS:

```css
.circle {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background: blue;
}
```

---

# Different Radius Values

```css
border-radius: 10px 20px 30px 40px;
```

Order:

```text
Top Left
Top Right
Bottom Right
Bottom Left
```

---

# Border Shorthand

Instead of:

```css
border-width: 2px;
border-style: solid;
border-color: black;
```

Use:

```css
border: 2px solid black;
```

Much cleaner.

---

# Outline vs Border

Border:

```css
border: 2px solid blue;
```

Outline:

```css
outline: 2px solid red;
```

Difference:

- Border takes space
- Outline does not take space

---

# Box Shadow

Creates shadows around elements.

Syntax:

```css
box-shadow: horizontal vertical blur color;
```

Example:

```css
box-shadow: 2px 2px 5px gray;
```

---

# Soft Card Shadow

```css
box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
```

Very common in modern UI design.

---

# Strong Shadow

```css
box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
```

---

# Multiple Shadows

```css
box-shadow:
  0 2px 5px rgba(0, 0, 0, 0.1),
  0 5px 15px rgba(0, 0, 0, 0.2);
```

---

# Practical Card Example

HTML:

```html
<div class="card">
  <h2>Product Card</h2>
  <p>Description here</p>
</div>
```

CSS:

```css
.card {
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}
```

Result:

- Rounded corners
- Clean border
- Modern shadow

---

# Button Example

```css
button {
  border: none;
  border-radius: 8px;
  padding: 12px 20px;
  background: #2563eb;
  color: white;
}
```

Modern buttons usually use:

- border-radius
- box-shadow
- padding

---

# Common Mistakes

❌ Using very thick borders

```css
border: 10px solid black;
```

Usually looks bad.

---

❌ Using too many shadow effects

```css
box-shadow: 0 0 50px red;
```

Can look unprofessional.

---

# Best Practices

✅ Use subtle borders

```css
border: 1px solid #ddd;
```

✅ Use rounded corners

```css
border-radius: 8px;
```

✅ Use soft shadows

```css
box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
```

✅ Keep design consistent

---

# Summary

Important properties:

```css
border
border-width
border-style
border-color
border-radius
outline
box-shadow
```

Most commonly used:

```css
.card {
  border: 1px solid #ddd;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}
```

Mastering borders and shadows is essential for creating modern, professional-looking websites.
