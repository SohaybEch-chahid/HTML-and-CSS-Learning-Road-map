# CSS Pseudo-Classes

Pseudo-classes define a **special state** of an element.

They allow you to style elements when something happens, like:

- Hovering 🖱️
- Clicking 👆
- Focusing ⌨️
- Visiting links 🔗

---

# Why Pseudo-Classes?

Without pseudo-classes:

❌ Static UI
❌ No interaction feedback

With pseudo-classes:

✅ Interactive UI
✅ Better UX
✅ Modern behavior

---

# Syntax

```css id="a8k2qp"
selector:pseudo-class {
  property: value;
}
```

---

# 1. :hover

Triggered when mouse is over element.

```css id="m4x9wv"
button:hover {
  background: red;
}
```

---

# Example

```css id="k7m2qp"
.box {
  width: 100px;
  height: 100px;
  background: blue;
}

.box:hover {
  background: green;
}
```

---

# 2. :active

Triggered when element is being clicked.

```css id="t9x3wv"
button:active {
  transform: scale(0.95);
}
```

---

# 3. :focus

Used for input fields when selected.

```css id="q2k8qp"
input:focus {
  border: 2px solid blue;
  outline: none;
}
```

---

# Example

```html id="v8m2qp"
<input type="text" placeholder="Enter name" />
```

```css id="x3k9wv"
input:focus {
  background: lightyellow;
}
```

---

# 4. :visited

Styles visited links.

```css id="b7m2qp"
a:visited {
  color: purple;
}
```

---

# 5. :link

Styles unvisited links.

```css id="z5x8wv"
a:link {
  color: blue;
}
```

---

# 6. :first-child

Selects first element inside a parent.

```css id="p2k8qp"
p:first-child {
  color: red;
}
```

---

# 7. :last-child

Selects last child.

```css id="m8x3wv"
p:last-child {
  color: green;
}
```

---

# 8. :nth-child()

Selects specific child.

```css id="k9m2qp"
li:nth-child(2) {
  color: blue;
}
```

---

# Example

```html id="v4x8wv"
<ul>
  <li>One</li>
  <li>Two</li>
  <li>Three</li>
</ul>
```

Result:

👉 Only "Two" is blue

---

# 9. :not()

Excludes elements.

```css id="t2k8qp"
p:not(.special) {
  color: gray;
}
```

---

# 10. :checked

Used for checkboxes and radio buttons.

```css id="x7m3wv"
input:checked {
  outline: 2px solid green;
}
```

---

# Checkbox Example

```html id="k3x9qp"
<input type="checkbox" />
```

---

# 11. :disabled

For disabled inputs.

```css id="m2x8wv"
input:disabled {
  background: #ccc;
}
```

---

# 12. :enabled

Opposite of disabled.

```css id="t8k3qp"
input:enabled {
  background: white;
}
```

---

# 13. :first-of-type

First element of its type.

```css id="q7m9wv"
p:first-of-type {
  font-weight: bold;
}
```

---

# 14. :last-of-type

Last element of its type.

```css id="v9x2wv"
p:last-of-type {
  color: red;
}
```

---

# Real UI Example (Buttons)

```css id="k4x8qp"
button {
  background: blue;
  color: white;
  padding: 10px 20px;
  transition: 0.3s;
}

button:hover {
  background: darkblue;
}

button:active {
  transform: scale(0.95);
}
```

---

# Input UI Example

```css id="m7x2wv"
input {
  border: 1px solid #ccc;
  padding: 10px;
}

input:focus {
  border-color: blue;
  outline: none;
}
```

---

# Navigation Example

```css id="c9k3qp"
a {
  color: black;
  text-decoration: none;
}

a:hover {
  color: blue;
}
```

---

# Common Mistakes

❌ Using hover on mobile only thinking it works same

❌ Overusing nth-child without structure

❌ Forgetting focus styles (bad accessibility)

---

# Best Practices

✔ Always style :focus for accessibility
✔ Use hover for desktop interaction
✔ Use active for click feedback
✔ Keep selectors simple

---

# Summary

Pseudo-classes make CSS interactive:

```css id="v1h0fu"
:hover
:active
:focus
:nth-child()
:not()
:checked
```

---

# Final Idea

Think of pseudo-classes like **UI states**:

```text id="k9m3qp"
Idle → Hover → Click → Focus → Active
```

They bring life and interaction to your website 🚀
