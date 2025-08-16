
# Chapter 0: Introduction to HTML & CSS

Welcome to your first topic in web programming! This chapter will guide you through the essential features of HTML and CSS, using the examples found in this folder. By the end, you'll be able to create a rich, interactive web page from scratch.

---

## Outline
1. Basic HTML Structure
2. Adding CSS Styles
3. Creating Tables
4. Adding Images
5. Building Forms
6. JavaScript Interactivity
7. Combining Features
8. Using Bootstrap
9. Final Challenge
10. Instructor Tips

---



## 1. Basic HTML Structure
Every web page is built using a standard structure. HTML uses tags to mark up content. Most tags have an opening and a closing part:

- Opening tag: `<tagname>`
- Closing tag: `</tagname>`

For example, `<body>` starts the body section, and `</body>` ends it. All content between these tags is part of the body.

Some tags are self-closing, meaning they do not wrap content and end with a slash, like `<img />` or `<br />`.

**Common tags:**
- `<html>`: The root element for the page. Must be closed with `</html>`.
- `<head>`: Contains metadata, links to stylesheets, and the page title. Closed with `</head>`.
- `<body>`: Contains all the visible content. Closed with `</body>`.
- `<title>`: Sets the browser tab name. Closed with `</title>`.
- `<img />`: Displays an image. Self-closing.
- `<br />`: Inserts a line break. Self-closing.

**Example:**
```html
<!DOCTYPE html>
<html>
	<head>
		<title>My First Web Page</title>
	</head>
	<body>
		Hello, world!<br />
		<img src="sailboat.jpg" width="100" height="100" alt="Boat Picture" />
	</body>
</html>
```

**Try it:**
Create a new HTML file with these basic tags and a custom title. Change the text in `<body>` to your name. Add a line break and an image using self-closing tags.

---


## 2. Adding CSS Styles
CSS (Cascading Style Sheets) lets you control the appearance of your web page. You can include CSS in a `<style>` block inside `<head>`.

**Selectors:**
- `element` (e.g., `h1`) styles all elements of that type.
- `.class` styles all elements with that class.
- `#id` styles the element with that id.

**Properties:**
- `color`: Sets text color.
- `font-family`: Sets the font.
- `font-size`: Sets the size of text.

**Example:**
```html
<head>
	<style>
		h1 { color: blue; }
		.highlight { background: yellow; }
		#main { font-size: 2em; }
	</style>
</head>
<body>
	<h1 id="main">Welcome!</h1>
	<p class="highlight">This is a highlighted paragraph.</p>
</body>
```

**Try it:**
Add a `<style>` block and experiment with different selectors and properties. Try changing colors and fonts for headings and paragraphs.

---



## 3. Creating Tables
Tables are used to display data in rows and columns. The main tags are:
- `<table>`: The table itself.
- `<thead>`: The header section.
- `<tbody>`: The body section.
- `<tr>`: Table row.
- `<th>`: Table header cell.
- `<td>`: Table data cell.

**Example:**
```html
<table>
	<thead>
		<tr>
			<th>Name</th>
			<th>Email</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Alice</td>
			<td>alice@example.com</td>
		</tr>
		<tr>
			<td>Bob</td>
			<td>bob@example.com</td>
		</tr>
	</tbody>
</table>
```

**Try it:**
Build a table with headers and rows. Add more rows for your friends or family.

---


## 4. Adding Images
Images make your page more interesting. Use the `<img>` tag to display images. You can set the size using `width` and `height` attributes.

**Example:**
```html
<img src="sailboat.jpg" width="100" height="100" alt="Boat Picture">
```

**Try it:**
Add an image to your page and adjust its size. Try changing the `width` and `height` values.

---


## 5. Building Forms
Forms let you collect input from users. The main tags are:
- `<form>`: The form container.
- `<input>`: Input fields (e.g., text, number).
- `<button>`: Button to submit the form.

**Example:**
```html
<form>
	<input type="number" name="num1" placeholder="First number">
	<input type="number" name="num2" placeholder="Second number">
	<button type="submit">Compare</button>
</form>
```

**Try it:**
Create a form to input two numbers. Change the input type to `text` or `email` and see what happens.

---



## 6. JavaScript Interactivity
JavaScript lets you make your page interactive. You can use `<script>` tags to add code that responds to user actions, such as clicking a button or submitting a form.

### Regular JavaScript Alerts
An alert is a simple popup message that appears in the browser. You can use the `alert()` function to show a message to the user. Alerts are useful for quick notifications or debugging.

**Example:**
```html
<button onclick="alert('Hello! This is an alert.')">Show Alert</button>
```

**Explanation:**
- `<button>` creates a clickable button.
- The `onclick` attribute runs JavaScript when the button is clicked.
- `alert('...')` shows a popup message.

### Handling Form Input and Showing Results
This script compares two numbers entered in a form and displays the result on the page:
```html
<form id="compareForm">
	<input type="number" id="num1" placeholder="First number">
	<input type="number" id="num2" placeholder="Second number">
	<button type="submit">Compare</button>
</form>
<div id="result"></div>

<script>
document.getElementById('compareForm').onsubmit = function(event) {
	event.preventDefault(); // Prevents the page from reloading
	var n1 = parseFloat(document.getElementById('num1').value); // Gets first number
	var n2 = parseFloat(document.getElementById('num2').value); // Gets second number
	var result = '';
	if (n1 > n2) result = 'First number is greater.';
	else if (n1 < n2) result = 'Second number is greater.';
	else result = 'Numbers are equal.';
	document.getElementById('result').innerText = result; // Shows result on page
};
</script>
```

**Explanation:**
- The form collects two numbers.
- When submitted, JavaScript prevents the default action (reloading).
- It reads the values, compares them, and updates the page with the result.

**Try it:**
Add a button to your page that shows an alert. Write JavaScript to handle form submission and show the result. Try changing the logic to compare strings or other values.

---



## 7. Combining Features
You can combine all these features to create complex layouts. For example, you can nest tables inside other tables, add images to table cells, and use multiple classes and IDs for styling.

**Example:**
```html
<table>
	<tr>
		<td><img src="sailboat.jpg" width="50" height="50"></td>
		<td>
			<form>
				<input type="number" placeholder="Number">
				<button type="submit">Submit</button>
			</form>
		</td>
	</tr>
</table>
<h1 class="highlight">Styled Heading</h1>
```

**Try it:**
Combine tables, images, forms, and headings as shown in the final example. Experiment with different layouts and styles.

---




## 8. Using Bootstrap
Bootstrap is a popular CSS framework that makes it easy to create modern, responsive web pages. You can add Bootstrap by linking to its CDN in your `<head>`:
```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
```

Bootstrap provides many ready-to-use classes for styling tables, buttons, and alerts.

### Bootstrap Tables
- `table`: Basic table styling
- `table-bordered`: Adds borders
- `table-striped`: Adds striped rows

**Example:**
```html
<table class="table table-bordered table-striped">
	<thead>
		<tr>
			<th>Name</th>
			<th>Email</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Alice</td>
			<td>alice@example.com</td>
		</tr>
		<tr>
			<td>Bob</td>
			<td>bob@example.com</td>
		</tr>
	</tbody>
</table>
```

### Bootstrap Alerts
Alerts are used to show important messages to users. Bootstrap alerts are styled with classes like `alert` and `alert-success`.

**Example:**
```html
<div class="alert alert-success" role="alert">
	This is a success alert—check it out!
</div>
```

**Explanation:**
- `<div>` creates a container for the alert.
- `alert` is the base class for all alerts.
- `alert-success` makes the alert green for success messages. Other types include `alert-danger` (red), `alert-warning` (yellow), and `alert-info` (blue).
- `role="alert"` helps with accessibility.

**Try it:**
Add Bootstrap to your page and update your tables to use Bootstrap classes for enhanced appearance. Try adding a Bootstrap alert to display a message. Experiment with different alert types and messages.

---


## 9. Final Challenge
Recreate the full example from `index.html` in this folder, including all tables, images, forms, styles, scripts, and Bootstrap enhancements. Try to match the layout and features as closely as possible. This will help you practice everything you've learned in this chapter.

---


## 10. Instructor Tips
- Start with a blank file and introduce each feature one at a time.
- Explain the purpose and syntax of each new element.
- Encourage students to experiment and ask questions.
- Use live coding and encourage students to follow along and modify examples.

---

Congratulations! You’ve completed your first chapter in web programming. Move on to the next topic to continue your journey.
