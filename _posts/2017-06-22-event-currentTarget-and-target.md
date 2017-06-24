---
layout: post
title:  "currentTarget and target"
categories: jekyll update
---

### Question:
The Event object has two properties called `currentTarget` and `target`. Explain the function of these properties and give one example of their usage and explain the difference between the two.
<hr>


The `currentTarget` is the element you actually bound the event too this will never change where as the `target` is the element that was actually clicked on for example : 


<p data-height="265" data-theme-id="0" data-slug-hash="zzdRdP" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="currentTarget vs target" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/zzdRdP/">currentTarget vs target</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>



In this example we make the whole list the currentTarget which is the element that the Event was added too. With the `target` we can get all the list items on click even though though they don't have the event applied to them. This is known as event delegation and is made possible in part due to the target elements.  