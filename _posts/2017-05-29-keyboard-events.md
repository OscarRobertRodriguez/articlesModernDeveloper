---
layout: post
title:  "keyBoard Events"
categories: jekyll update
---
### Question:
Describe at least 4 properties on the keyboard event object and explain what they are used for.
<hr>


I will discuss four key event properties. They are `key` , `code`, `location` and the `metaKey`. 


* ## key

The `key` property returns a string of the value you pressed. If you press the 'a' key it will return a. 

<p data-height="451" data-theme-id="0" data-slug-hash="pPXgaq" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="key" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/pPXgaq/">key</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


* ## code 


The `code` property returns a string for what key was pressed it's a bit more specific in terms of what it will return. 


<p data-height="337" data-theme-id="0" data-slug-hash="gWNPZv" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="code" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/gWNPZv/">code</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


* ## location

`location` will return a number based on what area the key in on your input device. 

<p data-height="489" data-theme-id="0" data-slug-hash="gWNrWB" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="location" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/gWNrWB/">location</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

* ## metaKey 


The `metaKey` is used to represent the command key on macs or the windows key on windows. We can use this property when we want to have the user press command and another key.

<p data-height="265" data-theme-id="0" data-slug-hash="GmbqYo" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="metakey" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/GmbqYo/">metakey</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

