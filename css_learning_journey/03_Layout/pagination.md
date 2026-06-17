# CSS Pagination

## What is Pagination?

Pagination is a navigation technique used to divide content into multiple pages. It allows users to move between pages using numbered links such as:

```text
Previous 1 2 3 4 5 Next
```

Pagination is commonly used for:

- Search results
- Blog posts
- Product listings
- Tables with many records

---

# Basic HTML Structure

```html
<div class="pagination">
  <a href="#">&laquo;</a>
  <a href="#">1</a>
  <a href="#" class="active">2</a>
  <a href="#">3</a>
  <a href="#">4</a>
  <a href="#">&raquo;</a>
</div>
```

Output:

```text
« 1 2 3 4 »
```

---

# Basic CSS Styling

```css
.pagination a {
  text-decoration: none;
  color: black;
  padding: 8px 16px;
  border: 1px solid #ddd;
}
```

This creates clickable page links with spacing and borders.

---

# Active Page

Usually, the current page is highlighted.

### HTML

```html
<a href="#" class="active">2</a>
```

### CSS

```css
.pagination a.active {
  background-color: #4caf50;
  color: white;
}
```

Output:

```text
1 [2] 3 4
```

---

# Hover Effect

Improve user experience by changing the appearance when the mouse hovers over a page link.

```css
.pagination a:hover:not(.active) {
  background-color: #ddd;
}
```

---

# Rounded Pagination

Add rounded corners:

```css
.pagination a {
  border-radius: 5px;
}
```

Example:

```text
(1) (2) (3) (4)
```

---

# Space Between Links

Use margins to separate page buttons.

```css
.pagination a {
  margin: 0 4px;
}
```

---

# Centered Pagination

Center the pagination on the page.

```css
.pagination {
  text-align: center;
}
```

---

# Complete Example

## HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Pagination Example</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h2>Pagination Example</h2>

    <div class="pagination">
      <a href="#">&laquo;</a>
      <a href="#">1</a>
      <a href="#" class="active">2</a>
      <a href="#">3</a>
      <a href="#">4</a>
      <a href="#">5</a>
      <a href="#">&raquo;</a>
    </div>
  </body>
</html>
```

---

## CSS

```css
.pagination {
  text-align: center;
}

.pagination a {
  color: black;
  text-decoration: none;
  padding: 8px 16px;
  border: 1px solid #ddd;
  margin: 0 4px;
}

.pagination a.active {
  background-color: #4caf50;
  color: white;
}

.pagination a:hover:not(.active) {
  background-color: #ddd;
}
```

---

# Using Flexbox for Pagination

Modern layouts often use Flexbox.

```css
.pagination {
  display: flex;
  justify-content: center;
  gap: 10px;
}
```

This creates evenly spaced pagination buttons.

---

# Common Use Cases

### Blog Posts

```text
← Previous 1 2 3 Next →
```

### E-Commerce Websites

```text
1 2 3 4 5 6 ...
```

### Search Results

```text
« Previous 1 2 3 4 Next »
```

---

# Quick Summary

| Property           | Purpose                     |
| ------------------ | --------------------------- |
| text-decoration    | Removes underline           |
| padding            | Adds spacing inside buttons |
| border             | Creates button borders      |
| margin             | Adds space between buttons  |
| background-color   | Highlights active page      |
| border-radius      | Creates rounded buttons     |
| text-align: center | Centers pagination          |
| display: flex      | Creates modern layouts      |

---

# Key Takeaway

Pagination helps users navigate through large amounts of content by splitting it into multiple pages.

To create attractive pagination:

- Use `<a>` elements for page links.
- Highlight the active page.
- Add hover effects.
- Center the links.
- Use Flexbox for modern layouts.

Pagination is commonly found in blogs, search engines, and e-commerce websites.
