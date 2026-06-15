# CSS Flexbox

Flexbox (Flexible Box Layout) is a one-dimensional layout system used to arrange items in rows or columns.

It is one of the most important CSS technologies and is used in almost every modern website.

Flexbox helps with:

- Alignment
- Centering
- Spacing
- Responsive layouts
- Navigation bars
- Cards
- Dashboards

---

# Why Flexbox?

Before Flexbox, layouts were difficult.

Developers used:

- Floats
- Tables
- Complex positioning

Flexbox makes layouts much easier.

---

# Flex Container

To start using Flexbox:

```css
.container {
  display: flex;
}
```

This creates a flex container.

All direct children become flex items.

HTML:

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

Items are placed in a row by default.

---

# Main Axis and Cross Axis

Flexbox works on two axes.

```text
Main Axis  →
Cross Axis ↓
```

By default:

```css
flex-direction: row;
```

Main axis:

```text
Left → Right
```

Cross axis:

```text
Top → Bottom
```

---

# flex-direction

Controls the direction of flex items.

---

## Row (Default)

```css
flex-direction: row;
```

Result:

```text
1 2 3
```

---

## Row Reverse

```css
flex-direction: row-reverse;
```

Result:

```text
3 2 1
```

---

## Column

```css
flex-direction: column;
```

Result:

```text
1
2
3
```

---

## Column Reverse

```css
flex-direction: column-reverse;
```

Result:

```text
3
2
1
```

---

# justify-content

Controls alignment on the main axis.

---

## Center

```css
justify-content: center;
```

```text
    1 2 3
```

---

## Start

```css
justify-content: flex-start;
```

```text
1 2 3
```

---

## End

```css
justify-content: flex-end;
```

```text
            1 2 3
```

---

## Space Between

```css
justify-content: space-between;
```

```text
1      2      3
```

---

## Space Around

```css
justify-content: space-around;
```

```text
 1    2    3
```

---

## Space Evenly

```css
justify-content: space-evenly;
```

```text
   1   2   3
```

---

# align-items

Controls alignment on the cross axis.

---

## Center

```css
align-items: center;
```

---

## Start

```css
align-items: flex-start;
```

---

## End

```css
align-items: flex-end;
```

---

## Stretch

```css
align-items: stretch;
```

Default value.

---

# Perfect Centering

One of the most famous Flexbox patterns:

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

Result:

```text
Perfect horizontal and vertical centering
```

---

# gap

Creates spacing between items.

```css
.container {
  display: flex;
  gap: 20px;
}
```

Result:

```text
1    2    3
```

Modern alternative to margins.

---

# flex-wrap

Controls whether items wrap.

---

## No Wrap

```css
flex-wrap: nowrap;
```

Default.

---

## Wrap

```css
flex-wrap: wrap;
```

Items move to the next line when needed.

Example:

```text
1 2 3 4
5 6 7 8
```

---

# flex-flow

Shorthand for:

```css
flex-direction
flex-wrap
```

Example:

```css
flex-flow: row wrap;
```

---

# align-content

Used when multiple rows exist.

```css
align-content: center;
```

Works only with wrapping.

---

# flex-grow

Allows items to grow.

HTML:

```html
<div class="container">
  <div class="box one">1</div>
  <div class="box two">2</div>
</div>
```

CSS:

```css
.one {
  flex-grow: 1;
}

.two {
  flex-grow: 2;
}
```

Result:

```text
Item 2 becomes twice as large
```

---

# flex-shrink

Controls shrinking.

```css
flex-shrink: 0;
```

Prevents shrinking.

---

# flex-basis

Sets the initial size.

```css
flex-basis: 200px;
```

---

# flex Shorthand

Instead of:

```css
flex-grow: 1;
flex-shrink: 1;
flex-basis: 200px;
```

Use:

```css
flex: 1 1 200px;
```

---

# order

Changes visual order.

```css
.item {
  order: 2;
}
```

Lower values appear first.

---

# align-self

Overrides align-items for one item.

```css
.item {
  align-self: center;
}
```

---

# Navigation Bar Example

HTML:

```html
<nav class="navbar">
  <div>Logo</div>
  <div>Menu</div>
</nav>
```

CSS:

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

Result:

```text
Logo                    Menu
```

---

# Card Layout Example

CSS:

```css
.cards {
  display: flex;
  gap: 20px;
}
```

Result:

```text
Card 1   Card 2   Card 3
```

---

# Centering Example

CSS:

```css
.hero {
  height: 100vh;

  display: flex;
  justify-content: center;
  align-items: center;
}
```

Perfect hero section.

---

# Common Mistakes

❌ Forgetting display:flex

```css
justify-content: center;
```

Will not work alone.

---

✅ Correct:

```css
display: flex;
justify-content: center;
```

---

❌ Using margins instead of gap

Old approach:

```css
margin-right: 20px;
```

Modern approach:

```css
gap: 20px;
```

---

# Best Practices

✅ Use Flexbox for navigation bars

✅ Use Flexbox for card layouts

✅ Use gap instead of margins

✅ Use justify-content and align-items together

✅ Learn centering patterns

---

# Summary

Most important properties:

```css
display: flex;
flex-direction;
justify-content;
align-items;
gap;
flex-wrap;
flex-grow;
flex-shrink;
flex-basis;
order;
align-self;
```

Most common setup:

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

Remember:

```text
justify-content → Main Axis
align-items     → Cross Axis
```

Master Flexbox and you can build most website layouts without difficulty.
