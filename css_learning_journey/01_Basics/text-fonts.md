i# CSS Text and Fonts

Typography is one of the most important parts of web design. Good typography improves readability and user experience.

---

# What is Typography?

Typography is the art of styling text.

With CSS, you can control:

- Font family
- Font size
- Font weight
- Font style
- Text alignment
- Line height
- Letter spacing
- Text decoration

---

# 1. Font Family

Defines the typeface used by text.

```css
body {
  font-family: Arial, sans-serif;
}
```

Examples:

```css
font-family: Arial, sans-serif;
font-family: Verdana, sans-serif;
font-family: "Times New Roman", serif;
font-family: Courier, monospace;
```

Generic font families:

| Family     | Description             |
| ---------- | ----------------------- |
| serif      | Decorative endings      |
| sans-serif | Clean modern fonts      |
| monospace  | Every letter same width |
| cursive    | Handwriting style       |
| fantasy    | Decorative fonts        |

---

# 2. Font Size

Controls text size.

```css
p {
  font-size: 16px;
}
```

Examples:

```css
font-size: 12px;
font-size: 18px;
font-size: 24px;
font-size: 2rem;
```

---

# 3. Font Weight

Controls thickness.

```css
p {
  font-weight: bold;
}
```

Values:

```css
font-weight: 100;
font-weight: 300;
font-weight: 400;
font-weight: 700;
font-weight: 900;
```

Common values:

```css
font-weight: normal;
font-weight: bold;
```

---

# 4. Font Style

Makes text italic.

```css
p {
  font-style: italic;
}
```

Values:

```css
font-style: normal;
font-style: italic;
font-style: oblique;
```

---

# 5. Text Color

Changes text color.

```css
p {
  color: blue;
}
```

Examples:

```css
color: red;
color: #ff0000;
color: rgb(255, 0, 0);
```

---

# 6. Text Alignment

Controls horizontal alignment.

```css
text-align: left;
text-align: center;
text-align: right;
text-align: justify;
```

Example:

```css
h1 {
  text-align: center;
}
```

---

# 7. Text Decoration

Adds or removes decorations.

```css
text-decoration: underline;
```

Values:

```css
text-decoration: none;
text-decoration: underline;
text-decoration: overline;
text-decoration: line-through;
```

Remove link underline:

```css
a {
  text-decoration: none;
}
```

---

# 8. Text Transform

Changes letter casing.

```css
text-transform: uppercase;
```

Values:

```css
text-transform: uppercase;
text-transform: lowercase;
text-transform: capitalize;
```

Examples:

```text
hello world
```

Uppercase:

```text
HELLO WORLD
```

Capitalize:

```text
Hello World
```

---

# 9. Letter Spacing

Controls space between letters.

```css
letter-spacing: 2px;
```

Example:

```css
h1 {
  letter-spacing: 5px;
}
```

---

# 10. Word Spacing

Controls space between words.

```css
word-spacing: 10px;
```

---

# 11. Line Height

Controls space between lines.

```css
line-height: 1.5;
```

Example:

```css
p {
  line-height: 2;
}
```

Useful for readability.

---

# 12. Text Shadow

Adds a shadow behind text.

```css
text-shadow: 2px 2px 5px gray;
```

Syntax:

```css
text-shadow: horizontal vertical blur color;
```

Example:

```css
h1 {
  text-shadow: 1px 1px 3px black;
}
```

---

# 13. Google Fonts

Google Fonts provides free fonts.

HTML:

```html
<link
  href="https://fonts.googleapis.com/css2?family=Poppins&display=swap"
  rel="stylesheet"
/>
```

CSS:

```css
body {
  font-family: "Poppins", sans-serif;
}
```

Popular fonts:

- Poppins
- Roboto
- Inter
- Open Sans
- Montserrat

---

# Example

HTML:

```html
<h1>Welcome</h1>
<p>This is a paragraph.</p>
```

CSS:

```css
body {
  font-family: Arial, sans-serif;
}

h1 {
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 3px;
}

p {
  font-size: 18px;
  line-height: 1.6;
}
```

---

# Best Practices

✅ Use readable fonts

✅ Keep body text around 16px

✅ Use line-height between 1.4 and 1.8

✅ Avoid too many font families

✅ Use Google Fonts carefully

---

# Summary

Important properties:

- font-family
- font-size
- font-weight
- font-style
- color
- text-align
- text-decoration
- text-transform
- letter-spacing
- word-spacing
- line-height
- text-shadow

These properties are used in almost every website.
