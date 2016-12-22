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
    - [Ruby bascis](#ruby-basics)
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
    - [Helper methods](#helper-methods)
    - [Form data](#form-data)
    - [Sessions](#sessions)
    - [Interactive console (tux)](#interactive-console-tux)
  1. [ActiveRecord](#activerecord)
    - [Defining a new class/object](#defining-a-new-class-object)
    - [Built-in methods](#built-in-methods)
    - [Defining relationships](#defining-relationships)
    - [Model validations](#model-validations)
    - [Updating values](#updating-values)
  1. [Git](#git)
  1. [Heroku](#heroku)


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


### Ruby basics

For a more comprehensive guide to the very very basics of ruby, refer to [this guide](https://gist.github.com/matt297/055ee0b28c2bd79aa9783359d83f4906).


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

When needed, you can also store data in more complicated ways. For instance, maybe you need to create a list of things, well, Ruby makes that easy! You can use an array to store any number of things (and each thing can be of a different type - i.e. a string, then an integer, then a float).

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

You can also pass values into your `actions.rb` file by using variables in the URL. When you create variables in the URL, you can then get to them from within ruby using `params[:variable_name]`, like you do for form data. For instance, perhaps you wanted to edit a particular user. You might want to have unique edit links for each user, so you can pass them around between the various website administrators. Your `actions.rb` file might look like this:

```ruby
get '/user/:id/edit` do
  # When someone visits "yoursite.com/users/5/edit", the value of "params[:id]" would be "5"
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


### Helper methods

When you create a method, typically it's only meant for use within your ruby files. But, Sinatra has a nifty way for you to create methods that you can also use within your view files (ERB). They are called helper methods, and here's how you use them:

```ruby
# In actions.rb

helpers do
  def time_of_day
    if Time.now.hour < 12
      'Morning'
    else
      'Afternoon'
    end
  end
end

get '/' do
  erb(:homepage)
end
```

```html
<!-- In your homepage.erb file -->

Hello there! Welcome and good <%= time_of_day %> to you!
```


### Form data

When you want to get user input, you use a form. Sinatra has some fun and helpful ways to let us easily access form data submitted by a user! To start, you define a form in your erb file, making sure to specify a `method` and an `action`. The method represents _how_ the data will be sent, and the action represents _where_ the data will be sent.

| Method | Description | When to use |
| ------ | ----------- | ----------- |
| GET | Values appear in the URL | Performing searches or filtering (when you're not "changing" data in your application) |
| POST | Values are sent silently/hidden | Submitting sensitive data, or when the form will change/save something in your application |

Inside an ERB file, a form would look like this:

```html
<form method="post" action="/signup">
  <label for="first-name">
  <input type="text" name="first-name" id="first-name">
  
  <button>Submit</button>
</form>
```

Then, in your `actions.rb` file, you would create a new URL that accepts incoming `POST` requests. Remember, you can access values submitted from a form using `params`, like this:

```ruby
post '/signup' do
  @name = params[:name]
end
```


### Sessions

Sessions are a quick and easy way to store data that lasts for more than a single page-load. Remember that anything stored in a session is available for the entire duration of a users browsing session. We use ruby to interact with sessions, like so:

```ruby
# Set a session value
session[:name] = 'Matt'

# Get the value of a session (returns "Matt")
session[:name]

# Clear a session value
session[:name] = nil

# Clear all session data
session.clear
```


### Interactive console (tux)

To start up the interactive console in Sinatra, you type `bundle exec tux` in a bash window/tab. If it worked, you should see something like:

```
Loading development environment (Rack 1.3)
>>
```


## ActiveRecord


### Defining a new class/object

To define a new class/type of object that has a corresponding database table, we create a new `.rb` file in the `app/models/` folder. To make sure the new class has all the ActiveRecord functionality built-in, we let it inherit from `ActiveRecord::Base`, like so:

```ruby
class Post < ActiveRecord::Base

end
```

*_Note:_* In the real world, you also need to create the relevant table in the database for this to hook up to. For our course, this was already done when we got started. The scope of how to do this is beyond what's covered in this cheat sheet, but if you're interested in learning more, [this tutorial](https://learn.co/lessons/sinatra-activerecord-setup) offers some insight.


### Built-in methods

ActiveRecord provides you with a variety of methods that make it easy to interact with your data in the database.

| Method | Example | Description | Return type |
| ------ | ------- | ----------- | --------- |
| `.find` | `User.find(5)` | Finds the object with the specified ID | Single object |
| `.where` | `User.where(name: 'Matt')` | Finds the object that matches the filters you provided (i.e. where the name is "Matt") | Array of objects |
| `.first` | `User.first` | Gets the first object in the database | Single object |
| `.last` | `User.last` | Gets the last object in the database | Single object |
| `.new` | `User.new(name: 'Matt')` | Creates a new instance of the user class (doesn't save to the database) | Single object |
| `.create` | `User.create(name: 'Matt')` | Creates and *SAVES* a new instance of the user class to the database (you know it's saved because it will have an ID) | Single object |
| `.save` | `User.new(name: 'Matt').save` | Saves your changes to the database | `true`/`false` |



### Defining relationships

In an application with multiple classes/models, you will usually have relationships between them. Consider the example of a `Post` belonging to a `User`. Here is how you would specify those relationships in your classes/models:

```ruby
class User < ActiveRecord::Base
  has_many :posts
end

class Post < ActiveRecord::Base
  belongs_to :user
end
```

Once you have the association setup, you can then easily get a lists of all the posts that a user has created by doing something like this...
```ruby
# Find a user
user = User.find(5)

# Get a list of all the posts by that user
user.posts

# We can also do it the opposite way... start by finding a post
post = Post.find(12)

# What user made this post?
post.user
```


### Model validations

ActiveRecord provides us with convenient ways to add validations to our classes/models. When a validation is in place, a new record in the database cannot be created/edited/saved unless it passes all of our validations! To define a validation, you specify it on the model/class:

```ruby
class User < ActiveRecord::Base

  # Every user must have a name and email
  validates_presence_of :name, :email
  
  # The same email can't belong to multiple users
  validates_uniqueness_of :email

end
```

To check if a particular instance of the `User` class passes validation, you could try creating a new one, then using the `.valid?` method (which returns `true`/`false`). Here is what you might do after someone submits a signup form:

```ruby
# In actions.rb

post '/signup' do

  name = params[:name]
  email = params[:email]
  
  @user = User.new(name: name, email: email)
  
  if @user.save # Calling .save automatically runs validations!
     erb(:signup_success)
   else
     erb(:signup_failed)
   end

end
```

_For a full list of all possible built-in validations, refer to [this guide](http://guides.rubyonrails.org/active_record_validations.html)._


### Updating values

The web isn't static, which necessitates having the ability to edit data after you've saved it to the database! With ActiveRecord, this is super easy! Let's say you wanted to update the name and address for a user in your database. You would start by locating their user ID, open up `bundle exec tux`, and then do the following:

```ruby
user = User.find(5)
user.name = 'New Name'
user.address = 'New Address'
user.save
```


## Git

When performing Git operations, you do them from within the `bash` window. In the majority of cases, when you're done working on the code for a particular set of features, you will do the following:

**Step 1:** Check file status
```
git status
```

**Step 2:** Stage your files (prepare them to be committed)
```
git add .
```

**Step 3:** Commit your changes
```
git commit -m "Description of your changes."
```

**Step 4:** Push your changes to GitHub
```
git push origin/master
```


## Heroku

Details on pushing to Heroku and updating your app with new changes can be found [in this guide](https://gist.github.com/matt297/dfc9a2c7e6c13516a767879f2ceb724e).