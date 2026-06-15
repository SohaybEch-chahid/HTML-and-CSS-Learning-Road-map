# CSS Grid

CSS Grid is a **two-dimensional layout system** used to create complex layouts easily.

It controls:

- Rows
- Columns
- Both at the same time

Grid is used for:

- Dashboards
- Website layouts
- Image galleries
- Complex UI systems

---

# Flexbox vs Grid

| Feature    | Flexbox            | Grid                |
| ---------- | ------------------ | ------------------- |
| Direction  | 1D (row OR column) | 2D (rows + columns) |
| Layout     | Small components   | Full pages          |
| Complexity | Simple             | Advanced            |

---

# Enable Grid

```css id="x7q8k2"
.container {
  display: grid;
}
```

---

# 1. grid-template-columns

Defines columns.

```css id="m2c9qv"
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```

Result:

```text id="v8p3lm"
| 1 | 2 | 3 |
```

Each column has equal space.

---

# 2. fr Unit

`fr` = fraction of available space.

Example:

```css id="t6w1kd"
grid-template-columns: 1fr 2fr;
```

Result:

```text id="3nqk8v"
| 1 part | 2 parts |
```

Second column is twice as big.

---

# 3. repeat()

Shortcut for repeating columns.

```css id="k9x2mp"
grid-template-columns: repeat(3, 1fr);
```

Same as:

```css id="a7b1zc"
1fr 1fr 1fr
```

---

# 4. grid-template-rows

Defines rows.

```css id="z3m8qp"
.container {
  grid-template-rows: 100px 200px;
}
```

---

# 5. gap

Spacing between items.

```css id="u8k5rd"
.container {
  display: grid;
  gap: 20px;
}
```

---

# Grid Example

HTML:

```html id="p1x7lm"
<div class="grid">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

CSS:

```css id="w4c9jn"
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
}
```

Result:

```text id="q8m2wv"
[1] [2] [3]
```

---

# 6. grid-column

Make an item span multiple columns.

```css id="n5x9qv"
.item {
  grid-column: 1 / 3;
}
```

Meaning:

- Start at column 1
- End at column 3

---

# Example Span

```html id="l7v2mc"
<div class="grid">
  <div class="box header">Header</div>
  <div class="box">1</div>
  <div class="box">2</div>
</div>
```

```css id="c9q1zp"
.header {
  grid-column: 1 / 3;
}
```

Result:

```text id="b8m4xk"
[   Header   ]
[ 1 ] [ 2 ]
```

---

# 7. grid-row

Spans rows.

```css id="h3k9wd"
.item {
  grid-row: 1 / 3;
}
```

---

# 8. grid-area

Shortcut for row + column positioning.

```css id="r6n2qp"
.item {
  grid-area: 1 / 1 / 3 / 3;
}
```

---

# 9. grid-template-areas

Very powerful for layout design.

HTML:

```html id="s9v3mc"
<div class="container">
  <header>Header</header>
  <nav>Nav</nav>
  <main>Main</main>
  <footer>Footer</footer>
</div>
```

CSS:

```css id="k2p7wx"
.container {
  display: grid;
  grid-template-areas:
    "header header"
    "nav main"
    "footer footer";
}
```

Assign areas:

```css id="x1q9vd"
header {
  grid-area: header;
}
nav {
  grid-area: nav;
}
main {
  grid-area: main;
}
footer {
  grid-area: footer;
}
```

---

# Result Layout

```text id="f4m8qp"
Header Header
Nav    Main
Footer Footer
```

---

# 10. justify-items

Aligns items horizontally inside grid cells.

```css id="u3k9qv"
justify-items: center;
```

Values:

- start
- center
- end
- stretch

---

# 11. align-items

Aligns items vertically.

```css id="j8v2md"
align-items: center;
```

---

# 12. place-items

Shortcut:

```css id="w6n9qp"
place-items: center;
```

---

# 13. justify-content

Controls whole grid horizontally.

```css id="k4x8mv"
justify-content: center;
```

---

# 14. align-content

Controls whole grid vertically.

```css id="v9m3qp"
align-content: center;
```

---

# Dashboard Example

```css id="r7n2kp"
.container {
  display: grid;
  grid-template-columns: 200px 1fr;
  grid-template-rows: 60px 1fr 60px;
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
  height: 100vh;
}
```

---

# Why Grid is Powerful

Grid allows you to:

- Build full website layouts
- Control both rows and columns
- Create responsive designs easily
- Replace complex CSS positioning hacks

---

# Common Mistakes

❌ Using Grid for small components

```css id="m2v8qp"
button {
  display: grid;
}
```

Not needed.

---

❌ Forgetting fr unit

```css id="x9k3wv"
grid-template-columns: 100px 100px 100px;
```

Not responsive.

---

# Best Practices

✅ Use Grid for page layouts

✅ Use Flexbox for small components

✅ Use fr instead of fixed px

✅ Use gap instead of margins

---

# Summary

Most important properties:

```css id="k8v2qp"
display: grid;
grid-template-columns;
grid-template-rows;
grid-template-areas;
gap;
fr;
grid-column;
grid-row;
place-items;
```

---

# Final Rule

```text id="m3q9wv"
Flexbox → 1D layout
Grid    → 2D layout
```

Master Grid and Flexbox and you can build any modern website layout.
