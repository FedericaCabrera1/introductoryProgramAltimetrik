Data attributes
Data-* attributes are used to store additional information of an HTML element without having to apply non.standard practices. Any attribute with data- is a data-* attribute.

It consist of two parts:
The attribute name should not contain any uppercase letters, and must be at least one character long after the prefix "data-"
The attribute value can be any string
ex. <li data-animal-type="bird">Owl</li>
 It's really helpful because we are able to access these attributes from CSS and Javascript documents. 

How to access data attributes from JS:
1- Using the property dataset it is possible to access the data attribute from its name after the “data-” (important: slashes (-) will be converted to camelCase)
Ex.  (html)                                              (js)








How to access data attributes from CSS:


Can be accessed by the function attr 
Ex. 

Or with the CSS attribute´ selector
Ex.








Data attributes bibliography:
https://www.w3schools.com/tags/att_data-.asp
https://developer.mozilla.org/es/docs/Learn/HTML/Howto/Use_data_attributes

