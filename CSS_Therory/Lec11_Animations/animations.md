Here's a revised and **complete note on CSS Animations**, with all the relevant animation properties, **possible values**, and **corrections** to syntax and explanations:

# 🎞️ **Animations in CSS**

CSS animations make it possible to animate transitions from one CSS style configuration to another.
The `animation` property in CSS can animate many CSS properties like `color`, `background-color`, `height`, `width`, `transform`, etc.

Animations are defined using the `@keyframes` rule and applied using the `animation` or related properties.

## ✅ **Steps to Create and Apply Animations in CSS**

### **1. Define a Named Animation Rule**

Use the `@keyframes` at-rule to define the animation steps.

```css
@keyframes <animation-name> {
  from {
    /* CSS properties at the start of the animation */
  }
  to {
    /* CSS properties at the end of the animation */
  }
}

/* OR use percentage values for more control */

@keyframes <animation-name> {
  0% {
    /* Start */
  }
  50% {
    /* Mid-point */
  }
  100% {
    /* End */
  }
}
```

> 🔹 `@keyframe` is incorrect — it should always be `@keyframes` (with an `s`).

### **2. Apply the Animation Using Properties**

Each animation property controls a different aspect of how the animation behaves.

#### 🏷️ 2.1 `animation-name`

Specifies the name of the `@keyframes` animation to apply.

```css
animation-name: slideIn;
```

- **Possible Values:** Any valid identifier (must match the defined `@keyframes` name)

#### ⏱️ 2.2 `animation-duration`

Specifies how long one cycle of the animation takes.

```css
animation-duration: 2s;
```

- **Possible Values:** `<time>`
  E.g., `1s`, `500ms`, `0.8s`

#### 🔁 2.3 `animation-iteration-count`

Defines how many times the animation should repeat.

```css
animation-iteration-count: infinite;
```

- **Possible Values:**

  - A number: `1`, `3`, `5.5`
  - `infinite` — animation never stops

#### ⏳ 2.4 `animation-delay`

Specifies a delay before the animation starts.

```css
animation-delay: 1s;
```

- **Possible Values:** `<time>`
  E.g., `0s`, `2s`, `250ms`

#### 🧮 2.5 `animation-timing-function`

Specifies the acceleration curve (easing) of the animation.

```css
animation-timing-function: ease-in-out;
```

- **Possible Values:**

  - `ease` (default)
  - `linear`
  - `ease-in`
  - `ease-out`
  - `ease-in-out`
  - `step-start`, `step-end`
  - `steps(n, start|end)`
  - `cubic-bezier(x1, y1, x2, y2)` — custom easing

#### 🔄 2.6 `animation-direction`

Specifies whether the animation should play forwards, backwards, or alternate.

```css
animation-direction: alternate;
```

- **Possible Values:**

  - `normal` (default)
  - `reverse`
  - `alternate`
  - `alternate-reverse`

#### 🎯 2.7 `animation-fill-mode`

Specifies how styles are applied before/after animation runs.

```css
animation-fill-mode: both;
```

- **Possible Values:**

  - `none` (default)
  - `forwards` — retain final state after animation ends
  - `backwards` — apply styles before animation starts
  - `both` — apply both `forwards` and `backwards`

#### ⏸️ 2.8 `animation-play-state`

Allows pausing and resuming of animation.

```css
animation-play-state: paused;
```

- **Possible Values:**

  - `running` (default)
  - `paused`

### 🧾 **Shorthand Property: `animation`**

Instead of writing each property individually, you can combine them into the `animation` shorthand:

```css
animation: <name> <duration> <timing-function> <delay> <iteration-count>
  <direction> <fill-mode> <play-state>;
```

#### ✅ Example:

```css
animation: fadeIn 2s ease-in 0.5s infinite alternate both running;
```

> Not all values are required — you can use as few or as many as needed. The only required value is `animation-name`.

### 🧪 Example of a Complete Animation

```css
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.box {
  animation: fadeIn 2s ease-in-out 0s 3 alternate both running;
}
```
