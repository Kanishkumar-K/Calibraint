# 1. HTML

### (Hypertext Markup Language)

HTML is the standard markup language used to create and structure web pages on the World Wide Web. 
It consists of a set of elements, tags, and attributes that define the structure, content, and layout of web documents.

---
## XHTML

XHTML stands for EXtensible HyperText Markup Language
XHTML is a stricter, more XML-based version of HTML.
An XHTML document must have an XHTML <!DOCTYPE> declaration.

It uses Document Type Definitions (DTDs) to define the structure and rules for the markup. XHTML supports three types of DTDs:

1. Strict DTD: This does not allow deprecated elements and attributes.
2. Transitional DTD: This allows deprecated elements and attributes.
3. Frameset DTD: This is used for documents containing frames.

---
## Elements, Tags, Attributes and Layout

####Elements
HTML elements are building blocks of web pages defined by tags, which enclose content and define its purpose.

#### Elements and Tags

- `<p>`: Defines a paragraph.
- `<h1>` to `<h6>`: Define headings of different levels.
- `<a>`: Creates hyperlinks.
- `<img>`: Embeds images.
- `<div>`: Defines a generic container.

#### Attributes

Attributes provide additional information about an element and are defined within the opening tag.
- `href` (in `<a>`): Specifies the URL of the link.
- `src` (in `<img>`): Specifies the source of the image.
- `class` and `id`: Attributes used for styling and JavaScript targeting.
- `alt` (in `<img>`): Specifies alternative text for images.

## HTML Layout Elements

- `<header>` - Defines a header for a document or a section.
- `<nav>` - Defines a set of navigation links.
- `<section>` - Defines a section in a document.
- `<article>` - Defines an independent, self-contained content.
- `<aside>` - Defines content aside from the content (like a sidebar).
- `<footer>` - Defines a footer for a document or a section.
- `<details>` - Defines additional details that the user can open and close on demand.
- `<summary>` - Defines a heading for the `<details>` element.

---
### HTML Layout Techniques

- **CSS Framework**: Uses frameworks like Bootstrap, providing pre-styled components and grids for responsive web design.

    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    ```
    
- **CSS Float Property**: Positions elements by floating them left or right within a container, often requiring clearfix techniques to manage layout.

    ```html
    <div style="float: left; width: 33.33%;"></div>
    ```

- **CSS Flexbox**: Offers a flexible layout model for containers and items, simplifying complex layouts and alignments with `display: flex`.

    ```html
    <div style="display: flex; justify-content: space-between;"></div>
    ```

- **CSS Grid**: Provides a two-dimensional layout system with rows and columns, allowing precise control over element positioning within a grid container.

    ```html
    <div style="display: grid; grid-template-columns: 1fr 1fr;"></div>
    ```
---
## Class and Id

#### Classes
Classes are used to apply styles or identify groups of elements.

`<div class="container">`: Defines a container with specific styling.

#### Id
IDs uniquely identify elements within the document.

`<div id="header">`: Identifies the header section of the page.
 
---
## Semantic, Non Semantic elements
#### Semantic Elements

Semantic elements are meaningful and convey structure and importance to browsers and developers:

- `<header>`: Represents introductory content typically at the beginning of a section or page.
- `<nav>`: Represents a section of navigation links.
- `<section>`: Represents grouping of content.
- `<footer>`: Represents footer information typically at the end of a section or page.

#### Non-Semantic Elements
Non-semantic elements do not convey meaning and are used for layout and styling:

- `<div>`: Represents a generic container or division.
- `<span>`: Represents a generic inline container, often used for styling.
---

## Formatting elements
Formatting elements were designed to display special types of text

| HTML Tag | Description                     |
|----------|---------------------------------|
| `<strong>` | Renders text in **bold**.       |
| `<em>`    | Renders text in *italics*.      |
| `<u>`     | Renders text with an underline. |
| `<mark>`  | Highlights text.                |
| `<del>`   | Renders text with a strikethrough. |
| `<ins>`   | Renders text as inserted.       |
| `<sub>`   | Renders text as subscript.      |
| `<sup>`   | Renders text as superscript.    |

---
### Character Sets in HTML

Character sets define the collection of characters that can be used in an HTML document. They are specified using the `<meta>` tag within the `<head>` section.


 **UTF-8**: Supports almost all characters across various languages and symbols worldwide.

    <meta charset="UTF-8">
    
---

## Document Object Model (DOM)

The DOM (Document Object Model) is an interface that represents the entire document as a tree of nodes, allowing manipulation of the document's structure, content, and style.

## DOM Representation

- **Window object**: Automatically created in the browser window.
- **Document object**: Represents the HTML document loaded in the browser.
- **Form / Link / Anchor objects**: Represent specific elements in the document.
- **Form control elements**: Represent interactive controls like input fields.

## HTML DOM Methods

### Finding Elements

1. **document.getElementById(id)**:
   Returns the element with the specified ID attribute.

   ```javascript
   var element = document.getElementById('myElementId');

2. document.getElementsByTagName():
   Returns a live HTMLCollection of elements with the specified tag name.

     ```javascript
    var elements = document.getElementsByTagName('div');

3. document.querySelectorAll():
   Returns a static NodeList of all elements that match a specified CSS selector.
   
     ```javascript
   var elements = document.querySelectorAll('div.container');
     
4. document.querySelector():
  Returns the first element that matches a specified CSS selector.

     ```javascript
   var element = document.querySelector('div#main');

### Changing html elements:

5. element.textContent():
 Retrieves or sets the text content of the specified element 
```javascript
var element = document.getElementById('myElement');
var textContent = element.textContent;  // Retrieves text content
element.textContent = 'New text content';  // Sets text content
```

6. element.innerHTML():
 Retrieves or sets the HTML content inside the element
```javascript
var element = document.getElementById('myElement');
var htmlContent = element.innerHTML;  // Retrieves HTML content
element.innerHTML = '<p>New HTML content</p>';  // Sets HTML content
```

8. element.style.property():
Retrieves or sets the value of a specific style property for the element
```javascript
var element = document.getElementById('myElement');
element.style.color = 'blue';  // Sets color style property
var color = element.style.color;  // Retrieves color style property
```

9. element.setAttribute(id, value):
Sets the value of an attribute on the element.
```javascript
var element = document.getElementById('myElement');
element.setAttribute('class', 'newClass');  // Sets class attribute
```

10. element.getAttribute(id):
 Retrieve the value of an attribute on the element.
```javascript
var element = document.getElementById('myElement');
var className = element.getAttribute('class');  // Retrieves class attribute value
```
---
### Element creation and manipulation:

10. document.createElement(value)
Create an html element
```javascript
var newDiv = document.createElement('div');  // Create a new <div> element
```

11. document.deleteChildt(value)
Deletes a html element
```javascript
var parent = document.getElementById('parentElement');
var child = document.getElementById('childElement');
parent.removeChild(child);
```

12. document.appendChild(value)
Append a html element
```javascript
var parent = document.getElementById('parentElement');
var newChild = document.createElement('div');
parent.appendChild(newChild);
```

13. document.replaceChild(new, old)
Replace a html element

---

## DOM Navigation and Events

## Nodes Navigation

- **parentNode**: Accesses the parent node of an element.
- **childNodes[number]**: Provides a collection of child nodes of a specific element, accessible by index.
- **firstChild**: Retrieves the first child node of an element.
- **lastChild**: Retrieves the last child node of an element.
- **nextSibling**: Retrieves the next sibling node, which is the next node at the same hierarchical level in the DOM.
- **previousSibling**: Retrieves the previous sibling node, which is the node immediately preceding the specified node in the DOM hierarchy.

### NodeList

A NodeList represents a list of nodes in an HTML document.

- **length**: Property that returns the number of nodes in the NodeList.

## DOM Events

### Mouse Events

- **click**: Occurs when the user clicks on an element.
- **mouseover**: Occurs when the mouse pointer enters the element.
- **mouseout**: Occurs when the mouse pointer leaves the element.
- **mousemove**: Occurs when the mouse pointer is moving while over an element.
- **mousedown**: Occurs when the mouse button is pressed down on an element.
- **mouseup**: Occurs when the mouse button is released over an element.

### Form Events

- **submit**: Occurs when a form is submitted.
- **reset**: Occurs when a form is reset.

---
# Event Bubbling, Event Delegation, Propagation, and Preventing Default

## Event Bubbling

Event bubbling is the phenomenon where an event triggered on a nested element "bubbles" up through its ancestors in the DOM tree.

### `event.stopPropagation()`

Prevents further propagation of the current event in the capturing and bubbling phases.

```javascript
document.getElementById('nestedElement').addEventListener('click', function(event) {
    event.stopPropagation();
    console.log('Click event stopped bubbling at nestedElement.');
});
```
## Event Delegation

Event delegation is a technique where a single event listener is attached to a parent element to manage events for multiple child elements that may be dynamically added or removed.

```javascript
document.getElementById('parentElement').addEventListener('click', function(event) {
    if (event.target.classList.contains('childElement')) {
        console.log('Child element clicked:', event.target.textContent);
    }
});
```
## Event Propagation

Event propagation refers to the flow of events through the DOM tree. Events can propagate in two phases: capturing phase and bubbling phase.

```javascript
document.getElementById('parentElement').addEventListener('click', function(event) {
    console.log('Event captured and bubbling:', event.target.nodeName);
}, true); // true for capturing phase
```

## Preventdefault():
The event.preventDefault() method stops the default action of an element from happening.

```javascript
document.getElementById('linkElement').addEventListener('click', function(event) {
    event.preventDefault();
    console.log('Link click default action prevented.');
});




