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







BEM Methodology: (Block Element Modifier)
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

