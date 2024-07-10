# HTML Lists
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

# HTML Forms

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

## HTML tables

The `<table>` tag is used to create a table in HTML. It contains the entire table structure including headers, rows, and data cells.




