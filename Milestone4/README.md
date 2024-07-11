# CSS

CSS - Cascading Style Sheets.
CSS is the language we use to style an HTML document.
It controls the layout, colors, fonts, and overall appearance of web pages.

## Why CSS?

CSS is used to define styles for your web pages, including the design, layout and variations in display for different devices and screen sizes.

---

## Types of CSS

CSS can be classified into 3 categories
1. Inline CSS
2. Internal CSS
3. External CSS

# Types of CSS

CSS (Cascading Style Sheets) can be classified into three main categories:

## 1. Inline CSS
Inline CSS is added directly within the HTML tag using the `style` attribute.

```html
    <h1 style="color: blue; text-align: center;">This is a heading</h1>
    <p style="color: red;">This is a paragraph.</p>
```

## 2. Internal CSS
Internal CSS is placed within the <style> tag inside the <head> section of the HTML file.

```html
    <style>
        body {
            background-color: lightblue;
        }
        h1 {
            color: blue;
            text-align: center;
        }
        p {
            color: red;
        }
    </style>
```

## 3. External CSS
 External CSS is stored in a separate CSS file and linked to HTML documents using the <link> tag.

```html
    <link rel="stylesheet" href="styles.css">

styles.css

body {
    background-color: lightblue;
}
h1 {
    color: blue;
    text-align: center;
}
p {
    color: red;
}

```


