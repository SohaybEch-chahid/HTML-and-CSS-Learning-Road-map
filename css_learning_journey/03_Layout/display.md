# CSS Display

The `display` property controls how an element behaves on a webpage.

It determines:

- How elements are positioned
- Whether they start on a new line
- Whether width and height can be changed
- How layouts are created

The `display` property is one of the most important CSS properties.

---

# Default Display Types

Different HTML elements have different default display values.

Examples:

```html
<div></div>
<p></p>
<h1></h1>
```

Default:

```css
display: block;
```

Examples:

```html
<span></span>
<a></a>
<strong></strong>
```

Default:

```css
display: inline;
```

---

# 1. display: block

A block element:

✅ Starts on a new line

✅ Takes the full available width

✅ Accepts width and height

Example:

```html
<div>Box 1</div>
<div>Box 2</div>
```

Result:

```text
Box 1
Box 2
```

CSS:

```css
div {
  background: lightblue;
}
```

Common block elements:

```html
<div>
  <p></p>
  <h1>
    <h2>
      <section>
        <article>
          <header>
            <footer></footer>
          </header>
        </article>
      </section>
    </h2>
  </h1>
</div>
```

---

# Block Example

```css
.box {
  display: block;
  width: 200px;
  height: 100px;
}
```

The element occupies its own line.

---

# 2. display: inline

An inline element:

✅ Stays on the same line

❌ Width does not work

❌ Height does not work

Example:

```html
<span>Hello</span> <span>World</span>
```

Result:

```text
Hello World
```

---

# Inline Example

```css
span {
  display: inline;
}
```

Common inline elements:

```html
<span>
  <a>
    <strong>
      <em> <label></label></em></strong></a
></span>
```

---

# Width and Height Problem

```css
span {
  width: 200px;
  height: 100px;
}
```

Result:

```text
Ignored
```

Inline elements do not respect width and height.

---

# 3. display: inline-block

Combines the best of both worlds.

✅ Stays on the same line

✅ Accepts width

✅ Accepts height

Example:

```css
.box {
  display: inline-block;
  width: 200px;
  height: 100px;
}
```

HTML:

```html
<div class="box">Box 1</div>
<div class="box">Box 2</div>
```

Result:

```text
Box 1   Box 2
```

---

# Inline-Block Example

```css
button {
  display: inline-block;
}
```

Often used for:

- Buttons
- Navigation items
- Small cards

---

# 4. display: none

Completely removes an element from the page.

Example:

```css
.hidden {
  display: none;
}
```

HTML:

```html
<p class="hidden">Hidden Text</p>
```

Result:

```text
Element disappears
```

It takes up no space.

---

# Visibility vs Display

Hidden with display:

```css
display: none;
```

Result:

```text
Removed completely
```

---

Hidden with visibility:

```css
visibility: hidden;
```

Result:

```text
Invisible but still occupies space
```

---

# 5. display: flex

Creates a Flexbox container.

Example:

```css
.container {
  display: flex;
}
```

Result:

Children line up horizontally.

Example:

```html
<div class="container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

Result:

```text
1  2  3
```

Flexbox is covered in detail later.

---

# 6. display: grid

Creates a Grid container.

Example:

```css
.container {
  display: grid;
}
```

Grid is used for two-dimensional layouts.

Covered later.

---

# 7. display: contents

Makes the element disappear visually but keeps its children.

Example:

```css
.wrapper {
  display: contents;
}
```

Advanced usage.

---

# 8. display: list-item

Behaves like a list item.

Example:

```css
.item {
  display: list-item;
}
```

Result:

Shows bullet points.

---

# Practical Example

HTML:

```html
<nav>
  <a href="#">Home</a>
  <a href="#">About</a>
  <a href="#">Contact</a>
</nav>
```

CSS:

```css
a {
  display: inline-block;
  padding: 10px 15px;
}
```

Result:

Better spacing for navigation links.

---

# Common Mistakes

❌ Trying to set width on inline elements

```css
span {
  width: 300px;
}
```

Will not work.

---

✅ Use:

```css
span {
  display: inline-block;
  width: 300px;
}
```

---

❌ Using display:none when you only want invisibility

```css
display: none;
```

Removes the element completely.

---

# Best Practices

✅ Use block for sections

✅ Use inline for text

✅ Use inline-block for buttons and links

✅ Use flex for one-dimensional layouts

✅ Use grid for two-dimensional layouts

✅ Use display:none carefully

---

# Summary

Most important values:

```css
display: block;
display: inline;
display: inline-block;
display: none;
display: flex;
display: grid;
```

Remember:

```text
Block        → New line
Inline       → Same line
Inline-Block → Same line + width/height
None         → Hidden
Flex         → One-dimensional layout
Grid         → Two-dimensional layout
```

Understanding display is the foundation of modern CSS layouts.
