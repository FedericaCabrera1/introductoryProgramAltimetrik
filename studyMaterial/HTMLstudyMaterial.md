HTML
What is HTML?

HTML stands for Hyper Text Markup Language. 

Hypertext: Hypertext refers to the “text wrapped within a text.” It is very similar to hyperlinks and contains an underlying text that, when clicked, redirects to a new webpage.
Markup language: A markup language is not necessarily a programming language. Instead, it is used to apply formatting and layout to a simple text document. This leads to more interactive and dynamic text content.
It is the standard markup language for creating Web pages. HTML files are plain text files and have an .html extension. They describe the structure of the Web page. HTML elements consist of a set of tags and attributes that will label pieces of the content such as "this is a heading", "this is a paragraph", "this is a link", etc. And therefore tell the browser how to display the content, web browsers receive HTML documents and render it into multimedia web pages. 

Tags: 
Tags are like keywords written between <  > that define how the browser will format and display the content. With the help of tags, the browser can distinguish between HTML content and the document content. 
Tags contain three main parts, opening tag, content and closing tag, however, there are some unclosed tags.

<h1>Título</h1>     
<p>Párrafo</p>  
<br> (unclosed tag)

There are some tags that directly introduce content into the page: <img> or <input>
while others provide information about the document document text: <p>

The browser do not display the HTML tags or content, but use them to interpret the content of the page.

All HTML tags must enclosed within < > these brackets.
Every tag in HTML perform different tasks.
If you have used an open tag <tag>, then you must use a close tag </tag> (except some tags)
Attributes: 
All HTML elements can have attributes, these provide additional information about elements. Attributes are always specified in the start tag, and usually consist in name/value pairs like:
name = “value”
Meta-tags
HTML documents are required to start with a Document Type Declaration, that helps the browser to define the rendering mode  <!DOCTYPE html> defines that this document is an HTML5 document.

The meta elements can be used to include properties of the HTML document, such as author, expiry date, a list of keywords, etc. These have no impact on the physical appearance of the document and go inside the <head> element (where meta information about the HTML page is found).
One or more <meta> tags can be included, based on what information is needed or wanted to include.
The <meta> tag defines metadata about an HTML document, which is additional important information about a document and its data. It is an empty element so it does not have a closing tag, however it carries information within its attributes. 

The viewport: 
It is the user´s visible area of a webpage, which varies with the device. Setting the <meta> element with information about the viewport, will give the browser instructions on how to control the page´s dimensions and scaling. 
So the element:
<meta name="viewport" content="width=device-width, initial-scale=1.0">
should be included in all web pages.

The width=device-width part sets the width of the page to follow the screen-width of the device (which will vary depending on the device).
The initial-scale=1.0 part sets the initial zoom level when the page is first loaded by the browser.
Meta-tag attributes: 

charset: specifies the character encoding for the HTML document.
http-equiv: provides an http header for the information/value of the content attribute.
content: specifies the value associated with the http-equiv or name attribute.
name: specifies a name for the metadata.
it also supports Global Attributes in HTML (are the attributes that can be used with all HTML elements)


An example of a simple HTML document: 

<!DOCTYPE html>
<html> 	//this is the root element of an HTML/XHTML page, every other element will go down
<head>
<meta charset="UTF-8">
<meta name="description" content="Free Web tutorials">
<meta name="keywords" content="HTML, CSS, JavaScript">
<meta name="author" content="John Doe">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Page Title</title>  //specifies a title for the HTML page (which is shown in the browser's title bar or in the page's tab)
</head>
<body>	//element defines the document's body, and is a container for all the visible contents, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.
<h1>My First Heading</h1>
<p>My first paragraph.</p>
</body>
</html>
Input types
An <input> element will directly introduce content into the page, one of the attributes of this element is type it will specify the type of input element that has to be displayed, if this attribute is not specified, the default type is “text”. 

<input type="value">



 Different types of inputs: (possible values of the type attribute)



Differences between HTML and XHTML
XHTML stands for Extensible Hypertext Markup Language. It is almost similar to HTML,  both languages are used for developing web and Android-based applications, but XHTML is stricter than HTML.
The first difference is that XHTML is XML-based, while HTML is SGML-based. Both XML and SGML are markup languages, actually, XML is based on SGML but XML imposes some restrictions that are not in SGML, that's why it is said that XHTML is stricter than HTML. 
Some other differences:
<!DOCTYPE> is mandatory
The xmlns attribute in <html> is mandatory
<html>, <head>, <title>, and <body> are mandatory
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN"
"http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
  <title>Title of document</title>
</head>
<body>
  some content here...
</body>
</html>
Elements must always be properly nested
Elements must always be closed (not unclosed tags)
Not unclosed tags like in HTML, for example: 
<br /> 	or 	<img src="happy.gif" alt="Happy face" />
Elements must always be in lowercase
Attribute names must always be in lowercase
Attribute values must always be quoted
Attribute minimization is forbidden
