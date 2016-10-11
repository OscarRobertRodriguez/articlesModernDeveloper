---
layout: post
title:  "Selectors API"
categories: jekyll update
---

### Question:
Describe the Selectors API and demonstrate the use of the two methods available in this API, `querySelector` and `querySelectorAll`.

<hr>

 <h1 style="color:#3CCAE6">What's that: Selectors API</h1>

 The Selectors <abbr title="Application Program Interface">API</abbr> is an extension to the DOM that allows us to select references using CSS selectors instead of having to rely on HTML markup. So instead of having of having to use `getElementById()` or `childNodes` we can traverse the DOM with more efficient CSS selectors.

 Often as developers we want to simply say "give me all elements that match this selector" or "give me the first element that matches this selector" and that's exactly what `querySelector` and `querySelectorAll` do for us. Let's talk about these selectors now. 

  <h1 style="color:#3CCAE6">querySelector</h1>

  The `querySelector` allows us to enter find a single element- returning the first element that meets the criteria. We either give it an id,class name or even the element itself. If not put incorrectly we will get an error and if it does not exit in the document we will get an error. 

```javascript
// returns the first span
var span = document.querySelector("span");

// returns element with the id = "fixedNav" (should only have one in document for ids)
var nav = document.querySelector("#fixedNav")

// returns the first element with class with class = "price" (can be more than one)

var price = document.querySelector(".price");

// returns the first span tag with the class = "price"

var span_price = document.querySelector("span.price");
```


   <h1 style="color:#3CCAE6">querySelectorAll</h1>

Now you might be wondering well you know I'd like to select all of a certain class or element at once and that's where the `querySelectorAll` comes in. We can target all elements in a document but it proves useful when we want to target all the elements within a particular parent elements.

```javascript
// selects all li elements in the HTML document
document.querySelectorAll("li");

// selects all the p tags with parent with the id="mainHeading"
document.querySelectorAll("#mainHeading p")
```

These are a few ways that these selectors can be used, check out the code pen below to see these selectors in action. 


<h1 style="color:#3CCAE6">Live By The Code</h1>


<p data-height="333" data-theme-id="0" data-slug-hash="dpZPLo" data-default-tab="js,result" data-user="nopity" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/dpZPLo/">Selectors API</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

   <br>

   <h1 style="color:#3CCAE6">Summary</h1>

   I hope now you have a good reference to come back to if you are having trouble using these methods or would like a quick refresher. We covered the  `querySelector` and `querySelectorAll`. We went over what the Selector API does, how it's a component defined by the W3C but will become part of the DOM 4 eventually so we will eventually lose the Selector API term. 

   <br>