# Sinatra & Web Development Cheat Sheet

## Table of Contents

  1. [HTML](#html)
    - [Basic page structure](#basic-page-structure)
    - [Formatting tags](#formatting-tags)
    - [Content tags](#content-tags)
    - [Structural tags](#structural-tags)
  1. [CSS](#css)
    - [Formatting](#formatting)
    - [Rule delcarations](#rule-declarations)
    - [Selectors](#selectors)
  1. [Ruby](#ruby)
    - [Data types](#data-types)
    - [Complex data stores](#complex-data-stores)


## HTML


### Basic page structure

A basic HTML page will have the following structure, and the file will end with the `.html` extension (i.e. `mypage.html`).

```html
<!doctype html>
<html>
  <head>
    <title>Your Page Title</title>
  </head>
  <body>
  
    <!-- Page contents go here -->
  
  </body>
</html>
```

_Tip: You can open HTML files directly in your browser without the need for Sinatra or any other kind of framework/backend - just double click the file and it'll open in your default web browser! If you're using Cloud9, go to Run -> Run With -> Apache httpd._


### Formatting tags

The following tags are used to format text and paragraphs.

| HTML Tag | Purpose | Needs Closing Tag | Info/Example |
| -------- | ------- | -------------------- | --------- |
| `<p>` | Paragraph of text | Yes | [Link](http://www.w3schools.com/tags/tag_p.asp) |
| `<br>` | Line break/pushes content to next line | No | [Link](http://www.w3schools.com/tags/tag_br.asp) |
| `<strong>` | Bold text | Yes | [Link](http://www.w3schools.com/tags/tag_strong.asp) |
| `<em>` | Italic/emphasized text | Yes | [Link](http://www.w3schools.com/tags/tag_em.asp) |
| `<u>` | Underlined text | Yes | [Link](http://www.w3schools.com/tags/tag_u.asp) |
| `<s>` | Strikethrough text | Yes | [Link](http://www.w3schools.com/tags/tag_s.asp) |


### Content tags

These tags are used to insert interactive and fun elements into your page (so that it's more than just plain text).

| HTML Tag | Purpose | Needs Closing Tag | Info/Example |
| -------- | ------- | -------------------- | --------- |
| `<a href="http://google.com">Link text</a>` | Link to another page | Yes | [Link](http://www.w3schools.com/tags/tag_a.asp) |
| `<img src="http://google.com/image.jpg">` | Displays an image | No | [Link](http://www.w3schools.com/tags/tag_img.asp) |
| `<form action="/process" method="POST">` | A form | Yes | [Link](http://www.w3schools.com/tags/tag_form.asp) |
| `<input type="text">` | An input field | No | [Link](http://www.w3schools.com/tags/tag_input.asp) |
| `<input type="password">` | A password field | No | [Link](http://www.w3schools.com/tags/tag_input.asp) |
| `<input type="email">` | An email field | No | [Link](http://www.w3schools.com/tags/tag_input.asp) |
| `<label>` | Input field label | No | [Link](http://www.w3schools.com/tags/tag_label.asp) |
| `<button>` | A button | Yes | [Link](http://www.w3schools.com/tags/tag_button.asp) |
| `<table>` | A table of data | Yes | [Link](http://www.w3schools.com/tags/tag_table.asp) |
| `<ol>` | Ordered (numbered) list | Yes | [Link](http://www.w3schools.com/tags/tag_ol.asp) |
| `<ul>` | Unordered (bulleted) list | Yes | [Link](http://www.w3schools.com/tags/tag_ul.asp) |
| `<li>` | List item (within a `ol`/`ul`) | Yes | [Link](http://www.w3schools.com/tags/tag_li.asp) |


### Structural tags

The following tags are used to provide structure and are largely used for semantics (i.e. to help a screen reader or a search engine better understand the content on our pages).

| HTML Tag | Purpose | Needs Closing Tag | Info/Example |
| -------- | ------- | -------------------- | --------- |
| `<header>` | Header content | Yes | [Link](http://www.w3schools.com/tags/tag_header.asp) |
| `<nav>` | Navigation/menu content | Yes | [Link](http://www.w3schools.com/tags/tag_nav.asp) |
| `<main>` | Main content of the document | Yes | [Link](http://www.w3schools.com/tags/tag_main.asp) |
| `<article>` | An article | Yes | [Link](http://www.w3schools.com/tags/tag_article.asp) |
| `<section>` | A section of content | Yes | [Link](http://www.w3schools.com/tags/tag_section.asp) |
| `<footer>` | Footer content | Yes | [Link](http://www.w3schools.com/tags/tag_footer.asp) |
| `<div>` | Any block of content | Yes | [Link](http://www.w3schools.com/tags/tag_div.asp) |


## CSS


### Adding a stylesheet

CSS goes in a separate file, with a `.css` extension. So, for example, you might create a file called `styles.css`. Once you've created a stylesheet, you then need to include it in your HTML page, within the `<head></head>` section. Make sure that the path to the file is correct!

```html
<head>
  <link rel="stylesheet" href="path/to/styles.css">
</head>
```

### Rule declarations

A “rule declaration” is the name given to a selector (or a group of selectors) with an accompanying group of properties. It's how you tell the browser to style a particular element a particular way. Here's an example:

```css
.my-element {
  font-size: 20px;
  color: blue;
}
```


### Selectors

Within a rule declaration, you can target an element (tell the browser what to apply those styles to) in a few different ways.

| Selector | Example | Description | Info/Example |
| -------- | ------- | ----------- | --------- |
| .class | `.intro` |	Selects all elements with `class="intro"` | [Link](http://www.w3schools.com/cssref/sel_class.asp) |
| #id |	`#firstname` | Selects the element with `id="firstname"` | [Link](http://www.w3schools.com/cssref/sel_id.asp) |
| element | `p` | Selects all `<p>` elements | [Link](http://www.w3schools.com/cssref/sel_element.asp) |


### Media queries

To apply different styles for different screen sizes (i.e. mobile device vs. a desktop computer), you can use media queries. The most common ways to use media queries is to specify a `min-width`, a `max-width`, or both together.

```css
@media (min-width: 992px) {
  /* These styles will be applied to desktop browsers */
  .my-element {
    color: red;
  }
}

@media (min-width: 768px) and (max-width: 991px) {
  /* These styles will be applied to tablets */
  .my-element {
    color: green;
  }
}

@media (max-width: 767px) {
  /* These styles will be applied to mobile devices */
  .my-element {
    color: blue;
  }
}
```


## Ruby


### Data types

In ruby, we can store different types of data. These are the most common types (with a couple examples for each).

```ruby
# A string, wrapped in quotes (single or double)
first_name = 'John'
last_name = "Doe"

# An integer (has no decimal places)
first_number = 1
second_number = 10

# A float (has decimal places)
first_number = 5.5
second_number = 8.2

# A boolean (true/false value)
first_value = true
second_value = false
```

## Complex data stores

When needed, you can also store data in more complicated ways. For instance, maybe you need to create a list of things, well, Ruby makes that easy! You can use an array to store any number of things (and each thing can be of a different type - i.e. a straing, then an integer, then a float).

```ruby
# Create an array (list of things of any types)
grocery_list = ['Potatoes', 'Bread', 'Milk', 'Butter']

# To get the first item from the list (returns "Potatoes")
grocery_list[0]

# To get the second item from the list (returns "Bread")
grocery_list[1]
```

For groups of related data, you can also use a hash as a different way to store the data.

```ruby
# Create hash
person = { name: 'Matt, age: 99, favourite_book: 'Harry Potter', favourite_movie: 'Inception' }

# Get the person's name (returns "Matt")
person['name']
```