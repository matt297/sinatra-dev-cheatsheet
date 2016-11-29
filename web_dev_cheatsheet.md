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
    - [Logical operators](#logical-operators)
    - [Logic and conditions](#logic-and-conditions)
    - [Methods](#methods)
  1. [Sinatra](#sinatra)
    - [Defining URLs](#defining-urls)
    - [Using a layout](#using-a-layout)
    - [Instance variables](#instance-variables)
    - [Partials](#partials)
  1. [Git](#git)


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
| `<h1> <h2> <h3> <h4>` | Headings | Yes | [Link](http://www.w3schools.com/tags/tag_hn.asp) |
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


### Logical operators

When performing logic, ruby always returns one of two things: `true` or `false`. That makes it easy for us to build programs around this behaviour. To do logic, you use operators, which are listed in the table below.

| Operator | Description | Info/Example |
| -------- | ----------- | ------------ |
| `==` | Equal to | [Link](https://www.tutorialspoint.com/ruby/ruby_operators.htm) |
| `!=` | Not equal to | [Link](https://www.tutorialspoint.com/ruby/ruby_operators.htm) |
| `>` | Greater than | [Link](https://www.tutorialspoint.com/ruby/ruby_operators.htm) |
| `>=` | Greater than or equal to | [Link](https://www.tutorialspoint.com/ruby/ruby_operators.htm) |
| `<` | Less than | [Link](https://www.tutorialspoint.com/ruby/ruby_operators.htm) |
| `<=` | Less than or equal to | [Link](https://www.tutorialspoint.com/ruby/ruby_operators.htm) |
| `&&` | And (allows you to combine multiple conditions) | [Link](https://www.tutorialspoint.com/ruby/ruby_operators.htm) | 
| `||` | Or (allows you to combine multiple conditions | [Link](https://www.tutorialspoint.com/ruby/ruby_operators.htm) |

```ruby
# Comparing two things
variable_one == variable_two

# Using multiple conditions
variable_one == variable_two && variable_three != variable_four
```


### Logic and conditions

Often times when programming, we need to perform logic, or create a set of conditions for a particular thing to happen. In ruby, this can be done in a variety of ways. The most common, is using an if/else block.

```ruby
# Simple with only one condition
if seconds > 60
  'More than 1 minute ago.'
else
  'Less than 1 minute ago.'
end

# More complex, with a few possibilities
if time_of_day == 'Morning'
  'Good morning!'
elsif time_of_day == 'Afternoon'
  'Good afternoon!'
else
  'Good evening!'
end

# Using multiple conditions
if time_of_day == 'Morning' && weather != 'Raining' do
  'Happy morning! It is not raining!'
end
```


### Methods

In programming, you often need to re-use code multiple times. Whenver this needs to be done, you put that code inside of a method, and then you can simply run the method whenver you need that code. Methods can either accept arguments (i.e. take in values and then do something with those values), or accept no arguments (i.e. if you just want to print out something). To define a method, you use the `def` and `end` keywords.

Remember, in Ruby, the last line of a method is automatically returned as the final value.

```ruby
# Define a new method with no arguments
def say_hello
  'Hello world!'
end

# Run the method (returns "Hello World!")
say_hello()

# Define a new method with two arguments
def multiply(first_number, second_number)
  first_number * second_number
end

# Run the method (returns "25")
multiply(5,5)

```


## Sinatra

In Sinatra, there are two primary types of files: ruby files (ending in `.rb`, only containing Ruby code), and embedded ruby files (ending in `.erb` and combining both HTML + Ruby code). ERB files are usually found in the `app/views/` folder, while Ruby files can be found in `app/` or `app/models/`. 


### Defining URLs

To define a new URL in Sinatra, you edit your `app/actions.rb` file. You can add as many URLs as you like, and each one will be visitable in the browser by a site visitor.

```ruby
get '/' do
  # This code gets run when a user visits "yoursite.com/"
end

get '/signup' do
  # This code gets run when a user visits "yoursite.com/signup"
end
```

Using the code above, your site visitor would just see a blank page, because you haven't defined any code to run. If you wanted to render the contents of a particular view file (ERB), you would have to explicitly tell Sinatra to do so. Here's how:

```ruby
get '/' do
  erb(:homepage) # Sinatra will now render the 'homepage.erb' file when a user visits 'yoursite.com/'
end
```


### Using a layout

Often times, websites will have a consistent header and footer that are shown on every page. In Sinatra, the way you accomplish this is by creating a `layout.erb` file. The contents of this file will be displayed on every single page of your app, so that each page has a consistent look and feel. In your `layout.erb` file, you also need to specify where the contents of each page go, and you do that using the `<%= yield %>` tag. Here is a sample layout file...

```html
<!doctype html>
<html>
  <head>
    <title>Super App</title>
  </head>
  <body>
    
    <img src="logo.jpg">
    <h1>Super App</h1>
    
    <!-- This is where the page contents gets inserted -->
    <%= yield %>
  
  </body>
</html>
```


### Instance variables

Sometimes you need to pass a variable/value to your view file, so that it can display something dynamically. For instance, maybe you want to display a homepage that says "Good morning" or "Good evening" based on the time of day. You would need to pass the time of day into your view file. To do so, you would use an instance variable (one that starts with an `@` sign).

```ruby
# Inside your actions.rb file

get '/' do
  @time_of_day = Time.now
  erb(:homepage)
end
```

```html
<!-- Inside your homepage.erb file -->

The current day and time is: <%= @time_of_day %>
```


### Partials

Sometimes in your application, you will want to re-use not only ruby code, but also HTML. The way you create re-usable HTML is by creating partials. A partial is a `.erb` file just like any other, and works exactly the same way. If someone had a weather app, perhaps they would create a single partial that contained today's forecast. Then, each time they wanted to show the forecast, they would just use the partial rather than re-typing all the code. Here's an example:

```ruby
# In the actions.rb file

get '/' do 
  erb(:homepage)
end

```

```html
<!-- In your homepage.erb file -->

<%= erb(:todays_forecast) %>
```

```html
<!-- In a new partial, called "todays_forecast.erb" -->

The forecast for today is sunny with a chance of meatballs!
```

You can get even more complicated with partials and also pass variables into them. For instance, consider the case of a blog website, where comments should always appear in the same format, but the actual text of the comment might change. Here is how you might approach that:

```ruby
# In actions.rb

get '/' do
  @comment = "Great post! Really fun to read!"
  @commenter = "Joe"
  erb(:homepage)
end
```

```html
<!-- In your homepage.erb file -->

<%= erb(:comment, locals: { text: @comment, name: @commenter }) %>
```

```html
<!-- In a new partial, called "comment.erb" -->

<%= name %> says: <%= text %>
```


## Git