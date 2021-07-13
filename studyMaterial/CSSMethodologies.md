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
