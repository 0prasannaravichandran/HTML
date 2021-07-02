# HTML
HTML (HyperText Markup Language) is the most basic building block of the Web. It defines the meaning and structure of web content.

![HTML banner](https://pixelmechanics.com.sg/wp-content/uploads/2019/06/html5-logo-for-web-development-1200x667.png)

## Description
The HyperText Markup Language`, `or HTML is the standard markup language for documents designed to be displayed in a web browser. HTML describes the structure of a web page semantically and originally included cues for the appearance of the document.

HTML elements are the building blocks of HTML pages. With HTML constructs`, `images and other objects such as interactive forms may be embedded into the rendered page. HTML provides a means to create structured documents by denoting structural semantics for text such as headings`, `paragraphs`, `lists`, `links`, `quotes and other items. HTML elements are delineated by tags`, `written using angle brackets. Browsers do not display the HTML tags`, `but use them to interpret the content of the page.

## Structure

- Start Tag
- End Tag
- Self Closing Tag
- HTML Element
- HTML Attribute

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>A Basic HTML5 Template</title>
  <link rel="stylesheet" href="css/styles.css?v=1.0">
	</head>
	<body>
  <!-- your content here... -->
  <script src="js/scripts.js"></script>
</body>
</html>
```
> **Note** : [Emmet Cheat Sheet](https://docs.emmet.io/cheat-sheet/)

## Basic Elements

- `head`, `title`, `body`, `header`, `footer`, `article`, 
- `section`, `p`, `div`, `span`, `img`, `aside`, `audio`,
- `canvas`, `datalist`, `details`, `embed`, `nav`, `output`,
- `progress`, `video`, `ul`, `ol`, `li`

### Add comments inside an HTML file
```html
<!-- This is a comment -->
<p>This is a paragraph.</p>
<!-- Remember to add more information here -->
```

### Add an Image
```html
<img src="/path/image.jpg" alt="ButtonImage">
```
- The src attribute is required`, `and contains the path to the image you want to embed.
- The alt attribute holds a text description of the image`, `which isn't mandatory but is incredibly useful for accessibility

### Add a Link
A basic link is created by wrapping the text or other content`, `inside an <a> element and using the href attribute`, `
also known as a Hypertext Reference`, `or target`, `that contains the web address.
- CTRL + Click to open the URL in a new tab.
```html
<a href="https://www.mozilla.org/en-US/">the Mozilla homepage</a>
```

### Add a table
The `table` HTML element represents tabular data — that is`, `information presented in a two-dimensional table 
comprised of rows and columns of cells containing data.
```html
<table>
    <thead>
        <tr>
            <th colspan="2">The table header</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>The table body</td>
            <td>with two columns</td>
        </tr>
    </tbody>
</table>
```

### Meta Tag
The `meta` HTML element represents metadata that cannot be represented by other HTML meta-related elements, like `base`, `link`, `script`, `style` or `title`.

```html
meta charset="utf-8">

<!-- Redirect page after 3 seconds -->
<meta http-equiv="refresh" content="3;url=https://www.mozilla.org">
```
The type of metadata provided by the meta element can be one of the following:
- If the **name** attribute is set, the meta element provides document-level metadata, applying to the whole page.
- If the **http-equiv** attribute is set, the meta element is a pragma directive, providing information equivalent to what can be given by a similarly-named HTTP header.
- If the **charset** attribute is set, the meta element is a charset declaration, giving the character encoding in which the document is encoded.
- If the **itemprop** attribute is set, the meta element provides user-defined metadata.

## Form Component
The `form` HTML element represents a document section containing interactive controls for submitting information.

```html
<form action="" method="get" class="form-example">
  <div class="form-example">
    <label for="name">Enter your name: </label>
    <input type="text" name="name" id="name" required>
  </div>
  <div class="form-example">
    <label for="email">Enter your email: </label>
    <input type="email" name="email" id="email" required>
  </div>
  <div class="form-example">
    <input type="submit" value="Subscribe!">
  </div>
</form>
```

### Attributes
The following attributes control behavior during form submission.

#### action
The URL that processes the form submission. This value can be overridden by a formaction attribute on a `button`, `input type="submit"`, or `input type="image"` element.

#### enctype
If the value of the method attribute is post, enctype is the MIME type of the form submission. Possible values:
- application/x-www-form-urlencoded: The default value.
- multipart/form-data: Use this if the form contains `input` elements with type=file.
- text/plain: Introduced by HTML5 for debugging purposes.
This value can be overridden by formenctype attributes on `button`, `input type="submit"`, or `input type="image"` elements.

#### method
The HTTP method to submit the form with. Possible (case insensitive) values:
- post: The POST method; form data sent as the request body.
- get: The GET method; form data appended to the action URL with a ? separator. Use this method when the form has no side-effects.
- dialog: When the form is inside a `dialog`, closes the dialog on submission.
This value is overridden by formmethod attributes on `button`, `input type="submit"`, or `input type="image"` elements.

#### novalidate
This Boolean attribute indicates that the form shouldn't be validated when submitted. If this attribute is not set (and therefore the form is validated), it can be overridden by a formnovalidate attribute on a `button`, `input type="submit"`, or `input type="image"` element belonging to the form.

#### target
Indicates where to display the response after submitting the form. In HTML 4, this is the name/keyword for a frame. In HTML5, it is a name/keyword for a browsing context (for example, tab, window, or iframe). The following keywords have special meanings:
- _self (default): Load into the same browsing context as the current one.
- _blank: Load into a new unnamed browsing context.
- _parent: Load into the parent browsing context of the current one. If no parent, behaves the same as _self.
- _top: Load into the top-level browsing context (i.e., the browsing context that is an ancestor of the current one and has no parent). If no parent, behaves the same as _self.
This value can be overridden by a formtarget attribute on a `button`, `input type="submit"`, or `input type="image"` element.

### Input Types

- `button`  ,`checkbox`        ,`color`
- `date`    ,`datetime-local`  ,`email`
- `file`    ,`hidden`          ,`image`
- `month`   ,`number`          ,`password`
- `radio`   ,`range`           ,`reset`
- `search`  ,`submit`          ,`tel`
- `text`    ,`time`            ,`url`
- `week`

### Event handler Attributes

 `onabort`, `onautocomplete`, `onautocompleteerror`, `onblur`, `oncancel`, `oncanplay`, `oncanplaythrough`, `onchange`, `onclick`, `onclose`, `oncontextmenu`,
 `oncuechange`, `ondblclick`, `ondrag`, `ondragend`, `ondragenter`, `ondragexit`, `ondragleave`, `ondragover`, `ondragstart`, `ondrop`, `ondurationchange`,
 `onemptied`, `onended`, `onerror`, `onfocus`, `oninput`, `oninvalid`, `onkeydown`, `onkeypress`, `onkeyup`, `onload`, `onloadeddata`, `onloadedmetadata`,
 `onloadstart`, `onmousedown`, `onmouseenter`, `onmouseleave`, `onmousemove`, `onmouseout`, `onmouseover`, `onmouseup`, `onmousewheel`, `onpause`, `onplay`,
 `onplaying`, `onprogress`, `onratechange`, `onreset`, `onresize`, `onscroll`, `onseeked`, `onseeking`, `onselect`, `onshow`, `onsort`, `onstalled`, `onsubmit`,
 `onsuspend`, `ontimeupdate`, `ontoggle`, `onvolumechange`, `onwaiting`.
 
### Global Attributes

 |	Attributes	|	value	|	Description	|
|	----	|	-----	|	------	|
|	accesskey	|	character	|	It is used to generate keyboard shortcuts for the current element.	|
|	class	|	classname	|	It is used to provide the class name for the current element. It is mainly used with the stylesheet.	|
|	Contenteditable	|	TRUE/FALSE	|	It determines whether the content within an element is editable or not.	|
|	contextmenu	|	menu_id	|	It defines the id for the <menu> element which is used as a context menu (a menu appear on right click) for an element.	|
|	data-*	|	somevalue	|	It is used to store element-specific private data which can be accessed by Javascript.	|
|	dir	|	rtl, ltr, auto	|	It specifies the direction of the content inside the current element.	|
|	draggable	|	TRUE, FALSE, Auto	|	It specifies whether the content within an element is movable or not using Drag and Drop API.	|
|	dropzone	|	copy, move, link	|	It specifies the action is taken on the dragged element when it is dropped, ¬¬ such as whether it is copied, moved or linked.	|
|	hidden	|		|	It is used to hide the element from view.	|
|	id	|	id	|	It specifies a unique id for the element. It can be used with CSS and JavaScript.	|
|	lang	|	language_code	|	It specifies the primary language for the content of an element.	|
|	style	|	style	|	It is used to apply inline CSS to the current element.	|
|	spellcheck	|	TRUE/FALSE	|	It specifies whether the content should be checked for spelling errors or not.	|
|	tabindex	|	number	|	It determines the tabbing order of an element.	|
|	title	|	text	|	It is used to provide the title, name, or some extra information about the element.	|
|	translate	|	yes/no	|	It specifies whether the content of the element should be translated when the page is localized or not.	|

### Deprecated Tags

|	Tag	|	Description	|	Alternate	|
|	------	|	----------	|	------------	|
|	applet|	Deprecated. Specifies an applet	|	object|
|	basefont|	Deprecated. Specifies a base font	|		|
|	center|	Deprecated. Specifies centered text	|	text-align	|
|	dir|	Deprecated. Specifies a directory list	|		|
|	embed|	Deprecated. Embeds an application in a document	|	object|
|	font|	Deprecated. Specifies text font`, `size`, `and color	|	font-family`, `font-size	|
|	isindex|	Deprecated. Specifies a single-line input field	|		|
|	listing|	Deprecated. Specifies listing of items	|	pre|
|	menu|	Deprecated. Specifies a menu list	|		|
|	plaintext|	Deprecated. Specifies plaintext	|	pre|
|	s|	Deprecated. Specifies strikethrough text	|	text-decoration	|
|	strike|	Deprecated. Specifies strikethrough text	|	text-decoration	|
|	u|	Deprecated. Specifies underlined text	|	text-decoration	|
|	xmp|	Deprecated. Specifies preformatted text	|	pre|

### Deprecated Attributes

|	Attribute	|	Description	|	Alternate	|
|------		|------		|-------		|
|	align	|	Specifies positioning of an element	|	text-align`, `float & vertical-align	|
|	alink	|	Specifies the color of an active link or selected link	|	active	|
|	background	|	Specifies background image	|	background-image	|
|	bgcolor	|	Specifies background color	|	background-color	|
|	border	|	Specifies a border width of any element	|	border-width	|
|	clear	|	Indicates how the browser should display the line after the <br /> element	|	clear	|
|	height	|	Specifies height of body and other elements	|	height	|
|	hspace	|	Specifies the amount of whitespace or padding that should appear left or right an element	|	padding	|
|	language	|	Specifies scripting language being used	|	type	|
|	link	|	Specifies the default color of all links in the document	|	link	|
|	nowrap	|	Prevents the text from wrapping within that table cell	|	white-space	|
|	start	|	Indicates the number at which a browser should start numbering a list	|	counter-reset	|
|	text	|	Specifies color of body text	|	color	|
|	type	|	Specifies the type of list in <li> tag	|	list-style-type	|
|	vlink	|	Specifies the color of visited links	|	visited	|
|	vspace	|	Specifies the amount of whitespace or padding that should appear above or below an element	|	padding	|
|	width	|	Specifies width of body and other elements	|	width	|

## Important Links

- [MDN - HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [W3Schools - HTML](https://www.w3schools.com/html/)
- [Dev Docs - HTML](https://devdocs.io/html/)
