# Sinatra & Web Development Cheat Sheet

## Table of Contents

  1. [HTML](#html)
    - [Basic Page Structure](#basic-page-structure)
  1. [CSS](#css)
    - [Formatting](#formatting)


## HTML

### Basic page structure

A basic HTML page will have the following structure, and the file will end with the `.html` extension (i.e. `mypage.html`). You can open HTML files directly in your browser without the need for Sinatra or any other kind of framework/backend.

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

## CSS

### Adding a stylesheet

CSS goes in a separate file, with a `.css` extension. So, for example, you might create a file called `styles.css`. Once you've created a stylesheet, you then need to include it in your HTML page, within the `<head></head>` section. Make sure that the path to the file is correct!

```html
<head>
  <link rel="stylesheet" href="path/to/styles.css">
</head>
```

