---
layout: post
title:  "range character"
categories: jekyll update
---

### Question:
Explain how the HTML element `children` method works and give an example of its usage.
<hr>


The `children` method will return all child element nodes while `.childNodes` returns all children including text nodes and comment nodes. 


<p data-height="305" data-theme-id="0" data-slug-hash="OgjVqN" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="children compared to childNodes" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/OgjVqN/">children compared to childNodes</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


This difference is a big one also childNodes return a live list while children does not. One of the main ways the children is used is if you want to see how many children are in the body or on some element without having to target the element nodes. 


```javascript

 var childrenOfBody = document.body.children.length; 
 
 // return all children of body not including the text or comment nodes 

```