# CSS Units

CSS units define the size of elements, text, spacing, and layouts.

Understanding units is essential for building responsive websites.

---

# Types of CSS Units

CSS units are divided into two categories:

1. Absolute Units
2. Relative Units

---

# Absolute Units

Absolute units have a fixed size.

Examples:

```css id="b9g6g8"
width: 300px;
font-size: 16px;
```

Common absolute units:

| Unit | Description |
| ---- | ----------- |
| px   | Pixels      |
| cm   | Centimeters |
| mm   | Millimeters |
| in   | Inches      |
| pt   | Points      |
| pc   | Picas       |

In web development, `px` is the most commonly used absolute unit.

---

# 1. px (Pixels)

Pixels are fixed units.

```css id="4b0wqx"
h1 {
  font-size: 32px;
}
```

Examples:

```css id="tspc7d"
width: 500px;
height: 300px;
margin: 20px;
padding: 10px;
```

Advantages:

✅ Easy to understand

✅ Precise sizing

Disadvantages:

❌ Less flexible for responsive design

---

# Relative Units

Relative units depend on another value.

They are better for responsive design.

---

# 2. % (Percentage)

Relative to the parent element.

HTML:

```html id="c70zv3"
<div class="container">
  <div class="box"></div>
</div>
```

CSS:

```css id="ggcb1s"
.container {
  width: 800px;
}

.box {
  width: 50%;
}
```

Result:

```text id="y0lnl6"
400px
```

Because 50% of 800px is 400px.

---

# 3. em

Relative to the font size of the parent.

```css id="31wvzs"
.parent {
  font-size: 20px;
}

.child {
  font-size: 2em;
}
```

Result:

```text id="mws6j5"
40px
```

Because:

```text id="s4vwqb"
2 × 20px = 40px
```

---

# 4. rem (Root EM)

Relative to the root element (`html`).

Default browser font size:

```text id="yq9rjc"
16px
```

Example:

```css id="6fwb2g"
font-size: 1rem;
```

Result:

```text id="zvwn92"
16px
```

Example:

```css id="w2gqj2"
font-size: 2rem;
```

Result:

```text id="0c4l4k"
32px
```

Because:

```text id="vbj7xm"
2 × 16px
```

Why use rem?

✅ Consistent sizing

✅ Better accessibility

✅ Easier responsive design

---

# em vs rem

Parent font size:

```css id="gmyutd"
.parent {
  font-size: 20px;
}
```

Child:

```css id="9pwbdi"
.child {
  font-size: 2em;
}
```

Result:

```text id="7u1v57"
40px
```

Using rem:

```css id="bfz9m8"
.child {
  font-size: 2rem;
}
```

Result:

```text id="njbr3m"
32px
```

Because rem uses the root font size.

---

# 5. vw (Viewport Width)

Relative to browser width.

```css id="r0m6cn"
width: 50vw;
```

Meaning:

```text id="95l9p2"
50% of screen width
```

Example:

```css id="53lqec"
.hero {
  width: 100vw;
}
```

---

# 6. vh (Viewport Height)

Relative to browser height.

```css id="24yvqs"
height: 100vh;
```

Meaning:

```text id="uq76d0"
100% of screen height
```

Example:

```css id="ptcb93"
.hero {
  height: 100vh;
}
```

Common for landing pages.

---

# 7. vmin

Uses the smaller viewport dimension.

```css id="p9uq8m"
font-size: 5vmin;
```

---

# 8. vmax

Uses the larger viewport dimension.

```css id="sxuwqz"
font-size: 5vmax;
```

---

# 9. fr (Fraction Unit)

Used with CSS Grid.

```css id="w8s8s5"
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```

Result:

```text id="vkj7w4"
3 equal columns
```

Example:

```css id="l9qjmc"
grid-template-columns: 1fr 2fr;
```

Result:

```text id="0tpjlwm"
Column 2 is twice as wide as Column 1
```

---

# Practical Examples

Text:

```css id="qf84dx"
font-size: 1rem;
```

Container:

```css id="v4r0a6"
width: 80%;
```

Hero Section:

```css id="rmjg9g"
height: 100vh;
```

Grid Layout:

```css id="lyvnlr"
grid-template-columns: repeat(3, 1fr);
```

---

# Best Practices

For text:

```css id="g5nr1l"
font-size: 1rem;
```

For layouts:

```css id="fj3z9k"
width: 80%;
```

For full-screen sections:

```css id="49x4m4"
height: 100vh;
```

For Grid:

```css id="w35lvi"
1fr 1fr 1fr
```

Avoid:

```css id="2n0vpu"
font-size: 10px;
```

Use:

```css id="f3gw6u"
font-size: 1rem;
```

---

# Summary

| Unit | Relative To           |
| ---- | --------------------- |
| px   | Fixed pixels          |
| %    | Parent element        |
| em   | Parent font size      |
| rem  | Root font size        |
| vw   | Viewport width        |
| vh   | Viewport height       |
| vmin | Smaller viewport side |
| vmax | Larger viewport side  |
| fr   | Grid fraction         |

---

# Recommended Usage

✅ rem → Text sizes

✅ % → Widths

✅ vh → Full screen sections

✅ vw → Responsive sizing

✅ fr → CSS Grid layouts

✅ px → Borders, shadows, small fixed values

Master these units and you'll understand sizing in modern CSS.
