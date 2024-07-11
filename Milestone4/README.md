# 1. CSS

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

---

# 2. SASS

Sass is a CSS pre-processor
Sass stands for Syntactically Awesome Stylesheet
Sass reduces repetition of CSS and therefore saves time

Stylesheets are getting larger, more complex, and harder to maintain. This is where a CSS pre-processor can help.

# Sass Variable

- Variables are used to store a value.
  
Values can be 
    strings
    numbers
    colors
    booleans
    lists
    nulls

Syntax : $variablename: value;

Variable scope in Sass:

Sass variables are only available at the level of nesting where they are defined.

```html
$myColor: red;

h1 {
  $myColor: green;
  color: $myColor;
}

p {
  color: $myColor;
}
```
O/p: Green has scope limited to h1 tag only.


Sass !global:

!global indicates that a variable is global, which means that it is accessible on all levels.

```html
$myColor: red;

h1 {
  $myColor: green !global;
  color: $myColor;
}

p {
  color: $myColor;
}     
```
O/p : Green is globally declared

---

##  Sass Nesting

Many CSS properties have the same prefix, like font-family, font-size and font-weight or text-align, text-transform and text-overflow.
With Sass, we can write them as nested properties.

```html
font: {
  family: Helvetica, sans-serif;
  size: 18px;
  weight: bold;
}

text: {
  align: center;
  transform: lowercase;
  overflow: hidden;
}
```

## Sass @import

The @import directive allows you to include the content of one file in another.

```scss
@import 'filename';
```

## Sass @mixin



