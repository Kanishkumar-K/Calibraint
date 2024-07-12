
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
    The selector .class is used to select the elements that belong to the specific class attribute.

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

![WhatsApp Image 2024-07-12 at 11 26 47_6ef27db7](https://github.com/user-attachments/assets/841416cf-02a3-42b4-9b3c-6a0e362018ca)

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







