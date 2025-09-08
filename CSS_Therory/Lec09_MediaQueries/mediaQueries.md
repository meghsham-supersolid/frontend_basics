# Media Queries

Media queries allow you to apply styles conditionally based on the characteristics of the device or screen rendering the content — such as screen width, height, resolution, orientation, and more.
For example, on YouTube, the video player and the playlist on the video page are placed side by side, but when the screen size is reduced (like on mobile), the video and playlist are stacked vertically.
They are a core part of responsive design, helping your website adapt to different devices such as phones, tablets, laptops, and desktops.

Syntax:

```
@media media-type and (condition) {
    /* CSS rules go here */
}
```

## List of Media Characteristics and Possible Values Used in CSS Media Queries

These are the characteristics you can use to make your design responsive across different devices.

### 1. Width and Height

Used to detect the size of the viewport (not the device screen).

| Feature    | Description                | Common Values / Units |
| ---------- | -------------------------- | --------------------- |
| width      | Exact width of viewport    | width: 768px          |
| min-width  | Minimum width of viewport  | min-width: 768px      |
| max-width  | Maximum width of viewport  | max-width: 1024px     |
| height     | Exact height of viewport   | height: 600px         |
| min-height | Minimum height of viewport | min-height: 500px     |
| max-height | Maximum height of viewport | max-height: 800px     |



### 3. Orientation

| Feature     | Description                | Values              |
| ----------- | -------------------------- | ------------------- |
| orientation | Detects screen orientation | portrait, landscape |

### 4. Color Preferences

| Feature              | Description                       | Values      |
| -------------------- | --------------------------------- | ----------- |
| prefers-color-scheme | Detects if user prefers dark mode | dark, light |

### 5. Motion and Contrast Preferences

| Feature                      | Description                         | Values                               |
| ---------------------------- | ----------------------------------- | ------------------------------------ |
| prefers-reduced-motion       | User prefers less motion/animations | reduce, no-preference                |
| prefers-reduced-transparency | User prefers less transparency      | reduce, no-preference                |
| prefers-contrast             | User prefers high/low contrast      | high, low, more, less, no-preference |

### 6. Aspect Ratio

| Feature          | Description                | Example Values         |
| ---------------- | -------------------------- | ---------------------- |
| aspect-ratio     | Width / height of viewport | 16/9, 3/2, 4/3         |
| min-aspect-ratio | Minimum aspect ratio       | min-aspect-ratio: 3/2  |
| max-aspect-ratio | Maximum aspect ratio       | max-aspect-ratio: 16/9 |

### 7. Resolution and Pixel Density

| Feature        | Description               | Values / Units         |
| -------------- | ------------------------- | ---------------------- |
| resolution     | Screen resolution         | 96dpi, 2dppx, 300dpi   |
| min-resolution | Minimum screen resolution | min-resolution: 2dppx  |
| max-resolution | Maximum screen resolution | max-resolution: 300dpi |

### 8. Pointer and Hover Capabilities

| Feature     | Description                        | Values             |
| ----------- | ---------------------------------- | ------------------ |
| pointer     | Type of pointing device            | none, coarse, fine |
| hover       | Whether device supports hover      | hover, none        |
| any-pointer | If any input device can point      | same as pointer    |
| any-hover   | If any input device supports hover | same as hover      |

### 9. Display Mode (for PWAs and apps)

| Feature      | Description              | Values                                      |
| ------------ | ------------------------ | ------------------------------------------- |
| display-mode | Detects app display mode | fullscreen, standalone, minimal-ui, browser |

# Applying Conditions

### 1. `and`

Used to combine multiple conditions. All conditions must be true for the styles to apply.

Example:

```css
@media (min-width: 768px) and (orientation: landscape) {
  /* Styles for screens wider than 768px AND in landscape mode */
}
```

### 2. `,` (comma) — behaves like OR

Used to apply styles if any one of the conditions is true. Acts like an OR.

Example:

```css
@media (max-width: 600px), (orientation: portrait) {
  /* Styles for either small screens OR portrait orientation */
}
```

> Note: CSS doesn’t have a keyword `or`. Instead, you separate queries with a comma.

### 3. `not`

Used to negate a condition. Applies styles if the condition is not true.

Example:

```css
@media not (min-width: 1024px) {
  /* Styles for screens smaller than 1024px */
}
```
