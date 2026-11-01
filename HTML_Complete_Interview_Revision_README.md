# HTML Course Notes --- Complete Revision Guide

A structured revision guide based on the HTML topics covered in the
course notes. It explains the elements, attributes, examples, and
important interview distinctions.

> **Scope:** This guide covers the topics present in the supplied course
> notes: document structure, headings, paragraphs, images, links,
> tables, lists, forms, input types, form attributes, select and
> datalist, textareas, iframes, audio, video, `div`, `span`, and
> text-formatting elements. A few clarifications are included where the
> original notes could lead to a misunderstanding.

------------------------------------------------------------------------

## Table of Contents

1.  [What Is HTML?](#1-what-is-html)
2.  [Basic HTML Document Structure](#2-basic-html-document-structure)
3.  [Headings, Paragraphs, Line Breaks, and Horizontal
    Rules](#3-headings-paragraphs-line-breaks-and-horizontal-rules)
4.  [Images](#4-images)
5.  [Links](#5-links)
6.  [Tables](#6-tables)
7.  [Lists](#7-lists)
8.  [Forms: Fundamentals](#8-forms-fundamentals)
9.  [Form Controls and Input Types](#9-form-controls-and-input-types)
10. [Important Input Attributes](#10-important-input-attributes)
11. [Select, Option, Optgroup, and
    Datalist](#11-select-option-optgroup-and-datalist)
12. [Textarea](#12-textarea)
13. [Iframes](#13-iframes)
14. [Audio and Video](#14-audio-and-video)
15. [Div and Span](#15-div-and-span)
16. [Text Formatting Elements](#16-text-formatting-elements)
17. [Important Differences to
    Remember](#17-important-differences-to-remember)
18. [Common Mistakes and
    Corrections](#18-common-mistakes-and-corrections)
19. [Interview Questions](#19-interview-questions)
20. [Practical Revision Tasks](#20-practical-revision-tasks)
21. [Quick Reference](#21-quick-reference)

------------------------------------------------------------------------

## 1. What Is HTML?

**HTML** stands for **HyperText Markup Language**. It is the standard
markup language used to structure content on web pages.

HTML describes the structure and meaning of content using elements
(often called tags).

HTML is **not a programming language** in the usual sense: it does not
provide general-purpose programming logic such as loops, conditions, or
calculations. It works alongside technologies such as:

-   **HTML:** Structure and content.
-   **CSS:** Presentation and layout.
-   **JavaScript:** Behavior and interactivity.

### Element anatomy

``` html
<p>This is a paragraph.</p>
```

-   `<p>` is the opening tag.
-   `This is a paragraph.` is the content.
-   `</p>` is the closing tag.
-   The opening tag, content, and closing tag together form an element.

An element can also have attributes:

``` html
<a href="https://example.com">Visit Example</a>
```

Here, `href` is an attribute and its value is `https://example.com`.

### Attributes

Attributes provide additional information or configure an element. They
are generally written in the opening tag:

``` html
<tag attribute="value">Content</tag>
```

Use lowercase tag and attribute names as a consistent convention.

------------------------------------------------------------------------

## 2. Basic HTML Document Structure

``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Page</title>
</head>
<body>
    <h1>Hello World</h1>
    <p>This is my first webpage.</p>
</body>
</html>
```

### Explanation

  -----------------------------------------------------------------------
  Part                                Purpose
  ----------------------------------- -----------------------------------
  `<!DOCTYPE html>`                   Declares an HTML5 document and
                                      enables standards-mode rendering.

  `<html>`                            Root element containing the
                                      document.

  `lang="en"`                         Identifies the primary language of
                                      the page.

  `<head>`                            Contains document metadata and
                                      linked resources.

  `<meta charset="UTF-8">`            Declares character encoding.

  `<meta name="viewport">`            Helps the page use the device's
                                      viewport correctly on mobile
                                      devices.

  `<title>`                           Sets the page title shown in the
                                      browser tab.

  `<body>`                            Contains the page content.
  -----------------------------------------------------------------------

### Head vs. Body

  -----------------------------------------------------------------------
  `<head>`                            `<body>`
  ----------------------------------- -----------------------------------
  Contains metadata and resource      Contains the document's content.
  references.                         

  Usually not displayed as page       Contains content displayed in the
  content.                            page.

  Includes title, meta, and link      Includes headings, paragraphs,
  elements.                           images, forms, and more.
  -----------------------------------------------------------------------

### What does DOCTYPE do?

`<!DOCTYPE html>` tells the browser to interpret the document as modern
HTML and use standards mode. It is a declaration, not an ordinary HTML
element.

### Is HTML case-sensitive?

HTML tag and attribute names are generally case-insensitive, but
lowercase is the standard convention.

------------------------------------------------------------------------

## 3. Headings, Paragraphs, Line Breaks, and Horizontal Rules

### Headings

HTML provides six heading levels:

``` html
<h1>Main Heading</h1>
<h2>Section Heading</h2>
<h3>Subsection Heading</h3>
<h4>Heading Level 4</h4>
<h5>Heading Level 5</h5>
<h6>Heading Level 6</h6>
```

-   `<h1>` represents the highest-level heading.
-   `<h6>` represents the lowest-level heading.
-   Headings communicate the structure and hierarchy of the content.
-   Do not choose a heading level only because of its default font size;
    use CSS for visual sizing.

### Paragraphs

``` html
<p>This is the first paragraph.</p>
<p>This is another paragraph.</p>
```

Each `<p>` element represents a paragraph.

### Line break: `<br>`

``` html
<p>First line<br>Second line</p>
```

`<br>` inserts a line break within text. It is a void element and does
not need a closing tag.

### Horizontal rule: `<hr>`

``` html
<p>First topic</p>
<hr>
<p>Next topic</p>
```

`<hr>` represents a thematic break between sections of content. Browsers
commonly display it as a horizontal line.

------------------------------------------------------------------------

## 4. Images

The `<img>` element embeds an image in the page.

``` html
<img src="./images/cat.jpg" alt="A cat sitting on a chair" width="350" height="350">
```

### Important attributes

  -----------------------------------------------------------------------
  Attribute                           Purpose
  ----------------------------------- -----------------------------------
  `src`                               Specifies the image location.

  `alt`                               Provides alternative text for
                                      accessibility and when the image
                                      cannot be displayed.

  `width`                             Specifies the displayed width.

  `height`                            Specifies the displayed height.
  -----------------------------------------------------------------------

### Relative and absolute paths

**Relative path:**

``` html
<img src="./image1.jpg" alt="Wild cat">
<img src="./images/cat.jpg" alt="Cat">
```

A relative path is resolved from the current document's location.

Common path notation:

-   `image.jpg`: File in the current directory.
-   `./image.jpg`: Explicitly refers to the current directory.
-   `images/image.jpg`: File inside an `images` subdirectory.
-   `../image.jpg`: File in the parent directory.

**Absolute URL:**

``` html
<img src="https://example.com/images/cat.jpg" alt="Cat">
```

This uses a complete web URL.

### Why is `alt` important?

1.  Screen readers can use it to describe meaningful images.
2.  It can be displayed when an image fails to load.
3.  It provides a text alternative for the image.

For a purely decorative image, use an empty alt attribute (`alt=""`) so
assistive technology can ignore it.

### Is `<img>` a container element?

No. `<img>` is a **void element**: it does not wrap content and has no
closing tag.

Other common void elements include:

-   `<br>`
-   `<hr>`
-   `<input>`
-   `<meta>`
-   `<link>`

------------------------------------------------------------------------

## 5. Links

The `<a>` (anchor) element creates a hyperlink.

``` html
<a href="about.html">About Page</a>
```

### Important attributes

  Attribute   Purpose
  ----------- ----------------------------------------------
  `href`      Specifies the destination.
  `target`    Specifies where the linked resource opens.
  `title`     Can provide additional advisory information.

### `target` values

``` html
<a href="about.html" target="_self">Open in this tab</a>
<a href="https://example.com" target="_blank">Open in a new tab</a>
```

-   `_self`: Opens in the current browsing context; this is the default.
-   `_blank`: Opens in a new browsing context, usually a new tab.

For external links opened with `_blank`, consider:

``` html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">
    Visit Example
</a>
```

### Common link types

**1. Internal page link**

``` html
<a href="about.html">About</a>
```

**2. External website link**

``` html
<a href="https://github.com">GitHub</a>
```

**3. Email link**

``` html
<a href="mailto:someone@example.com">Send an email</a>
```

**4. Telephone link**

``` html
<a href="tel:+201234567890">Call us</a>
```

**5. WhatsApp link**

``` html
<a href="https://wa.me/201234567890">Chat on WhatsApp</a>
```

Use the international phone number without `+`, spaces, or the local
leading zero in the WhatsApp URL.

**6. Link to a section on the same page**

``` html
<a href="#contact">Go to Contact</a>

<section id="contact">
    <h2>Contact Us</h2>
</section>
```

The `href` fragment matches the destination element's `id`.

### Can an image be clickable?

Yes. Put the image inside an anchor:

``` html
<a href="https://github.com">
    <img src="github.png" alt="Visit GitHub">
</a>
```

### `href` vs. `src`

-   `href` identifies a hyperlink destination or a related resource.
-   `src` specifies the location of an embedded resource, such as an
    image or media file.

------------------------------------------------------------------------

## 6. Tables

Tables represent data arranged in rows and columns.

### Basic table structure

``` html
<table border="1">
    <caption>Students Information</caption>

    <thead>
        <tr>
            <th>Name</th>
            <th>Age</th>
            <th>Department</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>Malak</td>
            <td>20</td>
            <td>Computer Engineering</td>
        </tr>
        <tr>
            <td>Omar</td>
            <td>21</td>
            <td>Electrical Engineering</td>
        </tr>
    </tbody>

    <tfoot>
        <tr>
            <td colspan="3">Total: 2 students</td>
        </tr>
    </tfoot>
</table>
```

### Table elements

  Element       Meaning
  ------------- ------------------------------------
  `<table>`     Creates the table.
  `<caption>`   Provides a table title or caption.
  `<thead>`     Groups header rows.
  `<tbody>`     Groups the main data rows.
  `<tfoot>`     Groups footer rows.
  `<tr>`        Creates a table row.
  `<th>`        Creates a header cell.
  `<td>`        Creates a regular data cell.

### `th` vs. `td`

-   `<th>` represents a header cell and is commonly bold and centered by
    default.
-   `<td>` represents a regular data cell.

### `rowspan`

`rowspan` makes a cell span multiple rows (vertically).

``` html
<table border="1">
    <tr>
        <th>Name</th>
        <th>Color</th>
    </tr>
    <tr>
        <td rowspan="2">Malak</td>
        <td>Blue</td>
    </tr>
    <tr>
        <td>Red</td>
    </tr>
</table>
```

The `Malak` cell occupies two rows. Therefore, the second data row does
not need another cell for the name column.

### `colspan`

`colspan` makes a cell span multiple columns (horizontally).

``` html
<table border="1">
    <tr>
        <td colspan="2">Personal Information</td>
    </tr>
    <tr>
        <td>Name</td>
        <td>Malak</td>
    </tr>
</table>
```

### `rowspan` vs. `colspan`

  `rowspan`              `colspan`
  ---------------------- -------------------------
  Spans multiple rows.   Spans multiple columns.
  Vertical merging.      Horizontal merging.

### Table styling note

The `border` attribute appears in older/simple examples, but modern
styling should be done with CSS.

``` html
<table>
    ...
</table>
```

``` css
table, th, td {
    border: 1px solid black;
    border-collapse: collapse;
}
```

------------------------------------------------------------------------

## 7. Lists

HTML has three main list types.

### 7.1 Ordered list: `<ol>`

An ordered list is used when the sequence or numbering matters.

``` html
<ol>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ol>
```

`<li>` represents a list item.

#### The `type` attribute

  Value   Numbering
  ------- ------------
  `1`     1, 2, 3
  `A`     A, B, C
  `a`     a, b, c
  `I`     I, II, III
  `i`     i, ii, iii

Example:

``` html
<ol type="I">
    <li>Red</li>
    <li>Green</li>
    <li>Yellow</li>
</ol>
```

#### The `start` attribute

``` html
<ol start="3">
    <li>Red</li>
    <li>Green</li>
    <li>Yellow</li>
</ol>
```

The list begins at 3.

The `start` value is numeric even when the list uses letters or Roman
numerals:

``` html
<ol type="a" start="27">
    <li>Item</li>
    <li>Item</li>
</ol>
```

### 7.2 Unordered list: `<ul>`

An unordered list is used when the order is not important.

``` html
<ul>
    <li>Red</li>
    <li>Green</li>
    <li>Blue</li>
</ul>
```

Common bullet styles include:

-   `disc`
-   `circle`
-   `square`

The older `type` attribute can be found in basic examples, but CSS is
preferred:

``` css
ul {
    list-style-type: square;
}
```

### 7.3 Description list: `<dl>`

A description list contains terms and their descriptions.

``` html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>

    <dt>CSS</dt>
    <dd>Cascading Style Sheets</dd>
</dl>
```

-   `<dl>`: Description list.
-   `<dt>`: Description term.
-   `<dd>`: Description/details for a term.

### 7.4 Nested lists

Lists can be nested inside list items.

``` html
<ul>
    <li>Frontend
        <ol>
            <li>HTML</li>
            <li>CSS</li>
        </ol>
    </li>
    <li>Backend</li>
</ul>
```

### Ordered vs. unordered lists

-   Use `<ol>` when sequence matters.
-   Use `<ul>` when sequence does not matter.
-   Use `<dl>` for terms and their descriptions.

------------------------------------------------------------------------

## 8. Forms: Fundamentals

Forms collect information from users and submit it for processing.

### Basic form

``` html
<form action="register.php" method="post">
    <label for="username">Username:</label>
    <input type="text" id="username" name="user">

    <input type="submit" value="Register">
</form>
```

### Form attributes

  Attribute        Purpose
  ---------------- ------------------------------------------------
  `action`         Specifies where the form data is submitted.
  `method`         Specifies the HTTP method used for submission.
  `target`         Specifies where the response is displayed.
  `autocomplete`   Controls browser autofill behavior.
  `enctype`        Specifies how the form data is encoded.

### GET vs. POST

**GET**

``` html
<form action="about.html" method="get">
    <input type="text" name="user">
    <input type="submit" value="Send">
</form>
```

If the user enters `Malak`, the resulting URL may look like:

``` text
about.html?user=Malak
```

GET characteristics:

-   Form data is commonly appended to the URL as query parameters.
-   Suitable for retrieving data.
-   The URL can be bookmarked or shared.
-   URLs have practical length limits.

**POST**

``` html
<form action="register.php" method="post">
    <input type="text" name="user">
    <input type="submit" value="Register">
</form>
```

POST characteristics:

-   Form data is sent in the request body.
-   Commonly used when submitting data or requesting a change.
-   Data is not normally displayed in the URL.
-   Can carry larger request bodies.

**Important security clarification:** POST does not encrypt data. HTTPS
provides encryption in transit. Sensitive data should not be placed in a
GET URL.

### Label

A label describes a form control.

``` html
<label for="email">Email:</label>
<input type="email" id="email" name="mail">
```

The label's `for` value must match the input's `id`.

Clicking the label can focus or activate its associated control.

### Placeholder

``` html
<input type="text" name="user" placeholder="Enter your name">
```

A placeholder is a temporary hint displayed inside an empty control. It
is not a replacement for a proper label.

### Fieldset and Legend

``` html
<fieldset>
    <legend>Personal Information</legend>

    <label for="name">Name:</label>
    <input type="text" id="name" name="user">
</fieldset>
```

-   `<fieldset>` groups related form controls.
-   `<legend>` gives the group a caption.

### `id` vs. `name`

  -----------------------------------------------------------------------
  `id`                                `name`
  ----------------------------------- -----------------------------------
  Identifies an element in the        Identifies a form field in
  document.                           submitted data.

  Used by labels, CSS, and            Used when the browser constructs
  JavaScript.                         form data.

  Should be unique in the document.   Can be shared by related controls,
                                      such as radio buttons.
  -----------------------------------------------------------------------

A form control generally needs a `name` to be included in submitted form
data.

------------------------------------------------------------------------

## 9. Form Controls and Input Types

The `<input>` element creates different controls depending on its
`type`.

### 9.1 Text input

``` html
<input type="text" name="username">
```

Accepts ordinary single-line text.

### 9.2 Email input

``` html
<input type="email" name="email">
```

Accepts an email-like value and provides browser validation.

### 9.3 Password input

``` html
<input type="password" name="password">
```

Masks the characters displayed on screen. It does not itself encrypt the
password.

### 9.4 Radio buttons

Radio buttons let a user choose one option from a group.

``` html
<input type="radio" name="gender" id="male" value="Male">
<label for="male">Male</label>

<input type="radio" name="gender" id="female" value="Female">
<label for="female">Female</label>
```

Important points:

-   Radio buttons with the same `name` belong to the same group.
-   Only one option in that group can be selected at a time.
-   `value` is the value submitted if the radio button is selected.
-   `checked` selects an option by default.

### 9.5 Checkboxes

Checkboxes allow users to select multiple options.

``` html
<input type="checkbox" name="sport" id="boxing" value="Boxing">
<label for="boxing">Boxing</label>

<input type="checkbox" name="sport" id="football" value="Football">
<label for="football">Football</label>

<input type="checkbox" name="sport" id="tennis" value="Tennis">
<label for="tennis">Tennis</label>
```

Multiple checked checkboxes can submit multiple values with the same
field name.

### Radio vs. Checkbox

  -----------------------------------------------------------------------
  Radio                               Checkbox
  ----------------------------------- -----------------------------------
  One selection per same-name group.  Multiple selections are possible.

  Used for mutually exclusive         Used for independent choices.
  choices.                            

  Usually displayed as a circle.      Usually displayed as a square.
  -----------------------------------------------------------------------

### 9.6 File input

``` html
<input type="file" name="cv">
```

Allows the user to choose a file.

To allow multiple files:

``` html
<input type="file" name="cv" multiple>
```

For a typical file-upload form:

``` html
<form action="upload.php" method="post" enctype="multipart/form-data">
    <label for="cv">Upload your CV:</label>
    <input type="file" id="cv" name="cv" multiple>
    <input type="submit" value="Upload">
</form>
```

`multiple` permits selecting more than one file. `multipart/form-data`
is the usual encoding for file uploads.

### 9.7 Date and time inputs

``` html
<input type="date" name="birthday">
<input type="month" name="month">
<input type="week" name="week">
<input type="datetime-local" name="appointment">
```

  Type               Purpose
  ------------------ --------------------------------
  `date`             Selects a date.
  `month`            Selects a month and year.
  `week`             Selects a week and year.
  `datetime-local`   Selects a local date and time.

The old `datetime` input type is obsolete. Use `datetime-local` when a
local date and time are needed.

### 9.8 Number input

``` html
<input type="number" name="quantity" min="3" max="21" step="3">
```

-   `min`: Minimum permitted value.
-   `max`: Maximum permitted value.
-   `step`: Permitted increments.

For the example above, values such as 3, 6, 9, 12, 15, 18, and 21
satisfy the range and step constraints.

### 9.9 Range input

``` html
<input type="range" name="price" min="0" max="500" step="10">
```

Displays a slider for selecting a value in a range.

If `min` and `max` are omitted, the usual defaults are 0 and 100. The
default value is generally the midpoint when no value is specified.

### 9.10 Color input

``` html
<input type="color" name="color">
```

Allows the user to choose a color.

### 9.11 Hidden input

``` html
<input type="hidden" name="user_id" value="5">
```

Stores a form value that is not shown as an ordinary visible control.

**Security warning:** A hidden input is not secure. Users can inspect
and modify its value using browser developer tools. Never trust hidden
input values for authorization or sensitive decisions.

### 9.12 Submit input

``` html
<input type="submit" value="Create Account">
```

Submits the form.

### 9.13 Reset input

``` html
<input type="reset" value="Clear">
```

Resets form controls to their initial values.

------------------------------------------------------------------------

## 10. Important Input Attributes

### Attribute reference

  Attribute        Meaning
  ---------------- ---------------------------------------------------------
  `name`           Name used when submitting the control's value.
  `id`             Identifies the element in the document.
  `value`          Initial or submitted value, depending on the control.
  `placeholder`    Displays a temporary hint.
  `required`       Requires a value before normal form submission.
  `checked`        Initially checks a radio button or checkbox.
  `selected`       Initially selects an option in a dropdown.
  `disabled`       Disables the control.
  `readonly`       Prevents editing while keeping the control submittable.
  `autofocus`      Requests focus when the page loads.
  `autocomplete`   Controls browser autofill behavior.
  `minlength`      Minimum text length.
  `maxlength`      Maximum text length.
  `min`            Minimum permitted numeric/date value.
  `max`            Maximum permitted numeric/date value.
  `step`           Permitted numeric increments.
  `multiple`       Allows multiple values/files where supported.

### `disabled` vs. `readonly`

``` html
<input type="text" name="disabledField" value="Malak" disabled>
<input type="text" name="readonlyField" value="Malak" readonly>
```

  -----------------------------------------------------------------------
  Disabled                            Readonly
  ----------------------------------- -----------------------------------
  User cannot interact with the       User can focus and select its value
  control normally.                   but cannot edit it.

  Not submitted with the form.        Submitted with the form if it has a
                                      name.

  Generally removed from normal       Can receive focus.
  keyboard focus.                     
  -----------------------------------------------------------------------

### `checked` vs. `selected`

-   `checked` is used with radio buttons and checkboxes.
-   `selected` is used with `<option>` elements inside a `<select>`.

### `value` vs. `placeholder`

``` html
<input type="text" value="Malak">
<input type="text" placeholder="Enter your name">
```

-   `value` sets the actual initial value.
-   `placeholder` displays a hint when the control is empty.

### `required` vs. `minlength`

``` html
<input type="text" name="username" required minlength="3">
```

-   `required`: The user must provide a value.
-   `minlength`: The entered text must meet a minimum length.

### `autofocus`

``` html
<input type="text" name="username" autofocus>
```

Requests that the browser focus this control when the page loads. Use it
carefully, especially on pages with multiple interactive elements.

### `autocomplete`

``` html
<input type="email" name="email" autocomplete="off">
```

Controls whether the browser may offer autocomplete suggestions. Browser
behavior can vary.

------------------------------------------------------------------------

## 11. Select, Option, Optgroup, and Datalist

### 11.1 Select and Option

`<select>` creates a dropdown list. `<option>` defines each choice.

``` html
<label for="country">Country:</label>

<select name="country" id="country">
    <option value="EG">Egypt</option>
    <option value="SD">Sudan</option>
    <option value="MA">Morocco</option>
    <option value="PS" selected>Palestine</option>
    <option value="SA">Saudi Arabia</option>
</select>
```

Important attributes:

-   `name`: Identifies the dropdown field in submitted data.
-   `id`: Identifies the element and can connect it to a label.
-   `value` on an option: Defines the value submitted for that option.
-   `selected`: Makes an option selected by default.

If an option has no explicit `value`, its text content is generally used
as its submitted value.

### 11.2 Optgroup

`<optgroup>` groups related options inside a dropdown.

``` html
<select name="country">
    <optgroup label="African Countries">
        <option value="EG">Egypt</option>
        <option value="SD">Sudan</option>
        <option value="MA">Morocco</option>
    </optgroup>

    <optgroup label="Asian Countries">
        <option value="PS">Palestine</option>
        <option value="SA">Saudi Arabia</option>
    </optgroup>
</select>
```

The `label` attribute gives the group its visible label.

### 11.3 Datalist

`<datalist>` provides suggestions for an input. Unlike a normal select
dropdown, the user can generally enter a value that is not in the
suggestions.

``` html
<label for="favcolor">Choose a color:</label>

<input type="text" id="favcolor" name="favcolor" list="colors">

<datalist id="colors">
    <option value="Red">
    <option value="Blue">
    <option value="Yellow">
    <option value="Gold">
    <option value="Silver">
</datalist>
```

The input's `list` attribute must match the datalist's `id`.

### Select vs. Datalist

  -----------------------------------------------------------------------
  Select                              Datalist
  ----------------------------------- -----------------------------------
  User chooses from defined options.  Offers suggestions for an input.

  Normally restricts the choice to    User can usually enter another
  available options.                  value.

  Uses `<option>` inside `<select>`.  Uses an input's `list` attribute
                                      connected to `<datalist>`.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 12. Textarea

`<textarea>` creates a multi-line text input.

``` html
<label for="message">Message:</label>

<textarea
    id="message"
    name="message"
    placeholder="Enter your message"
    cols="50"
    rows="5"
    maxlength="200">
</textarea>
```

### Important attributes

  Attribute       Purpose
  --------------- ----------------------------------------------------
  `name`          Identifies the submitted field.
  `id`            Identifies the element and connects it to a label.
  `placeholder`   Displays a hint.
  `rows`          Specifies the visible number of text rows.
  `cols`          Specifies the approximate visible character width.
  `maxlength`     Limits the maximum number of characters.

### Input text vs. Textarea

-   `<input type="text">` is designed for single-line text.
-   `<textarea>` is designed for multi-line text.

Unlike an input's `value` attribute, a textarea's initial text is
written between its opening and closing tags.

``` html
<textarea name="message">Initial message</textarea>
```

------------------------------------------------------------------------

## 13. Iframes

An `<iframe>` embeds another browsing context inside the current page.

``` html
<iframe
    src="https://example.com"
    width="600"
    height="400"
    title="Example website">
</iframe>
```

### Important attributes

  -----------------------------------------------------------------------
  Attribute                           Purpose
  ----------------------------------- -----------------------------------
  `src`                               URL of the embedded resource.

  `width`                             Width of the iframe.

  `height`                            Height of the iframe.

  `title`                             Accessible description of the
                                      embedded content.

  `allowfullscreen`                   Allows fullscreen presentation when
                                      supported.

  `loading="lazy"`                    Defers loading until the iframe is
                                      near the viewport.

  `referrerpolicy`                    Controls the referrer information
                                      sent with the request.
  -----------------------------------------------------------------------

### Common uses

-   Embedding maps.
-   Embedding YouTube videos.
-   Displaying another webpage or web application.

### Iframe vs. Anchor

-   An anchor navigates to a resource when activated.
-   An iframe embeds a resource within the current page.

### Can every website be embedded?

No. A website may prevent embedding through security policies such as
`X-Frame-Options` or the CSP `frame-ancestors` directive.

### Why use lazy loading?

``` html
<iframe src="https://example.com" loading="lazy" title="Example"></iframe>
```

Lazy loading can delay loading off-screen content, helping reduce
unnecessary work during the initial page load.

------------------------------------------------------------------------

## 14. Audio and Video

HTML provides native elements for embedding media.

### 14.1 Video

``` html
<video
    width="400"
    height="300"
    controls
    muted
    loop
    poster="./image1.jpg"
    preload="metadata">

    <source src="./video.mp4" type="video/mp4">

    Your browser does not support the video element.
</video>
```

### Video attributes

  Attribute    Purpose
  ------------ --------------------------------------------------
  `width`      Displayed video width.
  `height`     Displayed video height.
  `controls`   Displays playback controls.
  `autoplay`   Requests automatic playback.
  `muted`      Starts the media muted.
  `loop`       Repeats playback.
  `poster`     Specifies the preview image before playback.
  `preload`    Gives the browser a hint about preloading media.

### Preload values

  Value        Meaning
  ------------ ---------------------------------------------
  `auto`       Browser may preload the entire media.
  `metadata`   Browser may load metadata such as duration.
  `none`       Browser should not preload the media.

These are hints to the browser; actual behavior can vary.

### 14.2 Source element

``` html
<video controls>
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
</video>
```

The browser can select a source format it supports.

For a simple media file, `src` can also be used directly:

``` html
<video src="video.mp4" controls></video>
```

Using `<source>` is useful when providing alternative formats.

### 14.3 Audio

``` html
<audio controls muted loop preload="metadata">
    <source src="audio.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
</audio>
```

Common audio attributes:

-   `controls`
-   `autoplay`
-   `muted`
-   `loop`
-   `preload`

### Audio vs. Video

-   `<audio>` embeds sound.
-   `<video>` embeds visual media and may also include sound.

### Common interview questions

**What is the purpose of `poster`?**

It specifies the image displayed before the video plays.

**What is the difference between `muted` and `controls`?**

-   `muted` mutes the media.
-   `controls` displays playback controls.

**Does autoplay always work?**

No. Browsers commonly restrict autoplay with audible sound. Muted
autoplay is more likely to be allowed.

**Can `autoplay` and `poster` be used together?**

Yes. They are not mutually exclusive. The poster can serve as the
preview before playback begins.

------------------------------------------------------------------------

## 15. Div and Span

Both `<div>` and `<span>` are generic containers. They do not
communicate a specific semantic meaning by themselves.

### 15.1 Div

`<div>` is a generic block-level container by default.

``` html
<div>
    <h2>About Us</h2>
    <p>Welcome to our website.</p>
</div>
```

It is commonly used to group larger sections or elements for styling and
layout.

### 15.2 Span

`<span>` is a generic inline container by default.

``` html
<p>
    Hello <span style="color: red;">Malak</span>
</p>
```

It is commonly used to target a small portion of inline content.

### Div vs. Span

  -----------------------------------------------------------------------
  Div                                 Span
  ----------------------------------- -----------------------------------
  Block-level by default.             Inline by default.

  Starts on a new line in normal      Stays within the current line.
  flow.                               

  Takes the available width by        Takes the width required by its
  default.                            content.

  Often groups larger sections.       Often targets part of a text line.
  -----------------------------------------------------------------------

### Can a span be placed inside a paragraph?

Yes. This is a common use:

``` html
<p>
    HTML is <span style="color: blue;">important</span> for web development.
</p>
```

------------------------------------------------------------------------

## 16. Text Formatting Elements

HTML has elements that provide visual formatting or semantic meaning to
text.

  -----------------------------------------------------------------------
  Element                             Purpose
  ----------------------------------- -----------------------------------
  `<b>`                               Draws attention with bold
                                      presentation without indicating
                                      extra importance.

  `<strong>`                          Indicates strong importance,
                                      seriousness, or urgency.

  `<i>`                               Represents text in an alternate
                                      voice or mood, or otherwise offset
                                      from normal prose.

  `<em>`                              Indicates stress emphasis.

  `<u>`                               Represents a non-textual
                                      annotation, commonly rendered with
                                      an underline.

  `<ins>`                             Represents inserted content.

  `<mark>`                            Highlights text relevant in the
                                      current context.

  `<del>`                             Represents deleted content.

  `<small>`                           Represents side comments or small
                                      print.

  `<sup>`                             Displays superscript text.

  `<sub>`                             Displays subscript text.
  -----------------------------------------------------------------------

### Examples

**Bold and strong**

``` html
<b>Bold presentation</b>
<strong>Important information</strong>
```

`<b>` is primarily presentational; `<strong>` adds semantic importance.

**Italic and emphasis**

``` html
<i>Alternate voice or term</i>
<em>Emphasized words</em>
```

`<i>` is not simply a synonym for emphasis; `<em>` indicates stress
emphasis.

**Underline and inserted text**

``` html
<u>Annotated text</u>
<ins>Newly inserted text</ins>
```

**Mark**

``` html
<p>This is <mark>important</mark>.</p>
```

**Deleted text**

``` html
<del>Old price: $100</del>
<p>New price: $50</p>
```

**Small text**

``` html
<small>Terms and conditions apply.</small>
```

**Superscript and subscript**

``` html
<p>3<sup>4</sup></p>
<p>H<sub>2</sub>O</p>
```

-   `<sup>` raises the text, as in exponents.
-   `<sub>` lowers the text, as in chemical formulas.

------------------------------------------------------------------------

## 17. Important Differences to Remember

This section is useful for quick interview revision.

  -----------------------------------------------------------------------
  Pair                                Main difference
  ----------------------------------- -----------------------------------
  `head` vs. `body`                   Metadata/resources vs. page
                                      content.

  `href` vs. `src`                    Link destination vs. embedded
                                      resource location.

  `id` vs. `name`                     Document identifier vs. submitted
                                      form-field name.

  `th` vs. `td`                       Header cell vs. data cell.

  `rowspan` vs. `colspan`             Spans rows vs. spans columns.

  `ol` vs. `ul`                       Ordered vs. unordered list.

  `GET` vs. `POST`                    Query parameters in URL vs. request
                                      body.

  `radio` vs. `checkbox`              One choice per group vs. multiple
                                      choices.

  `disabled` vs. `readonly`           Disabled controls are not
                                      submitted; readonly controls can be
                                      submitted.

  `checked` vs. `selected`            Radio/checkbox state vs. select
                                      option state.

  `value` vs. `placeholder`           Actual initial value vs. temporary
                                      hint.

  `select` vs. `datalist`             Defined choices vs. suggestions
                                      with free entry.

  `input` vs. `textarea`              Single-line vs. multi-line text.

  `iframe` vs. `a`                    Embedded browsing context
                                      vs. navigation link.

  `div` vs. `span`                    Block-level by default vs. inline
                                      by default.

  `b` vs. `strong`                    Bold presentation vs. semantic
                                      importance.

  `i` vs. `em`                        Alternate voice/style vs. stress
                                      emphasis.

  `muted` vs. `controls`              Mutes media vs. displays playback
                                      controls.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 18. Common Mistakes and Corrections

### Mistake 1: Thinking POST encrypts data

Incorrect: POST hides and encrypts form data.

Correct: POST sends data in the request body. HTTPS is responsible for
encryption in transit.

### Mistake 2: Using placeholder instead of label

Incorrect:

``` html
<input type="email" placeholder="Email">
```

Better:

``` html
<label for="email">Email:</label>
<input type="email" id="email" name="email" placeholder="Enter your email">
```

### Mistake 3: Forgetting `name`

``` html
<input type="text" id="username">
```

This input can be used in the page, but it has no `name`, so it will not
be included as a named field in normal form submission.

Better:

``` html
<input type="text" id="username" name="username">
```

### Mistake 4: Giving radio buttons different names

Incorrect when the intention is one selection from a group:

``` html
<input type="radio" name="male" value="Male">
<input type="radio" name="female" value="Female">
```

Correct:

``` html
<input type="radio" name="gender" value="Male">
<input type="radio" name="gender" value="Female">
```

### Mistake 5: Forgetting `value` on radio and checkbox inputs

``` html
<input type="radio" name="gender">
```

If selected, a radio input without an explicit `value` submits the
default value `on`.

Prefer:

``` html
<input type="radio" name="gender" value="Male">
```

### Mistake 6: Assuming hidden inputs are secure

Hidden inputs are still accessible through browser tools and can be
modified by users. Validate important values on the server.

### Mistake 7: Using file input without multipart encoding

For a normal file upload, use:

``` html
<form method="post" enctype="multipart/form-data">
    <input type="file" name="file">
    <input type="submit">
</form>
```

### Mistake 8: Confusing `rowspan` and `colspan`

-   `rowspan`: Vertical span across rows.
-   `colspan`: Horizontal span across columns.

### Mistake 9: Treating datalist like select

A select normally restricts the choice to its options. A datalist
provides suggestions while allowing free text entry.

### Mistake 10: Thinking `div` and `span` are semantic elements

They are generic containers. Use semantic elements when the content has
a meaningful role.

------------------------------------------------------------------------

## 19. Interview Questions

Try answering these without looking at the explanations.

### Fundamentals

1.  What does HTML stand for?
2.  Why is HTML called a markup language?
3.  Is HTML a programming language? Why?
4.  What is the purpose of `<!DOCTYPE html>`?
5.  What is the difference between `<head>` and `<body>`?
6.  What is the purpose of the viewport meta tag?
7.  How many heading levels exist in HTML?
8.  What is the difference between `<br>` and `<hr>`?
9.  What is an HTML attribute?
10. What is a void element? Give examples.

### Images and links

11. What is the purpose of the `alt` attribute?
12. What is the difference between relative and absolute paths?
13. What is the difference between `src` and `href`?
14. What is the purpose of `target="_blank"`?
15. How can you create an email link?
16. How can you make an image clickable?
17. How can you navigate to a section on the same page?

### Tables and lists

18. What is the difference between `th` and `td`?
19. What is the purpose of `thead`, `tbody`, and `tfoot`?
20. What is the difference between `rowspan` and `colspan`?
21. What happens when a cell has `rowspan="3"`?
22. What are the three main types of HTML lists?
23. What is the difference between `ol` and `ul`?
24. What do `dt` and `dd` represent?
25. How can you start an ordered list from a particular number?

### Forms

26. What is the purpose of the `<form>` element?
27. What is the difference between GET and POST?
28. Does POST encrypt data?
29. What does the `action` attribute do?
30. What does the `method` attribute do?
31. What is the difference between `id` and `name`?
32. Why should we use a label?
33. What is the difference between `placeholder` and `value`?
34. What is the purpose of `fieldset` and `legend`?
35. Why do radio buttons in one group need the same name?
36. What is the difference between radio buttons and checkboxes?
37. What happens if a radio input has no explicit value?
38. What is the purpose of the `multiple` attribute?
39. Why do file uploads normally use `multipart/form-data`?
40. What is the difference between `disabled` and `readonly`?
41. What is the difference between `checked` and `selected`?
42. What is the purpose of `required`?
43. What does `step` do in a number input?
44. What is a hidden input, and is it secure?
45. What is the difference between submit and reset?

### Select, datalist, and textarea

46. What is the purpose of `<select>`?
47. What is the purpose of `<optgroup>`?
48. What is the difference between select and datalist?
49. How do you connect an input to a datalist?
50. What is the difference between input text and textarea?
51. What do `rows`, `cols`, and `maxlength` do?

### Embedded content and formatting

52. What is an iframe?
53. Can every website be embedded in an iframe?
54. What is the purpose of `loading="lazy"`?
55. What is the purpose of the `title` attribute on an iframe?
56. What is the difference between audio and video elements?
57. What does the `controls` attribute do?
58. What does `poster` do?
59. What are the possible values of `preload`?
60. Does autoplay always work?
61. What is the difference between div and span?
62. What is the difference between b and strong?
63. What is the difference between i and em?
64. What is the difference between sup and sub?
65. What is the purpose of mark and del?

------------------------------------------------------------------------

## 20. Practical Revision Tasks

Try implementing these tasks without copying the examples.

### Task 1: Personal information page

Create an HTML page containing:

-   A valid HTML document structure.
-   A page title.
-   One `h1` and at least two lower-level headings.
-   Two paragraphs.
-   An image with meaningful alternative text.
-   An internal link and an external link.
-   An email link.

### Task 2: Student table

Create a table with:

-   A caption.
-   A header containing three columns.
-   At least four data rows.
-   A `rowspan` example.
-   A `colspan` example.
-   A footer row.

### Task 3: Lists

Create:

-   An ordered list using Roman numerals.
-   An ordered list starting from 3.
-   An unordered list using square bullets.
-   A description list.
-   A nested list.

### Task 4: Registration form

Create a registration form with:

-   Name, email, and password.
-   Gender radio buttons.
-   Multiple hobby checkboxes.
-   CV file upload allowing multiple files.
-   Date of birth.
-   Number input with min, max, and step.
-   Range input.
-   Color input.
-   Hidden input.
-   Country dropdown with optgroups.
-   Datalist for favorite color.
-   Message textarea.
-   Reset and submit controls.

Make sure labels are connected to their controls and form fields have
appropriate names.

### Task 5: Media page

Create a page containing:

-   One iframe.
-   One video with controls, muted, loop, poster, and metadata preload.
-   One audio element with controls.

### Task 6: Formatting page

Use:

-   `b` and `strong`.
-   `i` and `em`.
-   `u` and `ins`.
-   `mark` and `del`.
-   `small`.
-   `sup` and `sub`.
-   `div` and `span`.

### Task 7: Debug this form

Find and correct the problems:

``` html
<form action="register.php" method="get">
    <label for="username">Username</label>
    <input type="text" id="user" placeholder="Name">

    <input type="radio" name="male" value="Male">
    <input type="radio" name="female" value="Female">

    <input type="file" name="cv" multiple>

    <input type="submit" value="Register">
</form>
```

Think about:

-   Label and input connection.
-   Missing field names.
-   Radio grouping.
-   File upload method and encoding.

------------------------------------------------------------------------

## 21. Quick Reference

### Common HTML elements

  Element      Use
  ------------ ---------------------------
  `html`       Root document element
  `head`       Metadata and resources
  `title`      Browser tab title
  `body`       Page content
  `h1`--`h6`   Headings
  `p`          Paragraph
  `br`         Line break
  `hr`         Thematic break
  `img`        Image
  `a`          Hyperlink
  `table`      Table
  `caption`    Table caption
  `thead`      Table header group
  `tbody`      Table body group
  `tfoot`      Table footer group
  `tr`         Table row
  `th`         Header cell
  `td`         Data cell
  `ol`         Ordered list
  `ul`         Unordered list
  `li`         List item
  `dl`         Description list
  `dt`         Description term
  `dd`         Description details
  `form`       Form
  `label`      Form-control label
  `input`      Input control
  `fieldset`   Group of controls
  `legend`     Fieldset caption
  `select`     Dropdown
  `option`     Dropdown option
  `optgroup`   Option group
  `datalist`   Input suggestions
  `textarea`   Multi-line input
  `iframe`     Embedded browsing context
  `video`      Video media
  `audio`      Audio media
  `source`     Media source
  `div`        Generic block container
  `span`       Generic inline container
  `b`          Bold presentation
  `strong`     Strong importance
  `i`          Alternate voice/style
  `em`         Stress emphasis
  `u`          Annotation
  `ins`        Inserted content
  `mark`       Highlight
  `del`        Deleted content
  `small`      Small print
  `sup`        Superscript
  `sub`        Subscript

### Common form input types

``` html
<input type="text">
<input type="email">
<input type="password">
<input type="radio">
<input type="checkbox">
<input type="file">
<input type="date">
<input type="month">
<input type="week">
<input type="datetime-local">
<input type="number">
<input type="range">
<input type="color">
<input type="hidden">
<input type="submit">
<input type="reset">
```

------------------------------------------------------------------------

## Final Revision Strategy

For each topic, make sure you can do three things:

1.  **Explain:** Describe what the element or attribute does in your own
    words.
2.  **Compare:** Explain the difference between similar elements and
    attributes.
3.  **Implement:** Write a small working example without looking at the
    notes.

A good interview answer should be clear and direct. You do not need to
recite the entire documentation; you need to demonstrate that you
understand what the browser does with your HTML.

**Suggested order:** Review the explanations, answer the interview
questions, then complete the practical tasks---especially the
registration form and debugging task.
