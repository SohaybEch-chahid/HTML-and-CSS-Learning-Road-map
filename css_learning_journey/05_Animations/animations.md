# CSS Animations

CSS Animations allow elements to move and change styles automatically over time.

Unlike transitions (which need interaction), animations run on their own.

They are used for:

- Loading spinners 🔄
- Bouncing elements
- Fading effects
- Attention effects
- Complex UI motion

---

# Why Animations?

Without animations:

❌ Static UI
❌ No motion feedback

With animations:

✅ Dynamic UI
✅ Better user experience
✅ Modern design feel

---

# Basic Structure

CSS animations use two parts:

1. `@keyframes` (defines animation steps)
2. `animation` property (applies animation)

---

# 1. @keyframes

Defines what happens during the animation.

```css id="a8k2qp"
@keyframes example {
  from {
    background-color: red;
  }
  to {
    background-color: blue;
  }
}
```

---

# 2. Apply Animation

```css id="m4x9wv"
.box {
  animation: example 2s;
}
```

---

# Simple Example

```css id="k7m2qp"
@keyframes colorChange {
  from {
    background: blue;
  }
  to {
    background: red;
  }
}

.box {
  width: 100px;
  height: 100px;
  animation: colorChange 2s;
}
```

---

# Animation States

Instead of just from/to, you can use percentages:

```css id="t9x3wv"
@keyframes moveBox {
  0% {
    transform: translateX(0);
  }

  50% {
    transform: translateX(100px);
  }

  100% {
    transform: translateX(0);
  }
}
```

---

# Animation Properties

---

# 1. animation-name

```css id="q2k8qp"
animation-name: moveBox;
```

---

# 2. animation-duration

```css id="v8m2qp"
animation-duration: 2s;
```

---

# 3. animation-delay

```css id="x3k9wv"
animation-delay: 1s;
```

---

# 4. animation-iteration-count

How many times it repeats.

```css id="b7m2qp"
animation-iteration-count: infinite;
```

Or:

```css id="z5x8wv"
animation-iteration-count: 3;
```

---

# 5. animation-direction

```css id="p2k8qp"
animation-direction: normal;
animation-direction: reverse;
animation-direction: alternate;
animation-direction: alternate-reverse;
```

---

# 6. animation-timing-function

Controls speed curve:

```css id="m8x3wv"
linear
ease
ease-in
ease-out
ease-in-out
```

---

# Full Example

```css id="k9m2qp"
@keyframes bounce {
  0% {
    transform: translateY(0);
  }

  50% {
    transform: translateY(-50px);
  }

  100% {
    transform: translateY(0);
  }
}

.box {
  width: 100px;
  height: 100px;
  background: blue;
  animation: bounce 1s infinite;
}
```

---

# Loading Spinner Example

```css id="v4x8wv"
@keyframes spin {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}

.loader {
  width: 50px;
  height: 50px;
  border: 5px solid #ccc;
  border-top: 5px solid blue;
  border-radius: 50%;
  animation: spin 1s linear infinite;
}
```

---

# Fade In Animation

```css id="t2k8qp"
@keyframes fadeIn {
  from {
    opacity: 0;
  }

  to {
    opacity: 1;
  }
}

.box {
  animation: fadeIn 2s ease-in;
}
```

---

# Slide In Animation

```css id="x7m3wv"
@keyframes slideIn {
  from {
    transform: translateX(-100px);
    opacity: 0;
  }

  to {
    transform: translateX(0);
    opacity: 1;
  }
}
```

---

# Pulse Effect

```css id="k3x9qp"
@keyframes pulse {
  0% {
    transform: scale(1);
  }

  50% {
    transform: scale(1.1);
  }

  100% {
    transform: scale(1);
  }
}

.box {
  animation: pulse 1s infinite;
}
```

---

# Multiple Animations

```css id="m2x8wv"
.box {
  animation:
    fadeIn 1s ease,
    slideIn 1s ease;
}
```

---

# Animation Fill Mode

Controls final state:

```css id="t8k3qp"
animation-fill-mode: forwards;
```

Values:

- none
- forwards
- backwards
- both

---

# Pause Animation

```css id="q7m9wv"
.box:hover {
  animation-play-state: paused;
}
```

---

# Performance Tip

✔ Use transform and opacity
❌ Avoid animating width/height

Better performance:

```css id="v9x2wv"
transform: translateX();
opacity: 0;
```

---

# Real UI Example

Card animation:

```css id="k4x8qp"
@keyframes float {
  0% {
    transform: translateY(0);
  }

  50% {
    transform: translateY(-10px);
  }

  100% {
    transform: translateY(0);
  }
}

.card {
  animation: float 3s ease-in-out infinite;
}
```

---

# Common Mistakes

❌ Animating layout properties

```css id="m7x2wv"
width: 200px;
height: 200px;
```

❌ Too fast animations

```css id="c9k3qp"
animation: move 0.1s;
```

---

# Best Practices

✔ Use subtle animations
✔ Prefer transform + opacity
✔ Use ease-in-out
✔ Keep duration 0.3s – 2s
✔ Don’t overuse animations

---

# Summary

CSS Animation structure:

```css id="v1h0fu"
@keyframes name {
  0% {
  }
  100% {
  }
}

element {
  animation: name duration timing delay iteration direction;
}
```

---

# Final Idea

Think of animations like this:

```text id="k9m3qp"
Static UI → Motion → Life ✨
```

Animations make your websites feel modern, smooth, and interactive 🚀
