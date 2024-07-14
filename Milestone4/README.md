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


## Sass !global:

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

Sass String functions:
```

## Sass @mixin

Sass mixin used to define reusuable styling components.

```scss
@mixin theme($theme: DarkGray) {
  background: $theme;
  color: #fff;
}

.alert {
  @include theme($theme: DarkRed);
}
.success {
  @include theme($theme: DarkGreen);
}
```

## Sass @extend / Inheritance

The @extend directive lets you share a set of CSS properties from one selector to another.

```scss
%message-shared {
  border: 1px solid #ccc;
}

.success {
  @extend %message-shared;
  border-color: green;
}
```
---

## Sass String Functions

Functions used to deal with strings

| Function                      | Description                                | Example                                    | Result                    |
|-------------------------------|--------------------------------------------|--------------------------------------------|---------------------------|
| `quote(string)`               | Adds quotes to string.                     | `quote("Hello world!")`                    | `"Hello world!"`          |
| `str-index(string, substring)`| Index of the first occurrence of substring.| `str-index("Hello world!", "H")`           | `1`                       |
| `str-insert(string, insert, index)` | Inserts string at index.                   | `str-insert("Hello world!", " wonderful", 6)`| `Hello wonderful world!`  |
| `str-length(string)`          | Returns the length of the string.          | `str-length("Hello world!")`               | `12`                      |
| `str-slice(string, start, end)` | Slices string from start to end.            | `str-slice("Hello world!", 2, 5)`          | `"ello"`                  |
| `to-lower-case(string)`       | Converts string to lower case.             | `to-lower-case("Hello World!")`            | `"hello world!"`          |
| `to-upper-case(string)`       | Converts string to upper case.             | `to-upper-case("Hello World!")`            | `"HELLO WORLD!"`          |
| `unique-id()`                 | Generates a unique string.                 | `unique-id()`                              | `tyghefnsv`               |
| `unquote(string)`             | Removes quotes around string.              | `unquote("Hello world!")`                  | `Hello world!`            |


## Sass Numeric Functions

Functions used to deal with numerical operations

| Function                 | Description                              | Example Code                    | Result   |
|--------------------------|------------------------------------------|---------------------------------|----------|
| `abs(number)`            | Returns the absolute value of number.    | `abs(-15)`                      | `15`     |
| `ceil(number)`           | Rounds number up to the nearest integer. | `ceil(15.20)`                   | `16`     |
| `comparable(num1, num2)` | Checks if num1 and num2 are comparable.  | `comparable(15px, 10px)`        | `true`   |
| `floor(number)`          | Rounds number down to the nearest integer. | `floor(15.80)`               | `15`     |
| `max(number...)`         | Returns the highest value.               | `max(5, 7, 9, 0, -3, -7)`       | `9`      |
| `min(number...)`         | Returns the lowest value.                | `min(5, 7, 9, 0, -3, -7)`       | `-7`     |
| `percentage(number)`     | Converts number to a percentage.         | `percentage(1.2)`               | `120%`   |
| `random()`               | Returns a random number between 0 and 1. | `random()`                      | `0.45673`|
| `random(number)`         | Returns a random integer between 1 and number. | `random(6)`              | `4`      |
| `round(number)`          | Rounds number to the nearest integer.    | `round(15.20)`                  | `15`     |

## Sass List Functions

The list functions are used to access values in a list, combine lists, and add items to lists.


| Function                        | Description                                          | Example Code                                 | Result                        |
|---------------------------------|------------------------------------------------------|----------------------------------------------|-------------------------------|
| `append(list, value, [separator])` | Adds a value to the end of the list. Separator can be `auto`, `comma`, or `space`. | `append((a b c), d)`                         | `a b c d`                     |
| `index(list, value)`            | Returns the index of the value in the list.          | `index(a b c, b)`                            | `2`                           |
| `is-bracketed(list)`            | Checks if the list has square brackets.              | `is-bracketed([a b c])`                      | `true`                        |
| `length(list)`                  | Returns the length of the list.                      | `length(a b c)`                              | `3`                           |
| `list-separator(list)`          | Returns the list separator used, as a string.        | `list-separator(a b c)`                      | `"space"`                     |


## Sass Map Functions

In Sass, the map data type represents one or more key/value pairs.

| Function                         | Description                                           | Example Code                                                                                             | Result                                                      |
|----------------------------------|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| `map-get(map, key)`              | Returns the value for the specified key in the map.   | `$font-sizes: ("small": 12px, "normal": 18px, "large": 24px)`<br>`map-get($font-sizes, "small")`          | `12px`                                                      |
| `map-has-key(map, key)`          | Checks whether map has the specified key.             | `$font-sizes: ("small": 12px, "normal": 18px, "large": 24px)`<br>`map-has-key($font-sizes, "big")`        | `false`                                                     |
| `map-keys(map)`                  | Returns a list of all keys in map.                    | `$font-sizes: ("small": 12px, "normal": 18px, "large": 24px)`<br>`map-keys($font-sizes)`                  | `"small", "normal", "large"`                                |


---

## 3.  Scss

SCSS and SASS are both syntaxes of the SASS preprocessor

SCSS (Sassy CSS) is a syntax of SASS, offering a more CSS-like syntax.

It has the following properties
    Variables
    @mixins
    @extend
    Nesting

| Feature         | SCSS                                      | Sass                                     |
|-----------------|-------------------------------------------|------------------------------------------|
| Syntax          | Uses curly braces `{}` and semicolons `;` | Uses indentation to separate code blocks |
| Compatibility   | Every valid CSS file is a valid SCSS file | Requires specific Sass syntax            |
| Readability     | Similar to standard CSS                   | More concise, fewer characters to write  |
| File Extension  | `.scss`                                   | `.sass`                                  |


## 4. CSS Properties

## Height

In CSS, `height` and `width` are properties used to define the dimensions of an element.

- **Syntax of Height**: `height: value;`
- 
- **Values**:
- 
  - `auto`: Default value, element height adjusts based on content.
  - `px`: Specifies height in pixels.
  - `%`: Specifies height as a percentage of the parent element's height.
  - `em`, `rem`: Relative units based on font-size.
  - `vh`: Viewport height (1vh = 1% of the viewport height).

**Example:**
```css
.element {
    height: 200px; /* Fixed height in pixels */
}
```

## Max Height
In CSS, `max-height` specifies the maximum height an element can take before it starts to overflow. 

```css
.element {
    max-height: 300px; /* Set maximum height */
    overflow: auto;    /* Add scrollbars if content overflows */
}
```

   
## Width

- **Syntax of Width**: `width: value;`
- 
- **Values**:
- 
  - `auto`: Default value, element height adjusts based on content.
  - `px`: Specifies height in pixels.
  - `%`: Specifies height as a percentage of the parent element's height.
  - `em`, `rem`: Relative units based on font-size.
  - `vw`: Viewport Width (1vh = 1% of the viewport width).

**Example:**
```css
.element {
    width: 200px; /* Fixed height in pixels */
}
```

---
## Max width

In CSS, `max-width` specifies the maximum width an element can take before it starts to overflow. 

```css
.element {
    max-width: 600px; /* Limits the width to 600 pixels */
}
```

---

## CSS Border

It is used to create border to the webpage

## Border Styles in css:

| Value   | Description                                      |
|---------|--------------------------------------------------|
| `dotted`| Defines a dotted border                           |
| `dashed`| Defines a dashed border                           |
| `solid` | Defines a solid border                            |
| `double`| Defines a double border                           |
| `groove`| Defines a 3D grooved border                       |
| `ridge` | Defines a 3D ridged border                        |
| `inset` | Defines a 3D inset border                         |
| `outset`| Defines a 3D outset border                        |
| `none`  | Defines no border                                 |
| `hidden`| Defines a hidden border                           |


Example:

```css
.element {
    border: 2px ridge #ccc; 
}
```
---

## CSS Background

The background peroperty adds background effects to the element

## CSS Background Properties

### 1 `background-color`
- **Definition**: Sets the background color of an element.
- **Example**: 
  ```css
  .example {
      background-color: #f0f0f0; /* Light gray background */
  }
  ```

### 2 `background-image`
- **Definition**: Sets one or more background images for an element.
- **Example**: 
```css
.example {
    background-image: url('background.jpg'); /* Sets a background image */
}
 ```
      
### 3 `background-repeat`
- **Definition**:  Specifies how background images should repeat.
- **Example**: 
```css
.example {
    background-repeat: no-repeat; /* Prevents background image from repeating */
}
 ```

### 4 `background-attachment`
- **Definition**: Specifies whether a background image is fixed or scrolls with the content.
- **Example**: 
```css
.example {
    background-attachment: fixed; /* Fixes the background image in place */
}
 ```

### 5 `background-position`
- **Definition**: Sets the starting position of background images.
```css
.example {
    background-position: center top; /* Positions background image at the top center */
}
```

---

## CSS Box Model

In CSS, every element is considered as a rectangular box. 
The CSS box model describes the space that surrounds an HTML element, including its content, padding, border, and margin.

### Components of the Box Model:

1. **Content**: The actual content of the element, where text and images appear.

2. **Padding**: Clears an area around the content. The padding is transparent.

3. **Border**: A border that goes around the padding and content.

4. **Margin**: Clears an area outside the border. The margin is transparent.
   <br />
<p align="center">
  <img src="https://github.com/user-attachments/assets/54759d97-671d-479c-9cff-2b5c0bb546ea" width="600" height="400" />
</p>

<br />


```css
div {
  width: 320px;
  height: 50px;
  padding: 10px;
  border: 5px solid gray;
  margin: 0;
}
```

## CSS Margin


In CSS, `padding` is properties used to control the space around  elements, respectively.

### `margin`

- **Definition**: Sets the space outside an element's border.
- 
- **Example**: 
  ```css
  .example {
      margin: 10px; /* Applies 10 pixels of margin to all sides */
  }

## CSS Padding

In CSS, `padding` is a property used to create space around an element's content, inside the element's border.

### Definition

The `padding` property controls the amount of space between the content of an element and its border.

### Syntax

```css
selector {
    padding: value;
}
```

## CSS Fonts

CSS provides several properties to style fonts and text within HTML elements.

## 1. `font-family`

### Definition
The `font-family` property specifies the font family for text. It allows you to define a prioritized list of font family names or generic family names.


### Example
```css
body {
  font-family: "Arial", sans-serif;
}
```
### Font Family

- Serif fonts have a small stroke at the edges of each letter. They create a sense of formality and elegance.
- Sans-serif fonts have clean lines (no small strokes attached). They create a modern and minimalistic look.

---
### Web safe fonts:

Web safe fonts are fonts that are widely available across different operating systems and devices. Here are some commonly used web safe fonts:

- Arial
- Times New Roman
- Georgia
- Verdana

---

## CSS Font Size

The `font-size` property in CSS sets the size of the text within HTML elements.

## Absolute Size (Pixels - `px`)

- Sets the text size to a specific pixel value.
- Does not allow users to change text size in browsers, which can be a drawback for accessibility.
  
Example:
```css
h1 {
  font-size: 40px;
}

p {
  font-size: 14px;
}
```

## Relative Size ( em )

Example:

- Sets text size relative to its parent element.
- Allows users to adjust text size in browsers, improving accessibility.

```css
h1 {
  font-size: 2.5em; 
}

p {
  font-size: 0.875em; 
}

```

---

## CSS Texts

CSS offers several properties to style and manipulate text within HTML elements.

## 1. Color (`color`)

### Definition
The `color` property sets the color of text.

### Example
```css
p {
  color: #333333; /* Dark gray */
}
```

## 2. Alignment

### Definition
The text-align property aligns text horizontally within its container.

### Example
```css
h1 {
  text-align: center;
}

```

## 3. Decorations

### Definition
The text-decoration property decorates text with underlines, overlines, etc.

- text-decoration-line
- text-decoration-color
- text-decoration-style
- text-decoration-thickness
- text-decoration

### Example
```css
a {
  text-decoration: none; /* Removes underline from links */
}

```

## 4. Transformation

### Definition
The text-transform property transforms text to uppercase, lowercase, etc.

- uppercase
- lowercase
- capitalize

### Example
```css
button {
  text-transform: uppercase;
}

```

## 5. Shadow

### Definition
The text-shadow property adds shadow effects to text.

### Example
```css
h2 {
  text-shadow: 2px 2px 4px #000000;
}

```

---

## CSS Image

CSS offers several properties to style and control the display of images within HTML elements.

## 1. Image Size (`width` and `height`)

### Definition
You can set the dimensions of an image using the `width` and `height` properties.

### Example
```css
img {
  width: 100px;
  height: 100px;
}
```

## 2. Image Border
Provides border to the image

    .image {
      border: 5px solid black;
    }


## 3. Image Display options
Provides various display options for image

    .image {
      display: block;
      margin: 10px;
      padding: 15px;
    }


## 4. Image Shadow
Adds a shadow effect to image

    .image {
      box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);
    }

---

# CSS Display Property

The CSS `display` property determines how an element behaves in the document layout.

## Values:

- **`block`**: Renders the element as a block-level element (e.g., `<div>`). Takes up the full width available.
  
- **`inline`**: Renders the element as an inline-level element (e.g., `<span>`). Occupies only as much width as necessary.
  
- **`inline-block`**: Combines features of inline and block elements. Allows setting width and height, and respects margins and padding.
  
- **`flex`**: Enables a flex container and lays out its direct children as flex items.
  
- **`grid`**: Enables a grid container and lays out its direct children as grid items.
  
- **`none`**: Hides the element from the layout (not from screen readers).

- **`table`**: Renders the element as a block-level table element, similar to `<table>` in HTML.

- **`inline-table`**: Renders the element as an inline-level table element, similar to `<table>` in HTML.

- **`list-item`**: Renders the element as a block container with a list-item box inside (e.g., `<li>`).

- **`inherit`**: Inherits the `display` value from its parent element.

- **`initial`**: Sets the `display` property to its default value.

- **`unset`**: Resets the `display` property to its inherited value if it inherits from its parent, otherwise sets it to its initial value.

### Example:

```css
.element {
  display: block;
}
```

---

## CSS Flexbox

Flexbox is used to craete flexible layout structures.

Flexbox has 2 components
 - Flex container (Outer box)
 - Flex items (Elements inside the container)

### Main Axis:
  It is the primary axis.

### Cross Axis:
  The cross axis is perpendicular to the main axis.
  
-  If flex-direction is row, main axis is row, cross axis is column
-  If flex-direction is column, main axis is column, cross axis is row

---

## Flexbox properties:

### flex-direction

- flex-direction: row
  
![Screenshot 2024-07-14 123908](https://github.com/user-attachments/assets/d0296b69-b71e-4231-9347-7b0d6722488a)

- flex-direction: column
  
   ![Screenshot 2024-07-14 123938](https://github.com/user-attachments/assets/c2ca1151-2dd5-4bac-82cb-20aa542484df)

- flex-direction: row-reverse
![Screenshot 2024-07-14 123959](https://github.com/user-attachments/assets/4850e5c0-7ee6-40c1-846f-80caba6414c9)

---

### flex wrap:

Allow us to wrap the items in a single line or multiple lines

### flex grow:

 flex-grow determines how much a flex item should grow relative to the other

![Screenshot 2024-07-14 124655](https://github.com/user-attachments/assets/a7a0d8f7-8b27-4af7-9649-34521881efc8)

### flex basis:

Sets the initial size of flex items

![Screenshot 2024-07-14 125256](https://github.com/user-attachments/assets/8b12cc30-f8a0-40a4-b3cf-42233066d795)


---

## Justify content (If row is main axis)

justify-content : flex start | flex end | space between | space around;

  
![Screenshot 2024-07-14 124332](https://github.com/user-attachments/assets/de1b8bee-9d01-4748-beb8-6aaa5674edea)


## Align Items (If column is main axis)

align items: flex-start | flex-end | baseline | initial | inherit;

![Screenshot 2024-07-14 125448](https://github.com/user-attachments/assets/bebb75df-df8e-48b5-8e65-6768d57888b8)




