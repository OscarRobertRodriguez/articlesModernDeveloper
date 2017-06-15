---
layout: post
title:  "getElementsByClassName"
categories: jekyll update
---
### Question:
Explain how the `document` `getElementsByClassName` method works and give an example of its usage.
<hr>



`getElementsByClassName` targets all the classes in the document and returns a live HtmlCollection list which is like an array but isn't able to use it's prototype methods like `slice` etc.


<p data-height="365" data-theme-id="0" data-slug-hash="rwWydq" data-default-tab="js" data-user="nopity" data-embed-version="2" data-pen-title="getElementsByClassName" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/rwWydq/">getElementsByClassName</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>



You can also chain commands to get classes from only certain sections like so. 

```javascript
var items = document.getElementsById('main').getElementsByClassName('items'); 
// this will get all class items that are children of the element with the id of main 
```

Or we can do something like this. 

```javascript
 var 2OfaKind = document.getElementsByClassName('alert green'); 
 // will collect all element that have both classes of alert and green 
```

