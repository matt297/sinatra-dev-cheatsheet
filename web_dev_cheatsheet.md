# Sinatra & Web Development Cheat Sheet

## Table of Contents

  1. [HTML](#html)
    - [Basic Page Structure](#basic-page-structure)
    - [Formatting Tags](#formatting-tags)
    - [Content Tags](#content-tags)
    - [Structural Tags](#structural-tags)
  1. [CSS](#css)
    - [Formatting](#formatting)


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

### Formatting Tags

The following tags are used to format text and paragraphs.

| HTML Tag | Purpose | Requires Closing Tag | Info/Example |
| -------- | ------- | -------------------- | --------- |
| `<p>` | Paragraph of text | Yes | [Link](http://www.w3schools.com/tags/tag_p.asp) |
| `<br>` | Line break/pushes content to next line | No | [Link](http://www.w3schools.com/tags/tag_br.asp) |
| `<strong>` | Bold text | Yes | [Link](http://www.w3schools.com/tags/tag_strong.asp) |
| `<em>` | Italic/emphasized text | Yes | [Link](http://www.w3schools.com/tags/tag_em.asp) |
| `<u>` | Underlined text | Yes | [Link](http://www.w3schools.com/tags/tag_u.asp) |
| `<s>` | Strikethrough text | Yes | [Link](http://www.w3schools.com/tags/tag_s.asp) |

### Content Tags

These tags are used to insert interactive and fun elements into your page (so that it's more than just plain text).

| HTML Tag | Purpose | Requires Closing Tag | Info/Example |
| -------- | ------- | -------------------- | --------- |
| `<a href="http://google.com">Link text</a>` | Link to another page | Yes | [Link](http://www.w3schools.com/tags/tag_a.asp) |
| `<img src="http://google.com/image.jpg">` | Displays an image | No | [Link](http://www.w3schools.com/tags/tag_img.asp) |
| `<form action="/process" method="POST">` | Marks the start of a form | Yes | [Link](http://www.w3schools.com/tags/tag_form.asp) |
| `<input>` | An input field | No | [Link](http://www.w3schools.com/tags/tag_input.asp) |
| `<button>` | A button | No | [Link](http://www.w3schools.com/tags/tag_button.asp) |

### Structural Tags

The following tags are used to provide structure and are largely used for semantics (i.e. to help a screen reader or a search engine better understand the content on our pages).

| HTML Tag | Purpose | Requires Closing Tag | Info/Example |
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

