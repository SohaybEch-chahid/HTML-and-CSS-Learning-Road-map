# CSS Overflow Property

## What is Overflow?

The `overflow` property controls what happens when content is too large to fit inside its container.

For example, if a box has a fixed width and height but contains more content than it can display, the `overflow` property determines whether the extra content is hidden, scrollable, or visible.

---

# Basic Syntax

```css
overflow: value;
```

Example:

```css
.box {
  width: 300px;
  height: 100px;
  overflow: hidden;
}
```

---

# Why Do We Need Overflow?

Consider the following box:

```css
.box {
  width: 300px;
  height: 100px;
  border: 2px solid black;
}
```

If the content inside the box becomes larger than 100px in height, it will overflow outside the container.

The `overflow` property helps control this behavior.

---

# Overflow Values

## 1. overflow: visible

This is the default value.

The content is allowed to overflow outside the element.

### CSS

```css
.box {
  overflow: visible;
}
```

### Result

```text
+----------+
| Content  |
+----------+
   More content outside the box
```

---

## 2. overflow: hidden

Extra content is hidden and cannot be seen.

### CSS

```css
.box {
  overflow: hidden;
}
```

### Result

```text
+----------+
| Content  |
| Content  |
+----------+

(The rest is hidden)
```

---

## 3. overflow: scroll

Adds horizontal and vertical scrollbars, even if they are not needed.

### CSS

```css
.box {
  overflow: scroll;
}
```

### Result

```text
+----------+
| Content  |
| Content  |
+----------+
  ↑ Scrollbars always appear
```

---

## 4. overflow: auto

Adds scrollbars only when necessary.

### CSS

```css
.box {
  overflow: auto;
}
```

### Result

```text
+----------+
| Content  |
| Content  |
+----------+

Scrollbars appear only if content overflows.
```

This is the most commonly used value.

---

# Overflow-X and Overflow-Y

You can control horizontal and vertical overflow separately.

---

## overflow-x

Controls horizontal overflow.

```css
.box {
  overflow-x: scroll;
}
```

---

## overflow-y

Controls vertical overflow.

```css
.box {
  overflow-y: scroll;
}
```

---

## Example

```css
.box {
  width: 300px;
  height: 100px;

  overflow-x: hidden;
  overflow-y: scroll;
}
```

Result:

- Horizontal overflow is hidden.
- Vertical overflow can be scrolled.

---

# Practical Example

## HTML

```html
<div class="box">
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Lorem ipsum dolor
  sit amet, consectetur adipisicing elit. Lorem ipsum dolor sit amet,
  consectetur adipisicing elit.
</div>
```

## CSS

```css
.box {
  width: 250px;
  height: 100px;
  border: 2px solid black;

  overflow: auto;
}
```

If the text becomes larger than the box, a scrollbar appears automatically.

---

# Common Use Cases

## Scrollable Chat Window

```css
.chat {
  height: 300px;
  overflow-y: auto;
}
```

---

## Hidden Content

```css
.card {
  overflow: hidden;
}
```

Useful for cards, images, and rounded corners.

---

## Scrollable Code Block

```css
pre {
  overflow-x: auto;
}
```

Long code lines can be scrolled horizontally.

---

# Quick Summary

| Value   | Description                           |
| ------- | ------------------------------------- |
| visible | Content overflows outside the element |
| hidden  | Extra content is hidden               |
| scroll  | Always shows scrollbars               |
| auto    | Shows scrollbars only when needed     |

---

# Complete Example

## HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Overflow Example</title>
    <style>
      .box {
        width: 300px;
        height: 120px;
        border: 2px solid black;
        overflow: auto;
      }
    </style>
  </head>
  <body>
    <div class="box">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Lorem ipsum
      dolor sit amet, consectetur adipisicing elit. Lorem ipsum dolor sit amet,
      consectetur adipisicing elit. Lorem ipsum dolor sit amet, consectetur
      adipisicing elit.
    </div>
  </body>
</html>
```

---

# Key Takeaway

The `overflow` property controls what happens when content is larger than its container.

- Use `visible` to let content escape.
- Use `hidden` to cut off extra content.
- Use `scroll` to always show scrollbars.
- Use `auto` to show scrollbars only when necessary.

In modern web development, `overflow: auto` is the most commonly used option.
