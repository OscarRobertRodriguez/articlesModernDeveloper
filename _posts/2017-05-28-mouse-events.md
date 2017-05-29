---
layout: post
title:  "Mouse Events"
categories: jekyll update
---
### Question:
Describe at least 4 properties on the mouse event object and explain what they are used for.
<hr>



Let's talk about four mouse events that I would like to explain in more detail. I will talk about the `click`, `mouseover`, `mouseout` and `mouseup`.



* ## click 

The `click` event does what you expect it fires the event listener on a mouse click . Let's show this. 



<p data-height="376" data-theme-id="0" data-slug-hash="BRgaYz" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="click" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/BRgaYz/">click</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


We used the click listener on the div and as you can see changed the text. 


* ## mouseover


The mouseover activate when you role your mouse over a target element.

<p data-height="265" data-theme-id="0" data-slug-hash="Wjqbvd" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="Wjqbvd" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/Wjqbvd/">Wjqbvd</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

Also in this example I included `mouseout` which is a bit different than `mouseleave` in that it only activates when you leave the container that holdes it's decendants but in this case we have made it work like mouseleave. 


* ## mouseout

 see above 


* mouseup 

The mouseup has special use cases. It doesn't need the default mouse button to fired(you can use the scroll will held down) and you can hold your click on a different part of the page and let it go over the target and it will work.

<p data-height="265" data-theme-id="0" data-slug-hash="ZKdYxN" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="mouseup" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/ZKdYxN/">mouseup</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


