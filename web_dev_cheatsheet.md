# Sinatra & Web Development Cheat Sheet

## Table of Contents

  1. [HTML](#html)
    - [Basic Page Structure](#basic-page-structure)
    - [Common Elements](#common-elements)
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

### Common elements

| HTML Tag | Requires Closing Tag | Purpose | More Info |
| -------- | -------------------- | ------- | --------- |
| `<p>` | Yes | Paragraph of text | [Link](http://www.w3schools.com/tags/tag_p.asp) |
| `<br>` | No | Line break/pushes content to next line | [Link](http://www.w3schools.com/tags/tag_br.asp) |
| `<strong>` | Yes | Bold text | [Link](http://www.w3schools.com/tags/tag_strong.asp) |
| `<em>` | Yes | Italic/emphasized text | [Link](http://www.w3schools.com/tags/tag_em.asp) |
| `<u>` | Yes | Underlined text | [Link](http://www.w3schools.com/tags/tag_u.asp) |
| `<s>` | Yes | Strikethrough text | [Link](http://www.w3schools.com/tags/tag_s.asp) |

## CSS

### Adding a stylesheet

CSS goes in a separate file, with a `.css` extension. So, for example, you might create a file called `styles.css`. Once you've created a stylesheet, you then need to include it in your HTML page, within the `<head></head>` section. Make sure that the path to the file is correct!

```html
<head>
  <link rel="stylesheet" href="path/to/styles.css">
</head>
```

