# Sizes and Units

## Absolute Length Units :

- based on an actual physical unit, and are generally considered to be the same size across devices. However, depending on your screen size and quality, or settings in your browser or OS, there may be some exceptions.

### px

     - with the introduction of modern displays which have more resolution px size can vary screen to screen
     - All other absolute length units are based on this definition of a pixel.
     - in absolute length px is most used

- If you know that your page will be printed on a high quality printer, then you may consider using another unit like cm or mm.
  and other than that, in, pt, pc are units that are also used.

## Relative Length Units

- Relative length units are relative to another element's size or settings. For example, the relative font size of an element may be calculated using the parent element's font size.

Here are some common relative length units:

### 1. em

    The CSS em unit gets its name from a typographical unit. In typography, the term em "was originally a reference to the width of the capital M in the typeface and size being used". When used with the font-size property, em inherits the font-size from its parent element:

         .container {
         font-size: 16px;
         }

         .container p {
         font-size: 1em;
         }

         .container h2 {
         font-size: 3em;
         }

         .container h3 {
         font-size: 2em;
         }

In this example, the font-size of p is 16px (16 1). Meanwhile, the font-size of h2 is 48px (16 3), and 32px for the h3 (16 \* 2).

If em is used with another property like width, em is calculated using the size of the targeted element.

### 3.rem

Root em. This relative unit is not affected by the size or setting of a parent element, and is instead based on the root of the document. For websites, the root of the document is the html element.

```
p {
font-size: 1.25rem;
}
```

In most browsers, the default font size is 16, so the font-size of html elements is 16px. So in this case, p is 20px (16 \* 1.25).

But if a user changes their browser's default font size, then the font-size of p will scale up or down accordingly.

### 4. %

Percentages, or the percent size relative to the parent's size:

div {
width: 400px;
}

```
div p {
width: 75%;
}
```

Since the parent’s width is 400px, the width of the inner paragraph is be 300px (400 \* .75).

### 5. vw

View width. 1vw is 1% of the width of the viewport.

For example:

```
body {
width: 100vw;
}
```

Since the body element is set to 100vw, or 100% of the viewport's width, it will take up the full width available to it. So if you resize your browser to 690 pixels wide, then the body will take up all 690 pixels in width.

### 6. vh

View height. 1vh is 1% of the height of the viewport.

For example:

```
div {
height: 50vh;
}
```

The div will fill 50% of the viewport's height. So if the browser window is 900 pixels high, the height of the div will be 450 pixels.

### 7. ex

The CSS ex unit gets its name from x-height in typography, or "the height of the letter x in the font". In many fonts, the lowercase x character is usually about half the height of the largest character.

An image showing the x-height of the word Sphinx.Source

In CSS, 1ex is the x-height of the font, or half of 1em.

But since the size of the lowercase x character can vary significantly based on the font, the CSS ex unit is rarely used.

### 8. ch

Character unit. The CSS ch unit is defined as the width of the character 0 (zero, or U+0030) of the font.

While the ch unit works as an exact measurement for monospaced / fixed width fonts like Courier, it can be unpredictable with proportional fonts like Arial.

For example, if your font is Courier and you set an element's width to 60ch, that element will be 60 exactly 60 characters wide.

But if your font is Arial and you set an element's width to 60ch there's no telling how wide the element will be – characters may overflow the container, or fall short.

An image showing 20ch as an exact measurement in Courier, but inexact in Helvetica and Georgia fonts.Source

Check out this article for an in-depth explanation of the ch unit, and to see some examples.

### 9. vmin and vmax

Viewport minimum (vmin) and viewport maximum (vmax) units are based on the values of vw and vh.

1vmin is 1% of the viewport's smallest dimension, and 1vmax is 1% of the viewports largest dimension.

For example, imagine a browser window that is 1200 pixels wide and 600 pixels high. In this case, 1vmin is 6px (1% of vh, which is smaller at 600 pixels). Meanwhile, 1vmax is 12px (1% of vh, which is the larger value at 1200 pixels).

# Summery

## Absolute Units

| **Unit**         | **What it is**                    | **When to Use**                                  |
| ---------------- | --------------------------------- | ------------------------------------------------ |
| `px`             | Pixel — smallest screen unit      | Most commonly used; reliable on screens          |
| `cm`, `mm`, `in` | Centimeters, millimeters, inches  | Use for print media, not recommended for screens |
| `pt`, `pc`       | Points, picas (print-based units) | Rarely used, mainly in print                     |

## Relative Units |

| **Unit** | **What it is**                           | **When to Use**                                 |
| -------- | ---------------------------------------- | ----------------------------------------------- |
| `em`     | Relative to **parent's font-size**       | Good for scaling typography locally             |
| `rem`    | Relative to **root element's font-size** | Better for global scaling (consistent sizes)    |
| `%`      | Relative to **parent element**           | Use for flexible layouts (e.g., widths)         |
| `vw`     | 1% of viewport **width**                 | For full-width elements or responsive scaling   |   
| `vh`     | 1% of viewport **height**                | For responsive height control                   |
| `vmin`   | 1% of **smaller** viewport dimension     | For fully responsive scaling                    |
| `vmax`   | 1% of **larger** viewport dimension      | Use for full coverage regardless of orientation |
| `ch`     | Width of character `0` in font           | Best for monospaced text (e.g., input fields)   |
| `ex`     | Height of lowercase `x`                  | Rarely used due to inconsistency                |

## Quick Recommendations

Use rem for consistent font sizes across your site.

Use %, vw, vh for responsive layouts.

Use px when you need pixel-perfect control (less flexible).

Avoid ex and ch unless you're doing precise typographic layout.

Use em when styling elements that need to inherit size from their parent.
 