
## CSS Selectors

A CSS selector selects the HTML element(s) you want to style.

**Types of selectors**:
- Element Selector
    Select an element and apply styling to it.
  
    ```html
    p {
    ...
    }
    ```    
    
- Grouping Selector
    Select multiple elements at a time and apply styling effects  

   ```html
    p, h1, h2 {
    ...
    }
    
- Class Selector
    The selector .class is used to select the elements (group) that belong to the specific class attribute.

  ```html
    .class1 {
    ...
    }
  
- Id Selector
    The id selector uses the id attribute of an HTML element to select a specific element.

    ```html
    #id1 {
    ...
    }
    
- Universal Selector
      It applies the styling to all the elements

    ```html
    * {
    ...
    }

---

## CSS Combinators

Combinators defines the relationship between the selectors. 

There are four different combinators in CSS:

- descendant selector (space)
- child selector (>)
- adjacent sibling selector (+)
- general sibling selector (~)

![WhatsApp Image 2024-07-13 at 15 53 48_2c435111](https://github.com/user-attachments/assets/9acf2bd3-8dcf-4a77-b009-42de7f902f93)


---

## CSS Pseudo class and elements

A pseudo-class is used to define a special state of an element.

    ```html
    selector:pseudo-class {
      property: value;
    }

## CSS Pseudo-Classes

| Pseudo-Class      | Description                                                              | Example                                                  |
|-------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| `:hover`          | Applies when cursor moves to the element, but does not activate it. | ```button:hover { background-color: yellow; }``` |
| `:active`         | Applies while an element is being activated by the user.                | ```a:active { color: red; }<br>```                 |
| `:first-child`    | Applies to the first child of its parent.                                | ```p:first-child { font-weight: bold; }```     |
| `:last-child`     | Applies to the last child of its parent.                                 | ```p:last-child { color: green; }```           |
| `:root`           | Applies to the root element of a document.                               | ```:root { --main-color: coral; }```           |

## CSS Pseudo Elements

A CSS pseudo-element is used to style specified parts of an element.

```html
selector::pseudo-element {
  property: value;
}
```

| Pseudo-Element  | Description                                                           | Example                                                    |
|-----------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| `::before`      | Inserts content before the content of selected elements.               | ```p::before { content: "Before text "; }```    |
| `::after`       | Inserts content after the content of selected elements.                | ```p::after { content: " After text"; }```      |
| `::first-line`  | Styles the first line of text within a selected element.               | ```p::first-line { color: blue; }```             |
| `::first-letter`| Styles the first letter of the text within a selected element.         | ```p::first-letter { font-size: 150%; }```       |
| `::selection`   | Styles the portion of an element that is selected by a user.           | ```::selection { background-color: yellow; color: black; }``` |


## ! important

The !important rule in CSS is used to add more importance to a property/value than normal.

```html
#myid {
  background-color: blue;
}

.myclass {
  background-color: gray;
}

p {
  background-color: red !important;
}
```

The only way to override an !important rule is to include another !important rule on a declaration with the same (or higher) specificity 

---

## CSS Specificity

<p align="center">
  <img src="https://github.com/user-attachments/assets/e93024a4-2293-4313-b93d-100c8244bae2" alt="Example Image" height="700" width="600">
</p>

---

## CSS Inheritance

Inheritance is a property where the parent styling transferred to the child styling.


### inherit keyword

The inherit keyword in CSS explicitly sets a property value to be inherited from its parent element.

```html
 <style>
        .parent {
            color: blue;
            font-size: 20px;
        }

        .child {
            color: inherit; 
            font-size: inherit; 
        }
    </style>
```

### Inherited and Non Inherited Properties

- **Inherited Properties**: These properties are automatically inherited from the parent element to its child elements unless explicitly overridden.
- **Non-Inherited Properties**: These properties are not inherited and must be explicitly defined for each element.


| Inherited Properties   | Non-Inherited Properties   |
|------------------------|----------------------------|
| `color`                | `margin`                   |
| `font-family`          | `padding`                  |
| `font-size`            | `border`                   |
| `font-weight`          | `width`                    |
| `font-style`           | `height`                   |
| `text-align`           | `display`                  |
| `text-indent`          | `position`                 |
| `line-height`          | `z-index`                  |

---

# CSS Functions

CSS functions are used as a value for various CSS properties.

| Function                      | Description                                                              |
|-------------------------------|--------------------------------------------------------------------------|
| `attr()`                      | Returns the value of an attribute of the selected element                |
| `calc()`                      | Allows you to perform calculations to determine CSS property values      |
| `conic-gradient()`            | Creates a conic gradient                                                 |
| `counter()`                   | Returns the current value of the named counter                           |
| `cubic-bezier()`              | Defines a Cubic Bezier curve                                             |
| `hsl()`                       | Defines colors using the Hue-Saturation-Lightness model (HSL)            |
| `hsla()`                      | Defines colors using the Hue-Saturation-Lightness-Alpha model (HSLA)     |
| `linear-gradient()`           | Creates a linear gradient                                                |
| `max()`                       | Uses the largest value, as the property value |
| `min()`                       | Uses the smallest value, as the property value |
| `radial-gradient()`           | Creates a radial gradient                                                |
| `repeating-conic-gradient()`  | Repeats a conic gradient                                                 |
| `repeating-linear-gradient()` | Repeats a linear gradient                                                |
| `repeating-radial-gradient()` | Repeats a radial gradient                                                |
| `rgb()`                       | Defines colors using the Red-Green-Blue model (RGB)                      |
| `rgba()`                      | Defines colors using the Red-Green-Blue-Alpha model (RGBA)               |
| `var()`                       | Inserts the value of a custom property                                   |

---

# CSS Comments

Comments in CSS can be used to explain code, make notes, or temporarily disable styles.

## Example:

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    /* margin: 0; */
}
```

---
