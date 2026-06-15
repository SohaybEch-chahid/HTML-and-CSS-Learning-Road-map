# CSS Media Queries

Media Queries are used to make websites **responsive**.

They allow your design to adapt to different screen sizes like:

- Phones 📱
- Tablets 📟
- Laptops 💻
- Large screens 🖥️

---

# Why Responsive Design?

Without responsive design:

❌ Website breaks on mobile
❌ Text becomes too small or too large
❌ Layout overflows screen

With responsive design:

✅ Works on all devices
✅ Better user experience
✅ Professional websites

---

# Basic Syntax

```css
@media (condition) {
  /* CSS rules */
}
```

---

# Example: Mobile Screens

```css id="m1k8qp"
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

Meaning:

👉 If screen width is **600px or less**, apply this style

---

# Common Breakpoints

| Device  | Width          |
| ------- | -------------- |
| Mobile  | 0 - 600px      |
| Tablet  | 600px - 900px  |
| Laptop  | 900px - 1200px |
| Desktop | 1200px+        |

---

# Mobile First Approach (Recommended)

Start designing for mobile first:

```css id="n2v9qp"
.container {
  font-size: 14px;
}
```

Then enhance for larger screens:

```css id="b7x3kp"
@media (min-width: 768px) {
  .container {
    font-size: 18px;
  }
}
```

---

# max-width vs min-width

## max-width (desktop → mobile)

```css id="k9m2qp"
@media (max-width: 768px) {
  body {
    background: black;
  }
}
```

---

## min-width (mobile → desktop)

```css id="x4p8wv"
@media (min-width: 768px) {
  body {
    background: white;
  }
}
```

👉 Modern developers prefer **min-width**

---

# Responsive Layout Example

```css id="c3v7qp"
.container {
  display: flex;
  gap: 20px;
}
```

Mobile fix:

```css id="r8m2wv"
@media (max-width: 600px) {
  .container {
    flex-direction: column;
  }
}
```

---

# Responsive Text

```css id="t5x9qp"
h1 {
  font-size: 24px;
}
```

Tablet:

```css id="v2k8wv"
@media (min-width: 768px) {
  h1 {
    font-size: 32px;
  }
}
```

Desktop:

```css id="z7m3qp"
@media (min-width: 1024px) {
  h1 {
    font-size: 48px;
  }
}
```

---

# Hide Elements on Mobile

```css id="p9k2wv"
@media (max-width: 600px) {
  .sidebar {
    display: none;
  }
}
```

---

# Show Only on Desktop

```css id="f4x8qp"
.desktop-only {
  display: none;
}

@media (min-width: 768px) {
  .desktop-only {
    display: block;
  }
}
```

---

# Responsive Grid Example

```css id="l6m2wv"
.grid {
  display: grid;
  grid-template-columns: 1fr;
}
```

Tablet:

```css id="q8x3qp"
@media (min-width: 768px) {
  .grid {
    grid-template-columns: 1fr 1fr;
  }
}
```

Desktop:

```css id="w2k9wv"
@media (min-width: 1024px) {
  .grid {
    grid-template-columns: 1fr 1fr 1fr;
  }
}
```

---

# Responsive Image

```css id="a7m3qp"
img {
  max-width: 100%;
  height: auto;
}
```

👉 Prevents images from overflowing

---

# Viewport Meta Tag (Important)

Add this in HTML:

```html id="u3k9wv"
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

Without this:

❌ Mobile layout breaks

---

# Orientation Media Query

```css id="d8x2qp"
@media (orientation: landscape) {
  body {
    background: lightgray;
  }
}
```

---

# Dark Mode Example

```css id="s5m9wv"
@media (prefers-color-scheme: dark) {
  body {
    background: black;
    color: white;
  }
}
```

---

# Print Media Query

For printing pages:

```css id="h2k8qp"
@media print {
  body {
    font-size: 12px;
  }
}
```

---

# Common Mistakes

❌ Only designing for desktop

❌ Forgetting viewport meta tag

❌ Using only px instead of responsive units

---

# Best Practices

✅ Use mobile-first design
✅ Prefer min-width media queries
✅ Use flexbox + grid for responsiveness
✅ Use relative units (%, rem, vw)
✅ Test on real devices

---

# Summary

Media queries allow you to adapt designs:

```css id="m7x2wv"
@media (min-width: 768px) {
}
@media (max-width: 600px) {
}
@media print {
}
@media (orientation: landscape) {
}
```

---

# Final Idea

Think of responsive design like this:

```text id="c9k3qp"
One website → Many screens
```

Master this and your websites will work everywhere 🌍
