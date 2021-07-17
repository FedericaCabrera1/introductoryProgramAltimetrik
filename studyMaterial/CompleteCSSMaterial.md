CSS:
CSS
What is CSS 
CSS stands for Cascading Style Sheets, it is used to define styles for your web pages, including the design, layout and variations in display. 

It describes how HTML elements are to be displayed. As it was said before, html never intended to contain tags for formatting a web page and it is not semantically correct, so CSS was created.

How to apply CSS to you HTML document
There are three ways:
Inline: By using the style attribute inside the HTML element
Internal: By using a <style> element in the <head> section
Ex. 	<h1 style="color:blue;">A Blue Heading</h1>
<p style="color:red;">A red paragraph.</p>
External: by using a <link> element to link an external CSS file 
Ex.	<link rel="stylesheet" type="text/css" href="css/estilos.css">
The latter is the most common way to add CSS.


CSS syntax 

This language consists of defining rules specifying groups of styles that should be applied to particular elements or groups of elements on the web page. 

The rule opens with a selector that will select the html element/s that we are going to style. 

Selectors: 
By type (HTML tag): h1{ , p{ , etc
If we want to select more than one, we add them separated by a coma: h1, h3, p{
When a tag is inside another tag, we separate them by a space: ul li{
To select every element:  *{
By id: #id{
By class: .class{
When a tag is inside another tag, we separate them 






Once we have selected the element/s, it's time to style them by adding the property and its value:
Some properties: 
font-size: 18px;
background-color: #8A2BE2;
text-align: center;
margin: 5%;
border: 5px;
etc

What is Specificity
If there are two or more conflicting CSS rules that point to the same element, the browser follows some rules to determine which one is more specific and therefore applied. 

Specificity Hierarchy: 

The property applied (if there´s any conflict) will always be the one with the highest hierarchy.

However, if the conflict is between two selectors within the same hierarchy, the property applied will be the one applied later (the one that is lower in the document, by cascading).

If we add !important to a property it will now have the highest hierarchy, however, this is a bad practice and should not be used.







Box Theory
Box Theory is that every HTML element is considered to be wrapped around by a box.

There are two types of boxes:
Block boxes: which wrap the most important HTML elements, these are boxes that form a block, the box adapts to the container's width. (Ex. h2 elements) 
Inline boxes: where the width of the box depends on the width of its content (Ex. b elements)

This means that if you put any element after a <h2> element, it will automatically be shown below it. However, an inline element after a <b> element, will be shown immediately after the b element has ended and can be in the same line.

Box Model
Every box contains 4 main elements:
Content: the content of the box, where text and images appear.
Padding: distance from the content to the border, its transparent space. 
Border: a border that goes around the padding and content.
Margin: distance from the border to the next box. Transparent space.



CSS Layout 
A good layout makes important stuff easily accessible and intuitive to find, making users stay on the site. 
 
Layout is a term that explains how a website is displayed on the screen. Using semantic tags in HTML (block elements that allow information to be grouped) with CSS we will be able to display as we want, these elements throughout the page.

A good layout should consider certain factors as: 
viewing ports
display devices
browsers
user´s screen sizes

The default layout will be the normal flow, one element below the other one, however, with CSS we can arrange the way elements are displayed using the display property. 
CSS Flexbox Layout
Flexbox is a one dimensional layout model that is efficient when aligning, distributing and directing elements in a page. 

The property display: flex; is applied to the container but will affect the items inside it, that will become flex items.

The key terminologies in Flexbox are the main axis and the cross axis. A flex container´s main axis is the primary axis along which these flex items are laid out, and the cross axis is perpendicular to it.

There are some properties that are applied to the container but will affect the items:

flex direction: defines the position of the axises (3 possible values)
the default value, x axis and y axis remain as normal.
column reverse: x axis will now be y axis and y axis will now be x axis
column: x axis will now be y axis and it will go from right to left. And y axis will now be x axis and it will go from top to bottom
flex wrap: 
no wrap: default value, boxes will adapt to the screen´s size
wrap: when screen/window reduces its size, boxes will not reduce it size but will maintain it and if no longer enter in the screen, they will move to the next row below. 
justify content:
space between: will give margin to the items
space around: so there is as much as possible space between boxes
space evenly: it will let the same space between the boxes and between the boxes and the border
align-items:
flex start: default value that puts items from the left 
center: it will center items vertically 
flex end: items will go at the end

Properties applied directly to the items:

align self: same possible values than align items property. To center itself
margin: 
auto: the item will center in the middle of the screen
flex grow: space between boxes will always remain the same (proportions) , even if the screen size is reduced
flex basis: its like the width property, but this one has priority.
flex shrink: allows us to choose how much space a box can loose if the screen size is reduced (if one box has flex shrink: 0, then if the screen size reduced, the other boxes will modify their size while this one will stay the same)
flex: its a shorthand that groups the three last properties (flex grow, basis and shrink) Ex. flex: 1 0 350px;
CSS Grid Layout
Unlike flexbox, grid is a two dimensional layout model (it can handle both rows and columns of the layout). Grid works with a 12-grid arrangement (the screen is invisibly divided into 12 parts.

The property display: gris; is applied to the container but will affect the items inside it, that will become grid items. The default value after applying this property, will create just 1 column (that will act as a block) so to add more cells to the grid we can use the properties: grid-template-rows or grid-template-columns, as explained below.

Properties applied to the container but will affect the items:

grid-template-rows: to add rows	
grid-template-columns: to add columns
Ex.
.grid-container{
	display: grid;
	grid-template-rows: 150px 150px 

grid-gap: (shorthand) it will add something like a margin but between cells grid-gap: 10px;


Properties applied directly to the items:

grid-column: to combine columns, to tell the start and the end of a cell grid-column:1 / 3;
One cell will start in column 1 and end in column 3, the other ones will just keep moving.
grid-row: to combine rows, to tell the start and the end of a cell.




Aligning and flow control properties:

	Added to the GRID CONTAINER:
particular aligning of an item: 
justify-items: this property will center the items horizontally (columns), 
align-items: this property will center the items vertically (rows)
3 possible values for both of them properties:
center: to center the cell content (pic)
start: so items start at the beginning of the page
end: so items end at the end of the page

columns and rows alignments applied to the container: 
Now everything will move as a block
justify-content: to center the container´s columns horizontally.
same 3 values as mentioned above (center, start, end)
align-content: to center the container´s columns vertically. (center, start, end)
Ex. 
.grid-container{
	display: grid;
	justify-content: center;
	align-content: center;
align-items: center;
	justify-items: center;

.grid-item{
	align-items: center;
	justify-items: center;

Added to the GRID ITEM:
align-self: align every item individually (vertically). Values: center, start, end
justify-self: align every item individually (horizontally). Values: center, start, end
place-self: shorthand of the last two properties (align, justify). Ex. place-self: end start;


CSS Methodologies
Using different methodologies we can organize our style sheets in order to achieve a semantic, accessible and easy to maintain code. 

Methodologies such as OOCSS, BEM, SMACSS, can be applied on its own or combined.
OOCSS (Object Oriented CSS)
OOCSS will focus on code reutilization and pattern searching in order to achieve more efficient and easy to maintain style sheets. 

An “Object” in OOCSS can be any repeating visual pattern that can be specified in snippets of code (from buttons, containers, medias, widgets, or even a full page, to any element of our interface that could and should be repeated/ reutilized as many times as necessary).


First rule of OOCSS: Separate the object´s style from its structure

The structure refers to things that are invisible to the user, such as instructions for element size and positioning (height, width, margins, padding, overflow)
And its style refers to the visual properties of elements (colors, fonts, shadows, gradients, etc).
Ex. 

Image 1 does not separates structure from style while image 2 does, where there is not as much repeated text as in image 1.

Second image classes would be added like:






Second rule of OOCSS: Separation of container and content
Styles should never be scoped to particular containers, otherwise could not be reused. Ex. -->


Benefits of OOCSS:
Speed: cutting down on repetitions helps applications run faster. 
Scalability (escalabilidad): as it allows you to freely mix and re-apply classes on different elements, it is easy to reuse things.
Efficiency: having fewer blocks of code makes CSS easier to scan that will facilitate editing and updating.
However there might also be some disadvantages:
Increase number of classes added to an element 
May be overkill for small projects
BEM: (Block Element Modifier)
In order to prevent specification problems, BEM is a naming convention for classes in HTML and CSS.
It consists on choosing a mnemotechnic name for our classes, following some rules:
class = “containerName__elementName”
Ex. 
<div class=”contact-form”>
	<input type=”text class=”contact-form__input”>
<p class=”contact-form__p”>
		<h2 class=”contact-form__p-h2”></h2>
</div>
<div class=”csuscriber-form”>
<p class=”suscriber-form__p”>
		<h2 class=”contact-form__p-h2”></h2>
</div>

SMACSS: (Scalable and Modular Architecture for CSS)
Like OOCSS, the purpose is less code repetition, a more consistent experience, and easier maintenance. 

There are 5 general categories of CSS rules:

Base: The defaults (html, body, h1, ul, etc)
Layout: divide the page into major sections
Module: the reusable modular components of a design
State: these describe how things look when in a particular state (hidden, active, inactive)
Theme: define things like color scheme or typography 

1.Base Rules:
Applied directly to elements through elements selectors, not specific class or ID selectors

2.Layout Rules:
There are major and minor components in every design, a header block would be a major component, while the combination of logo and tagline (lema) within the header, would be a minor component. 
The layout rules of SMACSS apply to major components;

3.Module Rules:
Modules are built around minor page components like navigation bars and widgets. They tend to be inside layout components and even within other modules.
Modules should be designed so they can exist on their own, which gives them greater flexibility in being combined and moved around to different parts of the design without breaking the layout. With modules we do want to avoid IDs and element selectors. More reuse means classes.

4.State Rules:
A state style is one that augments or overrides other styles under given conditions.

Most of us tend to mix styles across all of these categories, creating complexity, instead, applying some guidelines to each will simplify our css.

So a naming convention would help:
Base: nothing needed
Layout: l- or layout- prefixes 
State: is- + state. Ex. is-active 
Module: just use module name 


Media queries
With the @media rule, we can include a block of CSS properties if a certain condition is true. Adding a Breakppint, certain parts of the design will behave differently on each side of the breakpoint. Ex. 
@media screen and (max-width: 700px){
	.nav{
		width:100%;
		height:60%;
	}
	.section{
		width:100%;
		height:50%;
	}
}
When the width of the screen is bigger than 700px, it will act as normal, but when it is smaller than 700px, it will acquire the conditions i´ve put below the @media rule.

The question now is which unit to use for breakpoints? 
Using em media queries, your web page will be able to adapt even if the user had changed the font size on their screen, as the em will adapt to it. However, using px media queries, if the user has changed its font size, the breakpoint will remain the same, even though a bigger font size will require a bigger container.
So in conclusion, when using the em media query, the breakpoint will adapt to the conditions set by the user, so if the font size is bigger, the the viewport will need to adapt sooner than if it was normal, meaning that someone on a tablet might see the mobile layout.



jQuery: 
It is a Java Script´s library, a collection of tools that allow us to implement functionalities or effects, without the need of writing all the code that would be really needed to do it. 
It has an API that we can use to access its functionalities. (https://api.jquery.com/) 

Basic concept of jQuery is to “select some elements and do something with them” 

Selecting elements: jQuery supports most CSS selectors and others;
$( "#byId" );
$( ".byClass" );
$( "input[name='first_name']" ); By attribute
$( "#contents ul.people li" ); By compound CSS selector (when a tag is inside another, like ul li)
$( "div.myClass, ul.people" ); By a comma separated list of selectors (separating with a comma you can include plenty of CSS selectors)

Pseudo selectors:
Ex. 
$( "#myForm :input" );  Select all input-like elements in a form with that id
$( "form :checked" );  “checked” not only for checkboxes but also for radio buttons. use “selected” only for <select> elements 
etc. 

Bootstrap: 
Link to bootstrap webpage (with info about each tool bootstrap offers) →
https://getbootstrap.com/docs/5.0/layout/breakpoints/

It is a framework that enables developers and designers to quickly build fully responsive websites. It includes HTML and CSS based design templates for forms, buttons, tables, etcc. It also includes user interface components, layouts and JS tools.

Adding the following link to our HTML document
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">


Materialize: 
A responsive front-end framework similar to Bootstrap. Materialize CSS is based off Google´s material design.
Link to materialize webpage (with info about each tool materialize offers) →
https://materializecss.com/getting-started.html

CSS Preprocessors: 
A CSS preprocessor is a scripting language that extends CSS, basically you write CSS in a slightly different form (another language but so similar to CSS) and then compile it and get standard CSS code.
Preprocessors allow us to use logic in our CSS code, such as variables, nesting, inheritance, functions, etc. It make it easy to automate repetitive tasks, reduce the number of errors and code bloat, create reusable code snippets, etc.
There are plenty of CSS preprocessors, the oldest one is SASS.
SASS (Syntactically Awesome Style Sheet): 
Allows frontend developers to use logic in their CSS code;
Variables: 
variables as a way to store information that is going to be reused, like colors, etc. Sass uses $ symbol to make sth a variable. Ex. 

Sass.
$font-stack:    Helvetica, sans-serif
$primary-color: #333

body
  font: 100% $font-stack
  color: $primary-color


Css.
body {
  font: 100% Helvetica, sans-serif;
  color: #333;
}

Nesting:
Sass will let you nest your CSS selectors in a way that follows the same visual hierarchy of your HTML. Ex.

Sass.
nav
  ul
    margin: 0
    padding: 0
    list-style: none

  li
    display: inline-block

  a
    display: block
    padding: 6px 12px
    text-decoration: none
Css.
nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
nav li {
  display: inline-block;
}
nav a {
  display: block;
  padding: 6px 12px;
  text-decoration: none;
}


Partials:
You can create partial Sass files that contain little snippets of CSS that you can include in others Sass files. Usually named like _partial.scss and used with the @use rule 
Modules:
You don't have to write all your Sass in a single file, you can split it up and use the @use rule. This rule will load another Sass file as a Module, which means you can refer to its variables, mixins and functions in your Sass file. Ex. 

Sass. 
// _base.sass
$font-stack:    Helvetica, sans-serif
$primary-color: #333

body
  font: 100% $font-stack
  color: $primary-color
Css. 
// styles.sass
@use 'base'

.inverse
  background-color: base.$primary-color
  color: white

Mixins:
A mixin lets you make groups of CSS declarations that you want to reuse throughout your site. 
To create a mixin, use the @mixin directive and give it a name, then you can use it as a CSS declaration starting with @include followed by the name of the mixin. Ex. 

Sass. 
@mixin theme($theme: DarkGray)
  background: $theme
  box-shadow: 0 0 1px rgba($theme, .25)
  color: #fff


.info
  @include theme

.alert
  @include theme($theme: DarkRed)

.success
  @include theme($theme: DarkGreen)





Css. 
.info {
  background: DarkGray;
  box-shadow: 0 0 1px rgba(169, 169, 169, 0.25);
  color: #fff;
}

.alert {
  background: DarkRed;
  box-shadow: 0 0 1px rgba(139, 0, 0, 0.25);
  color: #fff;
}

.success {
  background: DarkGreen;
  box-shadow: 0 0 1px rgba(0, 100, 0, 0.25);
  color: #fff;
}


Extend/Inheritance:
Using @extend lets you share a set of CSS properties from one selector to another. Ex.

Sass.
/* This CSS will print because %message-shared is extended. */
%message-shared
  border: 1px solid #ccc
  padding: 10px
  color: #333
.message
  @extend %message-shared

.success
  @extend %message-shared
  border-color: green

.error
  @extend %message-shared
  border-color: red

.warning
  @extend %message-shared
  border-color: yellow
Css.
/* This CSS will print because %message-shared is extended. */
.message, .success, .error, .warning {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.success {
  border-color: green;
}

.error {
  border-color: red;
}

.warning {
  border-color: yellow;


You create a block of properties and then apply it to different selectors, so you don't have to write it that many times.
Operators:
Sass has a handful of standard math operators. Ex. Take pixel values and convert them to percentages.


Sass.
.container
  width: 100%

article[role="main"]
  float: left
  width: 600px / 960px * 100%

aside[role="complementary"]
  float: right
  width: 300px / 960px * 100%


 Css.
.container {
  width: 100%;
}
article[role="main"] {
  float: left;
  width: 62.5%;
}
aside[role="complementary"] {
  float: right;
  width: 31.25%;
}
