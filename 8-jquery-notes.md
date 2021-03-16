# jQuery Research Notes

### Topics

1. Introduction to jQuery
2. Getting Started
3. Syntax
4. Selectors Examples

### Introduction to jQuery

* jQuery is a JavaScript library, so it has the .js file extension.
* JavaScript and jQuery can accomplish the same task. 
* However, with jQuery, you can make make code much more shorter and easily readable.
* For Example:

JavaScript:

```javascript
var el = document.getElementById("start");
el.innerHTML = "Go";
```

Versus, jQuery:

```javascript
$("#start").html("Go");
```


* You can download a copy of the jQuery library from www.jquery.com
* You can include jQuery from a CDN (Content Delivery Network), like Google or Microsoft or the official jQuery website:

```javascript
<script src = "https://code.jquery.com/jquery-3.1.1.js"></script>
```

### Getting Started

* Best practice: wait for the HTML document to be loaded before working with jQuery.
* Use the `ready` event of the document object:

```javascript
$(document).ready(function() {
    // ┌───────────────────┐
    // │ jQuery code here  │	
    // └───────────────────┘
})

// This line of code accesses the document object and defines
// a function to be called when the document's ready event is fired.

```

* The `$` is used to access jQuery.
* The code above is very common, therefore, there is a shorthand version:


```javascript
$(function() {
    // ┌───────────────────┐
    // │ jQuery code here  │	
    // └───────────────────┘
})
```

### Syntax

* jQuery is used to select (query) HTML elements and perform "actions" on them.
* Basic syntax is: `$("selector").action()
  1. The `$` accesses jQuery.
  2. The (selector) finds HTML elements.
  3. The action() is then performed on the element(s).

##### Examples:
```javascript
$("p").hide() // hides all <p> elements
$(".demo").hide() // hides all elements with class = "demo"
$("#demo").hide() // hides the element with id="demo"
$("#start").html("Go!"); // Selects element with id start and calls the html() function for it.
// The html function is used to change the HTML content of an element.
```

### Selectors Examples

* jQuery selectors start with the dollar sign and parentheses: `$()`
* Selectors make accessing HTML DOM elements easy compared to pure JavaScript.

```javascript
$("div") // selects all <div> elements
$("#test") // selects the element with the id = "test"
$(".menu") // selects all elements with class = "menu"
$("div.menu") // all <div> elements with class = "menu"
$("p:first") // the first <p> element
$("h1, p") // all <h1> and all <p> elements
$("div p") // all <p> elements that are descendants of a <div> element
$("*") // all elements of the DOM
$("p a") // select all <a> links which are inside paragraph tags.
$("div > *") // select all elements that are children of div
$("h1, h2") // select all h1 and h2 elements
$("#demo p") // select all p elements with the id="demo"
```

##### More Selectors

![useful jquery selectors](assets/useful-selectors-jQuery.png)