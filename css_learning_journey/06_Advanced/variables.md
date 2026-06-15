# CSS Variables (Custom Properties)

CSS Variables allow you to store values and reuse them across your styles.

They make CSS:

- Easier to maintain 🧠
- More scalable 📈
- Cleaner and reusable ♻️

---

# Why CSS Variables?

Without variables:

❌ Repeating colors everywhere
❌ Hard to update design

With variables:

✅ One change updates everything
✅ Consistent design system

---

# Basic Syntax

```css id="a8k2qp"
:root {
  --primary-color: blue;
  --text-color: #333;
}
```

Usage:

```css id="m4x9wv"
button {
  background-color: var(--primary-color);
  color: var(--text-color);
}
```

---

# What is :root?

`:root` represents the highest level of the document (like HTML).

It is the best place to define global variables.

---

# Example

```css id="k7m2qp"
:root {
  --main-bg: #f5f5f5;
}

body {
  background: var(--main-bg);
}
```

---

# Fallback Values

If variable is missing:

```css id="t9x3wv"
color: var(--primary-color, black);
```

👉 If variable doesn't exist → uses black

---

# Local Variables

Variables can also be defined inside a class:

```css id="q2k8qp"
.card {
  --card-color: white;
  background: var(--card-color);
}
```

---

# CSS Variables with Components

```css id="v8m2qp"
.button {
  --btn-color: blue;
  background: var(--btn-color);
}
```

---

# Theme Example

```css id="x3k9wv"
:root {
  --bg: white;
  --text: black;
}

body {
  background: var(--bg);
  color: var(--text);
}
```

---

# Dark Mode with Variables

```css id="b7m2qp"
.dark {
  --bg: black;
  --text: white;
}
```

Usage:

```css id="z5x8wv"
body {
  background: var(--bg);
  color: var(--text);
}
```

---

# Change Theme Easily

Just switch class:

```html id="p2k8qp"
<body class="dark"></body>
```

---

# Variables in Flex/Grid

```css id="m8x3wv"
:root {
  --gap: 20px;
}

.container {
  display: flex;
  gap: var(--gap);
}
```

---

# Variables for Spacing System

```css id="k9m2qp"
:root {
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 32px;
}
```

Usage:

```css id="v4x8wv"
.box {
  padding: var(--space-md);
}
```

---

# Variables for Colors System

```css id="t2k8qp"
:root {
  --primary: #2563eb;
  --secondary: #1e40af;
  --danger: #dc2626;
}
```

---

# Advantages

✔ Reusable values
✔ Easy theme switching
✔ Cleaner code
✔ Better scalability

---

# Common Mistakes

❌ Forgetting `--`

```css id="x7m3wv"
color: var(primary-color);
```

❌ Undefined variables

```css id="k3x9qp"
color: var(--not-defined);
```

---

# Best Practices

✔ Define variables in `:root`
✔ Use meaningful names
✔ Create design system (colors, spacing, fonts)
✔ Use fallback values when needed

---

# Summary

CSS Variables structure:

```css id="m2x8wv"
:root {
  --name: value;
}

selector {
  property: var(--name);
}
```

---

# Final Idea

Think of CSS variables like a **design brain** 🧠

```text id="t8k3qp"
One variable → Many places
```

They make your CSS professional and scalable 🚀
