# 1. HTML Lists
HTML lists allows to group a set of related items one by one.

## Unordered List

An unordered list is a list of items where the order of the items does not matter. It is represented by the ul tag.

```html
<ul>
    <li>Apples</li>
    <li>Oranges</li>
    <li>Bananas</li>
</ul>
```
## Ordered List

An ordered list is a list of items where each item is sequentially numbered. It is represented by the ol tag.

```html
<ol>
    <li>Apples</li>
    <li>Oranges</li>
    <li>Bananas</li>
</ol>
```

## Description List
A description list consists of terms and their associated descriptions. It is represented by the dl tag, with dt for terms and dd for descriptions.

```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>
    <dt>CSS</dt>
    <dd>Cascading Style Sheets</dd>
    <dt>JS</dt>
    <dd>JavaScript</dd>
</dl>
```

# 2. HTML Forms

HTML forms are used to collect user input on web pages. They consist of various form elements that allow users to enter data, which is then sent to a server for processing.

### HTML Form Elements

| Element       | Description                                                   | Example Usage                                          |
|---------------|---------------------------------------------------------------|--------------------------------------------------------|
| `<form>`      | Defines a form for user input.                                 | `<form action="/submit-form" method="post"> ... </form>` |
| `<input>`     | Input fields for text, password, email, checkbox, radio, etc. | `<input type="text" id="username" name="username">`     |
| `<textarea>`  | Multiline text input area.                                     | `<textarea id="message" name="message" rows="4"></textarea>` |
| `<label>`     | Labels for form inputs.                                        | `<label for="username">Username:</label>`               |
| `<select>`    | Dropdown list selection.                                       | `<select id="city" name="city"> ... </select>`          |
| `<option>`    | Options for `<select>` element.                                | `<option value="1">Option 1</option>`                   |
| `<button>`    | Button for form submission or other actions.                    | `<button type="submit">Submit</button>`                 |
| `<fieldset>`  | Groups related elements in a form.                              | `<fieldset><legend>Contact Information</legend> ... </fieldset>` |
| `<legend>`    | Caption for `<fieldset>` element.                              | `<fieldset><legend>Contact Information</legend> ... </fieldset>` |
| `<input type="submit">` | Submit button for form submission.                        | `<input type="submit" value="Submit">`                   |

These are some of the commonly used HTML form elements along with their descriptions and example usage. Customize attributes and elements as per your specific form requirements.


#### Example

```html
<form action="/submit-form" method="post">
  <label for="username">Username:</label>
  <input type="text" id="username" name="username" placeholder="Enter your username" required>
  
  <label for="password">Password:</label>
  <input type="password" id="password" name="password" placeholder="Enter your password" required>
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" placeholder="Enter your email" required>
  
  <label for="message">Message:</label>
  <textarea id="message" name="message" rows="4" placeholder="Enter your message"></textarea>
  
  <input type="submit" value="Submit">
</form>
```

### HTML Input Types
Different ways to get user input in a form

| Input Type     | Description                                                   | Example Usage                                          |
|----------------|---------------------------------------------------------------|--------------------------------------------------------|
| `<input type="text">`   | Single-line text input.                                        | `<input type="text" id="username" name="username">`     |
| `<input type="password">`   | Password input field (characters are masked).                  | `<input type="password" id="password" name="password">` |
| `<input type="email">`  | Email address input validation.                                | `<input type="email" id="email" name="email">`          |
| `<input type="number">` | Numeric input field (supports numbers only).                   | `<input type="number" id="quantity" name="quantity">`   |
| `<input type="checkbox">` | Checkbox for selecting multiple options.                       | `<input type="checkbox" id="subscribe" name="subscribe">`|
| `<input type="radio">`    | Radio button for selecting one option from multiple choices.   | `<input type="radio" id="gender-male" name="gender" value="male">` |
| `<input type="file">`     | File upload input field.                                       | `<input type="file" id="avatar" name="avatar">`         |
| `<input type="submit">`   | Submit button for form submission.                             | `<input type="submit" value="Submit">`                  |
| `<input type="reset">`    | Reset button to clear form inputs.                             | `<input type="reset" value="Reset">`                    |
| `<input type="date">`     | Date input field.                                              | `<input type="date" id="birthday" name="birthday">`     |
| `<input type="time">`     | Time input field.                                              | `<input type="time" id="meeting-time" name="meeting-time">` |
| `<input type="color">`    | Color picker input field.                                      | `<input type="color" id="color" name="color">`          |


---

## 3. HTML tables

The `<table>` tag is used to create a table in HTML. It contains the entire table structure including headers, rows, and data cells.

### Table elements:

## `<thead>`

The `<thead>` element defines the header section of a table. It contains one or more `<tr>` (table row) elements.

```html
<thead>
    <tr><th>Header 1</th><th>Header 2</th></tr>
</thead>
```

## `<tbody>`

The `<tbody>` element defines the body section of a table, containing the main content. It includes one or more `<tr>` elements.
```html
<tbody>
    <tr><td>Data 1</td><td>Data 2</td></tr>
</tbody>
```


## `<tfoot>`

The `<tfoot>` element defines the footer section of a table. It contains one or more `<tr>` elements and is usually used for summary or total rows.
```html
<tfoot>
    <tr><td>Footer 1</td><td>Footer 2</td></tr>
</tfoot>
```

## `<tr>`

The `<tr>` element defines a table row. It can be used inside `<thead>`, `<tbody>`, or `<tfoot>`.
```html
<tr>
    <td>Row Data</td><td>Row Data</td>
</tr>
```

## `<th>`

The `<th>` element defines a header cell in a table. It is used within a `<tr>` element and typically resides inside `<thead>` or `<tfoot>`.
```html
<th>Header Cell</th>
```

## `<td>`

The `<td>` element defines a standard data cell in a table. It is used within a `<tr>` element, usually inside `<tbody>`.
```html
<td>Data Cell</td>
```

## `<caption>`

The `<caption>` element provides a title or caption for the table, giving a brief description of the table’s contents.
```html
<caption>Table Title</caption>
```

## `<colgroup>`

The `<colgroup>` element is used to group one or more `<col>` elements, which define the column properties for the table.
```html
<colgroup>
    <col span="2" style="background-color: #f2f2f2;">
</colgroup>
```

## `<col>`

The `<col>` element specifies column properties for each column within a `<colgroup>`. It is used to apply styles or attributes to entire columns.
```html
<col span="2" style="background-color: #f2f2f2;">
```

## Attributes
```html
<thead>
    <tr><th>Header 1</th><th>Header 2</th></tr>
</thead>
```

### `colspan`

The `colspan` attribute allows a `<td>` or `<th>` element to span multiple columns.
```html
<td colspan="2">Spanning Columns</td>
```

### `rowspan`

The `rowspan` attribute allows a `<td>` or `<th>` element to span multiple rows.
```html
<td rowspan="2">Spanning Rows</td>

```

---

## 4. HTML Comments

HTML comments are used to insert notes or explanations in the code that are not visible to users. Comments help developers understand and maintain the code.

### Syntax

```html
<!-- This is a comment -->
```
---

## 5. Accessibility:
Accessibility in HTML involves using semantic HTML, ARIA (Accessible Rich Internet Applications) attributes, and best practices to improve the accessibility of web page

- Semantic HTML uses elements that provide meaning and context to the content, making it more accessible and easier to understand.
  
- ARIA attributes provide additional information to assistive technologies, enhancing the accessibility of dynamic content and complex UI components.

  # Common ARIA Attributes

| Attribute Name    | Description                                                                       |
|-------------------|-----------------------------------------------------------------------------------|
| `aria-label`      | Provides an accessible name for an element.                                       |
| `aria-hidden`     | Indicates whether an element is visible or hidden.                                |
| `aria-disabled`   | Indicates that an element is perceivable but disabled.                            |
| `aria-expanded`   | Indicates whether an element is expanded or collapsed.                            |
| `aria-haspopup`   | Indicates the availability and type of interactive popup element.                 |
| `aria-invalid`    | Indicates the entered value does not conform to the expected format.              |
| `aria-orientation`| Indicates whether the element's orientation is horizontal, vertical, or undefined.|
| `aria-readonly`   | Indicates that the element is not editable, but is otherwise operable.            |
| `aria-required`   | Indicates that user input is required before submission.                          |
| `aria-selected`   | Indicates the current "selected" state of various widgets.                        |

Example

    <header aria-label="Main Header"><h1>Title</h1></header>

---

## 5. SEO

SEO stands for “search engine optimization.” 
In simple terms, SEO means the process of improving your website to increase its visibility in Google, Microsoft Bing, and other search engines.

HTML plays a critical role in SEO as it helps search engines understand and rank the content of a webpage. 

## 1. Title Tag

The title tag defines the title of the webpage, which appears in the browser tab and is used by search engines as the primary indicator of the page’s content.

  ```html
  <title>Page Title</title>
  ```

## 2. Meta Description
It defines the metadata about an HTML document.

  ```html
<meta name="description" content="Brief description of the page content.">
  ```

## 3. Header Tags

Header tags structure the content and indicate its hierarchy, making it easier for search engines to understand the page.

  ```html
<H1> Heading </H1>
  ```

## 4. Alt text for Images

Alt attributes describe images to search engines and visually impaired users, improving accessibility and SEO.

  ```html
<img src="image.jpg" alt="Description of the image">
  ```

  ## 5. URL Structure

Clean and descriptive URLs help search engines and users understand the page content.

  ```html
https://www.example.com/seo-tips
  ```

  ## 6. Schema Markup
Helps search engines understand the context of your content, which can enhance search results with rich snippets.

  ```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "Example Article",
  "datePublished": "2024-07-11",
  "author": {
    "@type": "Person",
    "name": "Author Name"
  }
}
</script>
  ```
---

## 6.  HTML APIS

##  1. Geolocation API:

Retrieve the geographic location of a user.

  ```html
if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(function(position) {
        console.log("Latitude: " + position.coords.latitude);
        console.log("Longitude: " + position.coords.longitude);
    });
} 
  ```

## 2. Drag and Drop API

Enable drag-and-drop functionality for elements.

  ```html
<div id="drag1" draggable="true" ondragstart="drag(event)">Drag me</div>
<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>

<script>
function allowDrop(ev) {
    ev.preventDefault();
}

function drag(ev) {
    ev.dataTransfer.setData("text", ev.target.id);
}

function drop(ev) {
    ev.preventDefault();
    var data = ev.dataTransfer.getData("text");
    ev.target.appendChild(document.getElementById(data));
}
</script>
  ```

## 3. Fetch API

 Make HTTP requests to fetch resources.

  ```html
fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

## 4. Web Storage API

Store data locally in the browser

  ```html
localStorage.setItem("username", "JohnDoe");
var user = localStorage.getItem("username");
console.log(user);

```
---
