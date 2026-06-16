# CSS Float

## What is Float?

`float` is a CSS property used to position elements to the left or right of their container, allowing other content (such as text) to wrap around them.

Originally, `float` was designed for wrapping text around images, similar to how images appear in newspapers.

---

## Basic Syntax

```css
float: left;
```

or

```css
float: right;
```

---

## Example: Floating an Image

### HTML

```html
<img src="cat.jpg" alt="Cat" class="cat" />

<p>This text will wrap around the image.</p>
```

### CSS

```css
.cat {
  float: left;
  margin-right: 10px;
}
```

### Result

```text
[IMAGE] This text wraps around
        the image.
        More text...
```

---

# Float Values

## 1. float: left

Moves an element to the left side of its container.

```css
img {
  float: left;
}
```

Result:

```text
[IMAGE] Text here...
```

---

## 2. float: right

Moves an element to the right side of its container.

```css
img {
  float: right;
}
```

Result:

```text
Text here... [IMAGE]
```

---

## 3. float: none

This is the default value.

```css
img {
  float: none;
}
```

The element remains in its normal position.

---

# Example with Div Elements

### HTML

```html
<div class="box1">Box 1</div>
<div class="box2">Box 2</div>
```

### CSS

```css
.box1 {
  width: 100px;
  height: 100px;
  background: red;
  float: left;
}

.box2 {
  width: 100px;
  height: 100px;
  background: blue;
  float: left;
}
```

### Result

```text
[Box1][Box2]
```

Without float:

```text
[Box1]
[Box2]
```

---

# The Float Problem

When all child elements are floated, the parent container may collapse because floated elements are removed from the normal document flow.

### Example

```html
<div class="container">
  <div class="box"></div>
</div>
```

```css
.box {
  float: left;
}
```

The container may appear to have a height of zero.

---

# The Clear Property

The `clear` property is used to prevent elements from wrapping around floated elements.

### HTML

```html
<div class="left-box"></div>

<p class="clear-text">New line starts here.</p>
```

### CSS

```css
.left-box {
  float: left;
}

.clear-text {
  clear: left;
}
```

---

## Clear Values

```css
clear: left;
clear: right;
clear: both;
```

### Explanation

| Value | Description                       |
| ----- | --------------------------------- |
| left  | Clears left floats                |
| right | Clears right floats               |
| both  | Clears both left and right floats |

`clear: both;` is the most commonly used value.

---

# Modern CSS Alternatives

Today, developers rarely use `float` for creating page layouts.

Instead, use:

- Flexbox ✅
- CSS Grid ✅

Example:

```css
.container {
  display: flex;
}
```

These modern layout systems are easier to use and more powerful than float-based layouts.

---

# When Should You Use Float?

### Good Use Cases

- Wrapping text around images
- Magazine-style content layouts
- Simple content positioning

Example:

```css
img {
  float: left;
}
```

### Not Recommended

- Entire website layouts
- Navigation bars
- Complex page structures

Use Flexbox or Grid instead.

---

# Quick Summary

| Property     | Description                      |
| ------------ | -------------------------------- |
| float: left  | Moves an element to the left     |
| float: right | Moves an element to the right    |
| float: none  | Default positioning              |
| clear: left  | Stops floating on the left side  |
| clear: right | Stops floating on the right side |
| clear: both  | Stops all floating               |

---

# Complete Example

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      img {
        float: left;
        margin-right: 15px;
      }
    </style>
  </head>
  <body>
    <img src="image.jpg" width="150" alt="Image" />

    <p>
      This text wraps around the image because the image is floated to the left.
    </p>
  </body>
</html>
```

---

# Key Takeaway

Think of `float` like placing a picture inside a newspaper article. The image sticks to one side of the page, and the text flows around it.

Today, `float` is mainly used for text wrapping, while Flexbox and Grid are preferred for building modern web layouts.
