# CSS Transitions

Transitions allow you to create **smooth changes** between CSS states.

Instead of instant changes, you get animation-like effects.

---

# Why Transitions?

Without transitions:

❌ Changes happen instantly
❌ UI feels rough

With transitions:

✅ Smooth interactions
✅ Better user experience
✅ Modern UI feel

---

# Basic Syntax

```css id="a8k2qp"
transition: property duration timing-function delay;
```

---

# Simple Example

```css id="m4x9wv"
button {
  background-color: blue;
  transition: 0.3s;
}

button:hover {
  background-color: red;
}
```

👉 Smooth color change on hover

---

# Transition on Hover

```css id="k7m2qp"
.box {
  width: 100px;
  height: 100px;
  background: blue;
  transition: 0.5s;
}

.box:hover {
  width: 150px;
  background: green;
}
```

---

# transition-property

Defines what to animate.

```css id="t9x3wv"
transition-property: background-color;
```

Example:

```css id="q2k8qp"
button {
  transition-property: background-color;
}
```

---

# transition-duration

Controls how long animation takes.

```css id="v8m2qp"
transition-duration: 0.5s;
```

---

# transition-delay

Delays animation start.

```css id="x3k9wv"
transition-delay: 0.2s;
```

---

# transition-timing-function

Controls animation speed curve.

---

## linear

```css id="b7m2qp"
transition: 0.5s linear;
```

Same speed all the time.

---

## ease (default)

```css id="z5x8wv"
transition: 0.5s ease;
```

Slow → fast → slow

---

## ease-in

Starts slow.

---

## ease-out

Ends slow.

---

## ease-in-out

Smooth start and end.

---

# Complete Transition Example

```css id="p2k8qp"
button {
  background: blue;
  padding: 10px 20px;
  transition: background-color 0.3s ease;
}

button:hover {
  background: red;
}
```

---

# Multiple Properties

```css id="m8x3wv"
.box {
  transition:
    width 0.3s,
    height 0.3s;
}
```

---

# All Properties

```css id="k9m2qp"
transition: all 0.3s ease;
```

⚠️ Use carefully (can affect performance)

---

# Smooth Card Hover

```css id="v4x8wv"
.card {
  transition: 0.3s ease;
}

.card:hover {
  transform: scale(1.05);
}
```

---

# Button Hover Effect

```css id="t2k8qp"
button {
  background: #2563eb;
  color: white;
  transition: 0.3s ease;
}

button:hover {
  background: #1d4ed8;
}
```

---

# Common Mistakes

❌ No transition applied

```css id="x7m3wv"
button:hover {
  background: red;
}
```

❌ Using transition on hover only

```css id="k3x9qp"
button:hover {
  transition: 0.3s;
}
```

⚠️ Must be on base element

---

# Best Practices

✔ Use 0.2s – 0.5s for UI
✔ Use ease or ease-in-out
✔ Apply transitions on base element
✔ Avoid animating layout-heavy properties

---

# What NOT to Animate

❌ width (can cause lag)
❌ height (can cause lag)
❌ top/left (use transform instead)

---

# Better Alternative

Instead of:

```css id="m2x8wv"
left: 20px;
```

Use:

```css id="t8k3qp"
transform: translateX(20px);
```

---

# Real UI Example

```css id="q7m9wv"
.card {
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}
```

---

# Summary

Transitions make UI feel alive:

```css id="v9x2wv"
transition: property duration timing-function delay;
```

Core idea:

```text id="k4x8qp"
State A → Smooth transition → State B
```

---

# Final Thought

Transitions are the first step into motion design in CSS 🎬
