
## CSS Selectors

A CSS selector selects the HTML element(s) you want to style.

**Types of selectors**:
- Simple Selector
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

# CSS Pseudo-Classes

| Pseudo-Class      | Description                                                              | Example                                                  |
|-------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| `:hover`          | Applies when the user designates an element (with some pointing device), but does not activate it. | ``` <br>button:hover { background-color: yellow; }<br>``` |
| `:active`         | Applies while an element is being activated by the user.                | ```<br>a:active { color: red; }<br>```                 |
| `:first-child`    | Applies to the first child of its parent.                                | ```<br>p:first-child { font-weight: bold; }<br>```     |
| `:last-child`     | Applies to the last child of its parent.                                 | ```<br>p:last-child { color: green; }<br>```           |
| `:root`           | Applies to the root element of a document.                               | ```<br>:root { --main-color: coral; }<br>```           |



