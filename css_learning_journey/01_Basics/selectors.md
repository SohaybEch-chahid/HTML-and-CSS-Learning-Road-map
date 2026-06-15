# CSS Selectors

Selectors are used to target HTML elements and apply styles to them.

---

# 1. Element Selector

Targets all elements of a specific type.

```css
p {
  color: red;
}
```

HTML:

```html
<p>Hello World</p>
<p>CSS is awesome</p>
```

---

# 2. Class Selector

Targets elements with a specific class.

HTML:

```html
<p class="text">Hello</p>
<h1 class="text">Welcome</h1>
```

CSS:

```css
.text {
  color: green;
}
```

Classes can be reused on multiple elements.

---

# 3. ID Selector

Targets one unique element.

HTML:

```html
<h1 id="title">Welcome</h1>
```

CSS:

```css
#title {
  color: blue;
}
```

IDs should be unique on a page.

---

# 4. Universal Selector

Targets every element.

```css
* {
  margin: 0;
  padding: 0;
}
```

Commonly used for CSS resets.

---

# 5. Group Selector

Apply the same styles to multiple elements.

```css
h1,
h2,
p {
  color: black;
}
```

---

# 6. Descendant Selector

Targets elements inside another element.

HTML:

```html
<div>
  <p>Hello</p>
</div>
```

CSS:

```css
div p {
  color: red;
}
```

Only paragraphs inside a div are affected.

---

# 7. Child Selector

Targets direct children only.

HTML:

```html
<div>
  <p>Direct Child</p>

  <section>
    <p>Not Direct Child</p>
  </section>
</div>
```

CSS:

```css
div > p {
  color: blue;
}
```

Only the first paragraph is selected.

---

# 8. Adjacent Sibling Selector

Targets the next sibling.

HTML:

```html
<h1>Title</h1>
<p>Paragraph</p>
```

CSS:

```css
h1 + p {
  color: green;
}
```

---

# 9. General Sibling Selector

Targets all following siblings.

HTML:

```html
<h1>Title</h1>
<p>Paragraph 1</p>
<p>Paragraph 2</p>
```

CSS:

```css
h1 ~ p {
  color: red;
}
```

---

# 10. Attribute Selector

Targets elements with specific attributes.

HTML:

```html
<input type="text" />
```

CSS:

```css
input[type="text"] {
  border: 2px solid blue;
}
```

---

# 11. Hover Selector

Applies styles when the mouse is over an element.

```css
button:hover {
  background-color: blue;
}
```

---

# 12. Focus Selector

Applies styles when an input is selected.

```css
input:focus {
  border: 2px solid green;
}
```

---

# 13. Active Selector

Applies styles while clicking.

```css
button:active {
  transform: scale(0.95);
}
```

---

# 14. First Child Selector

Targets the first child.

```css
li:first-child {
  color: red;
}
```

---

# 15. Last Child Selector

Targets the last child.

```css
li:last-child {
  color: blue;
}
```

---

# 16. Nth Child Selector

Targets specific children.

```css
li:nth-child(2) {
  color: green;
}
```

Even items:

```css
li:nth-child(even) {
  background: lightgray;
}
```

Odd items:

```css
li:nth-child(odd) {
  background: white;
}
```

---

# Selector Specificity

Priority order:

```text
Inline Style > ID > Class > Element
```

Example:

```css
#title {
  color: red;
}

.text {
  color: blue;
}

h1 {
  color: green;
}
```

Result: Red (ID wins).

---

# Summary

Common selectors used daily:

- Element Selector
- Class Selector
- ID Selector
- Descendant Selector
- Child Selector
- Attribute Selector
- :hover
- :focus
- :nth-child()

Master these and you'll use them in almost every CSS project.
