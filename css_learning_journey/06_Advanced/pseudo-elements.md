# CSS Pseudo-Elements

Pseudo-elements let you style **specific parts of an element** or **add extra content** without changing HTML.

They are very powerful for:

- Decorations 🎨
- UI effects ✨
- Custom designs 🧩
- Text styling 📝

---

# Syntax

```css id="a8k2qp"
selector::pseudo-element {
  property: value;
}
```

👉 Notice: double `::`

---

# 1. ::before

Adds content before an element.

```css id="m4x9wv"
h1::before {
  content: "🔥 ";
}
```

---

# Example

```html id="k7m2qp"
<h1>Welcome</h1>
```

Result:

```text id="t9x3wv"
🔥 Welcome
```

---

# 2. ::after

Adds content after an element.

```css id="q2k8qp"
h1::after {
  content: " 🚀";
}
```

---

# Example Result

```text id="v8m2qp"
Welcome 🚀
```

---

# before + after together

```css id="x3k9wv"
h1::before {
  content: "✨ ";
}

h1::after {
  content: " ✨";
}
```

---

# 3. ::first-letter

Styles the first letter.

```css id="b7m2qp"
p::first-letter {
  font-size: 2rem;
  color: red;
}
```

---

# 4. ::first-line

Styles first line only.

```css id="z5x8wv"
p::first-line {
  font-weight: bold;
}
```

---

# 5. ::selection

Styles selected text.

```css id="p2k8qp"
::selection {
  background: yellow;
  color: black;
}
```

---

# Example

When user highlights text:

👉 Background becomes yellow
👉 Text becomes black

---

# Practical Button Decoration

```css id="m8x3wv"
button::before {
  content: "👉 ";
}

button::after {
  content: " ← Click me";
}
```

---

# Decorative Card Example

```css id="k9m2qp"
.card::before {
  content: "";
  display: block;
  width: 5px;
  height: 100%;
  background: blue;
  position: absolute;
  left: 0;
  top: 0;
}
```

---

# Tooltip Example

```css id="v4x8wv"
.tooltip::after {
  content: "Hover for info";
  position: absolute;
  background: black;
  color: white;
  padding: 5px;
  font-size: 12px;
}
```

---

# Important Rule: content property

Without `content`, pseudo-elements don’t show:

```css id="t2k8qp"
::before {
  content: "";
}
```

---

# Difference: Element vs Pseudo-element

| Element        | Pseudo-element  |
| -------------- | --------------- |
| Exists in HTML | Created by CSS  |
| Real DOM       | Virtual element |

---

# Styling Form Inputs Example

```css id="x7m3wv"
input::placeholder {
  color: gray;
}
```

---

# Advanced Example: Badge

```css id="k3x9qp"
.notification::after {
  content: "3";
  background: red;
  color: white;
  border-radius: 50%;
  padding: 5px;
  font-size: 12px;
  position: absolute;
}
```

---

# Common Mistakes

❌ Forgetting content:

```css id="m2x8wv"
::before {
  background: red;
}
```

❌ Using single colon:

```css id="t8k3qp"
:before❌;
```

---

# Best Practices

✔ Use pseudo-elements for decoration only
✔ Keep HTML clean
✔ Use for icons, badges, highlights
✔ Don’t overuse for important content

---

# Summary

Main pseudo-elements:

```css id="q7m9wv"
::before
::after
::first-letter
::first-line
::selection
```

---

# Final Idea

Think of pseudo-elements like:

```text id="v9x2wv"
CSS-generated decorations 🎨
```

They let you enhance UI without touching HTML 🚀
