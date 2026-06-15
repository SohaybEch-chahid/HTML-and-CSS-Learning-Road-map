# CSS Colors

Colors are used to style text, backgrounds, borders, shadows, and many other elements on a webpage.

---

# Why Colors Matter

Colors help:

* Improve user experience
* Create visual hierarchy
* Strengthen branding
* Increase readability

Example:

```css
h1 {
    color: blue;
}
```

---

# 1. Color Names

CSS supports many predefined color names.

```css
p {
    color: red;
}
```

Examples:

```css
color: blue;
color: green;
color: black;
color: white;
color: gray;
color: orange;
color: purple;
```

Advantages:

✅ Easy to read

Disadvantages:

❌ Limited precision

---

# 2. HEX Colors

HEX (Hexadecimal) is the most common way to define colors.

Syntax:

```css
color: #RRGGBB;
```

Example:

```css
h1 {
    color: #ff0000;
}
```

Examples:

| Color | HEX     |
| ----- | ------- |
| Red   | #ff0000 |
| Green | #00ff00 |
| Blue  | #0000ff |
| Black | #000000 |
| White | #ffffff |

---

# Short HEX

Some HEX values can be shortened.

```css
color: #ffffff;
```

becomes:

```css
color: #fff;
```

Example:

```css
color: #000;
```

for black.

---

# 3. RGB Colors

RGB stands for:

```text
Red Green Blue
```

Syntax:

```css
rgb(red, green, blue)
```

Example:

```css
color: rgb(255, 0, 0);
```

Values range from:

```text
0 → 255
```

Examples:

```css
color: rgb(0, 255, 0);
color: rgb(0, 0, 255);
color: rgb(255, 255, 255);
```

---

# 4. RGBA Colors

RGBA adds transparency.

Syntax:

```css
rgba(red, green, blue, alpha)
```

Example:

```css
background-color: rgba(0, 0, 255, 0.5);
```

Alpha values:

| Value | Meaning           |
| ----- | ----------------- |
| 0     | Fully transparent |
| 0.5   | 50% visible       |
| 1     | Fully visible     |

---

# 5. HSL Colors

HSL stands for:

```text
Hue
Saturation
Lightness
```

Syntax:

```css
hsl(hue, saturation, lightness)
```

Example:

```css
color: hsl(0, 100%, 50%);
```

Red:

```css
color: hsl(0, 100%, 50%);
```

Green:

```css
color: hsl(120, 100%, 50%);
```

Blue:

```css
color: hsl(240, 100%, 50%);
```

---

# 6. HSLA Colors

HSL with transparency.

```css
background-color: hsla(240, 100%, 50%, 0.5);
```

---

# Text Color

```css
p {
    color: navy;
}
```

Example:

```css
body {
    color: #333;
}
```

---

# Background Color

```css
body {
    background-color: #f4f4f4;
}
```

Example:

```css
.card {
    background-color: white;
}
```

---

# Border Color

```css
div {
    border: 2px solid red;
}
```

Example:

```css
button {
    border: 1px solid #333;
}
```

---

# Opacity

Controls transparency of the entire element.

```css
opacity: 0.5;
```

Values:

```text
0   = invisible
1   = fully visible
```

Example:

```css
img {
    opacity: 0.8;
}
```

---

# Linear Gradient

Creates smooth color transitions.

```css
background: linear-gradient(red, blue);
```

Example:

```css
background: linear-gradient(to right, #4facfe, #00f2fe);
```

Directions:

```css
to right
to left
to top
to bottom
```

---

# Radial Gradient

Starts from the center.

```css
background: radial-gradient(red, yellow);
```

Example:

```css
background: radial-gradient(circle, white, blue);
```

---

# Color Picker Tools

Popular tools:

* CSS Color Picker
* Coolors
* Color Hunt
* Adobe Color

These help create professional color palettes.

---

# Common Website Colors

Primary Blue:

```css
#2563eb
```

Success Green:

```css
#22c55e
```

Warning Yellow:

```css
#eab308
```

Danger Red:

```css
#ef4444
```

Dark Gray:

```css
#333333
```

Light Gray:

```css
#f5f5f5
```

---

# Best Practices

✅ Use HEX for most projects

✅ Use RGBA or HSLA for transparency

✅ Maintain good contrast

✅ Limit your color palette

✅ Use consistent branding colors

---

# Example

```css
body {
    background-color: #f4f4f4;
    color: #333;
}

button {
    background-color: #2563eb;
    color: white;
    border: none;
}
```

---

# Summary

Common color formats:

* Color Names
* HEX
* RGB
* RGBA
* HSL
* HSLA

Most used in modern web development:

1. HEX
2. RGB/RGBA
3. HSL/HSLA

Mastering colors will help you create beautiful and professional websites.

