# CSS Combinators

## What are CSS Combinators?

CSS combinators are special selectors used to define relationships between elements.

They allow you to select elements based on their position relative to other elements.

There are four main combinators:

1. Descendant Selector (space)
2. Child Selector (`>`)
3. Adjacent Sibling Selector (`+`)
4. General Sibling Selector (`~`)

---

# 1. Descendant Selector (space)

Selects all elements that are descendants of another element.

## Syntax

```css
selector1 selector2 {
    properties;
}
```

## Example

### HTML

```html
<div>
  <p>Paragraph 1</p>

  <section>
    <p>Paragraph 2</p>
  </section>
</div>
```

### CSS

```css
div p {
  color: blue;
}
```

### Result

Both paragraphs become blue because both are descendants of `<div>`.

---

# 2. Child Selector (>)

Selects only the direct children of an element.

## Syntax

```css
selector1 > selector2 {
    properties;
}
```

## Example

### HTML

```html
<div>
  <p>Paragraph 1</p>

  <section>
    <p>Paragraph 2</p>
  </section>
</div>
```

### CSS

```css
div > p {
  color: red;
}
```

### Result

- Paragraph 1 → Red ✅
- Paragraph 2 → Not affected ❌

Because Paragraph 2 is inside `<section>`, not directly inside `<div>`.

---

# 3. Adjacent Sibling Selector (+)

Selects the first sibling immediately after another element.

## Syntax

```css
selector1 + selector2 {
    properties;
}
```

## Example

### HTML

```html
<h1>Title</h1>

<p>Paragraph 1</p>

<p>Paragraph 2</p>
```

### CSS

```css
h1 + p {
  color: green;
}
```

### Result

- Paragraph 1 → Green ✅
- Paragraph 2 → Not affected ❌

Only the first `<p>` after `<h1>` is selected.

---

# 4. General Sibling Selector (~)

Selects all sibling elements that come after another element.

## Syntax

```css
selector1 ~ selector2 {
    properties;
}
```

## Example

### HTML

```html
<h1>Title</h1>

<p>Paragraph 1</p>

<p>Paragraph 2</p>

<p>Paragraph 3</p>
```

### CSS

```css
h1 ~ p {
  color: purple;
}
```

### Result

- Paragraph 1 → Purple ✅
- Paragraph 2 → Purple ✅
- Paragraph 3 → Purple ✅

All `<p>` elements after `<h1>` are selected.

---

# Visual Representation

## Descendant Selector

```text
div
├── p          ✅
└── section
    └── p      ✅
```

```css
div p
```

---

## Child Selector

```text
div
├── p          ✅
└── section
    └── p      ❌
```

```css
div > p
```

---

## Adjacent Sibling Selector

```text
h1
↓
p     ✅
p     ❌
p     ❌
```

```css
h1 + p
```

---

## General Sibling Selector

```text
h1
↓
p     ✅
p     ✅
p     ✅
```

```css
h1 ~ p
```

---

# Complete Example

## HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <title>CSS Combinators</title>
  </head>
  <body>
    <div>
      <p>Direct child paragraph</p>

      <section>
        <p>Nested paragraph</p>
      </section>
    </div>

    <h1>Heading</h1>

    <p>First paragraph</p>
    <p>Second paragraph</p>
    <p>Third paragraph</p>
  </body>
</html>
```

## CSS

```css
/* Descendants */
div p {
  color: blue;
}

/* Direct children */
div > p {
  background-color: yellow;
}

/* First sibling only */
h1 + p {
  font-weight: bold;
}

/* All following siblings */
h1 ~ p {
  border: 1px solid black;
}
```

---

# Quick Summary

| Combinator  | Name                      | Selects                |
| ----------- | ------------------------- | ---------------------- |
| ` ` (space) | Descendant Selector       | All descendants        |
| `>`         | Child Selector            | Direct children only   |
| `+`         | Adjacent Sibling Selector | First next sibling     |
| `~`         | General Sibling Selector  | All following siblings |

---

# Key Takeaway

CSS combinators allow you to target elements based on their relationship with other elements:

- **Space (` `)** → all descendants.
- **Greater-than (`>`)** → direct children only.
- **Plus (`+`)** → immediate next sibling.
- **Tilde (`~`)** → all following siblings.

Mastering combinators makes your CSS selectors more powerful and helps you write cleaner, more maintainable stylesheets.
