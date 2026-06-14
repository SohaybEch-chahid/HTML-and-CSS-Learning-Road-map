# HTML File Structure

## Introduction

Every HTML page follows a basic structure. Understanding this structure is one of the most important skills when learning web development.

A typical HTML document looks like this:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Website</title>
  </head>

  <body>
    <h1>Hello World</h1>
    <p>My first web page.</p>
  </body>
</html>
```

---

# Understanding the Structure

```text
HTML Document
│
├── <!DOCTYPE html>
│
└── <html>
    │
    ├── <head>
    │   ├── meta
    │   ├── title
    │   ├── css
    │   └── scripts
    │
    └── <body>
        ├── headings
        ├── paragraphs
        ├── images
        ├── links
        ├── forms
        └── tables
```

---

# 1. DOCTYPE Declaration

```html
<!DOCTYPE html>
```

## Purpose

The DOCTYPE declaration tells the browser which version of HTML the page uses.

For modern websites, HTML5 is used.

```html
<!DOCTYPE html>
```

This line must always be the first line of the document.

---

# 2. The HTML Element

```html
<html lang="en"></html>
```

## Purpose

The `<html>` element is the root element of the entire webpage.

Everything inside the webpage must be placed between:

```html
<html></html>
```

---

## Language Attribute

```html
<html lang="en"></html>
```

The `lang` attribute specifies the language of the page.

Examples:

```html
<html lang="en"></html>
```

English

```html
<html lang="fr"></html>
```

French

```html
<html lang="es"></html>
```

Spanish

```html
<html lang="ar"></html>
```

Arabic

This helps:

- Search engines
- Browsers
- Screen readers

understand the language of the page.

---

# 3. The Head Section

```html
<head> </head>
```

## Purpose

The `<head>` contains information about the webpage.

Most content inside the head is not displayed directly on the page.

Common items inside the head include:

- Meta tags
- Title
- CSS files
- JavaScript files
- Favicon

---

# 4. Meta Tags

Meta tags provide information about the webpage.

---

## Character Encoding

```html
<meta charset="UTF-8" />
```

### Purpose

Allows the page to display:

- Special symbols
- Accented characters
- Multiple languages

Examples:

```text
é
ñ
ü
مرحبا
こんにちは
```

UTF-8 is the standard character encoding used today.

---

## Viewport Meta Tag

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

### Purpose

Makes the website responsive on:

- Phones
- Tablets
- Laptops
- Desktop computers

Without this tag, websites may appear incorrectly on mobile devices.

---

# 5. Title Element

```html
<title>My Website</title>
```

## Purpose

The title appears in:

- Browser tabs
- Bookmarks
- Search engine results

Example:

```text
My Website
```

A clear title improves SEO and user experience.

---

# 6. The Body Section

```html
<body></body>
```

## Purpose

The body contains everything visible on the webpage.

Examples:

- Headings
- Paragraphs
- Images
- Links
- Forms
- Tables
- Lists

---

## Example

```html
<body>
  <h1>Welcome</h1>

  <p>This is my first website.</p>

  <img src="image.jpg" alt="Example image" />
</body>
```

Everything inside the body is displayed to users.

---

# Complete Example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />

    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <title>My First Web Page</title>
  </head>

  <body>
    <h1>Welcome to My Website</h1>

    <p>This page demonstrates the basic structure of an HTML document.</p>
  </body>
</html>
```

---

# Professional Starter Template

This is the template most developers start with when creating a new HTML page.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />

    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <title>Page Title</title>
  </head>

  <body>
    <!-- Your content goes here -->
  </body>
</html>
```

---

# House Analogy

Think of an HTML document like a house.

```text
<!DOCTYPE html>
│
├── House blueprint type
│
<html>
│
├── Entire house
│
<head>
│
├── House information
│   ├── Address
│   ├── Owner information
│   └── Plans
│
<body>
│
├── Actual rooms and furniture
│   that visitors can see and use
```

The head contains information about the house.

The body contains everything visitors interact with.

---

# Summary

## Main Parts of an HTML Document

### DOCTYPE

```html
<!DOCTYPE html>
```

Tells the browser that the page uses HTML5.

---

### HTML

```html
<html lang="en"></html>
```

Root element of the page.

---

### Head

```html
<head> </head>
```

Contains metadata and page information.

---

### Meta Tags

```html
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

Provide browser and device information.

---

### Title

```html
<title>Page Title</title>
```

Displayed in browser tabs and search results.

---

### Body

```html
<body></body>
```

Contains all visible page content.

---

## Final Structure

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Page Title</title>
  </head>

  <body>
    <!-- Website Content -->
  </body>
</html>
```

Mastering this structure is the foundation of all web development. Every HTML page you create will follow this pattern.
