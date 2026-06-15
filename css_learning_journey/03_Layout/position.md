# CSS Position

The `position` property controls how an element is placed on a webpage.

It works together with:

```css
top
right
bottom
left
z-index
```

Understanding positioning is essential for:

- Navigation bars
- Dropdown menus
- Modals
- Tooltips
- Sidebars
- Floating buttons

---

# Position Types

CSS provides five main positioning methods:

```css
static
relative
absolute
fixed
sticky
```

---

# 1. position: static

Default positioning.

```css
position: static;
```

Every HTML element is static by default.

Example:

```css
.box {
  position: static;
}
```

Characteristics:

✅ Normal document flow

❌ top does not work

❌ right does not work

❌ bottom does not work

❌ left does not work

---

# Static Example

HTML:

```html
<div>Box 1</div>
<div>Box 2</div>
```

Result:

```text
Box 1
Box 2
```

Normal flow.

---

# 2. position: relative

Moves an element relative to its original position.

Example:

```css
.box {
  position: relative;
  top: 20px;
  left: 30px;
}
```

Result:

```text
Original Position
       ↓
Moved 20px down
Moved 30px right
```

The original space remains reserved.

---

# Relative Example

HTML:

```html
<div class="box">Relative Box</div>
```

CSS:

```css
.box {
  position: relative;
  top: 20px;
}
```

The box moves down by 20px.

---

# Why Relative Is Important

Relative positioning is commonly used as a reference point for absolutely positioned children.

Example:

```css
.parent {
  position: relative;
}
```

This becomes very important later.

---

# 3. position: absolute

Removes the element from normal flow.

Example:

```css
.box {
  position: absolute;
  top: 0;
  right: 0;
}
```

Characteristics:

✅ Can be placed anywhere

❌ Does not reserve space

❌ Removed from normal layout

---

# Absolute Example

HTML:

```html
<div class="parent">
  <div class="child">Absolute</div>
</div>
```

CSS:

```css
.parent {
  position: relative;
  width: 300px;
  height: 200px;
}

.child {
  position: absolute;
  top: 0;
  right: 0;
}
```

Result:

```text
Parent
┌──────────────┐
│          Box │
└──────────────┘
```

The child is positioned relative to the parent.

---

# Important Rule

If no positioned parent exists:

```css
position: absolute;
```

uses:

```text
Browser Window
```

as the reference.

Always remember:

```css
.parent {
  position: relative;
}
```

---

# 4. position: fixed

Fixes an element to the viewport.

Example:

```css
.box {
  position: fixed;
  bottom: 20px;
  right: 20px;
}
```

Characteristics:

✅ Stays visible while scrolling

✅ Removed from normal flow

---

# Fixed Example

Floating button:

```css
.chat-button {
  position: fixed;
  bottom: 20px;
  right: 20px;
}
```

Common uses:

- Chat buttons
- Back to top buttons
- Floating menus

---

# 5. position: sticky

Acts like relative until scrolling reaches a point.

Then it becomes fixed.

Example:

```css
.navbar {
  position: sticky;
  top: 0;
}
```

Result:

```text
Scroll
↓
Navbar sticks to top
```

---

# Sticky Example

HTML:

```html
<nav>Navigation</nav>
```

CSS:

```css
nav {
  position: sticky;
  top: 0;
}
```

Common uses:

- Navigation bars
- Side menus
- Table headers

---

# Top, Right, Bottom, Left

Used with:

```css
relative
absolute
fixed
sticky
```

Example:

```css
.box {
  position: relative;
  top: 20px;
  left: 50px;
}
```

Meaning:

```text
20px down
50px right
```

---

# z-index

Controls stacking order.

Example:

```css
.box1 {
  z-index: 1;
}

.box2 {
  z-index: 2;
}
```

Result:

```text
Box 2 appears above Box 1
```

Higher value wins.

---

# z-index Example

HTML:

```html
<div class="red"></div>
<div class="blue"></div>
```

CSS:

```css
.red {
  position: absolute;
  z-index: 1;
}

.blue {
  position: absolute;
  z-index: 2;
}
```

Blue appears on top.

---

# Practical Example: Notification Badge

HTML:

```html
<div class="profile">
  <img src="avatar.jpg" alt="Avatar" />
  <span class="badge">3</span>
</div>
```

CSS:

```css
.profile {
  position: relative;
}

.badge {
  position: absolute;
  top: -5px;
  right: -5px;
}
```

Result:

Badge appears on the profile image.

---

# Practical Example: Sticky Navbar

CSS:

```css
nav {
  position: sticky;
  top: 0;
  background: white;
}
```

Navbar stays visible while scrolling.

---

# Common Mistakes

❌ Using absolute without a relative parent

```css
.child {
  position: absolute;
}
```

Unexpected positioning may occur.

---

✅ Better:

```css
.parent {
  position: relative;
}

.child {
  position: absolute;
}
```

---

❌ Using large z-index values

```css
z-index: 999999;
```

Can become difficult to manage.

---

# Best Practices

✅ Use relative for positioning context

✅ Use absolute for overlays and badges

✅ Use fixed for floating elements

✅ Use sticky for navigation

✅ Keep z-index values organized

---

# Summary

Position values:

```css
static
relative
absolute
fixed
sticky
```

Most common combination:

```css
.parent {
  position: relative;
}

.child {
  position: absolute;
}
```

Remember:

```text
Static   → Normal flow
Relative → Move from original position
Absolute → Position relative to parent
Fixed    → Stays on screen
Sticky   → Becomes fixed when scrolling
```

Mastering positioning is essential before learning Flexbox and Grid.
