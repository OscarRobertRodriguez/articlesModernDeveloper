---
layout: post
title:  "Audio and Video Tags"
categories: jekyll update
---

### Question:
Describe the `audio` and `video` tags and how they enhance the user experience. Provide examples of their usages.

<hr>

 <h1 style="color:#3CCAE6">Audio tag</h1>

 Audio can add depth to a site by giving the user an experience more aligned with our media center world nowadays with some notable examples such as Pandora, for our purposes our examples will be much simple.

 <audio src="https://www.dropbox.com/s/1vsvv1gwm8sxstr/butthead.mp3?dl=0" controls="controls" >
 </audio> 

 <h2 style="color:#3CCAE6"> The appendChild() Method</h2>  

 Using the appendChild method we can add any element we want to the DOM, we do this using an `onClick` function that will add an item to a shopping cart when we click on it. However, to do this we must first create that item and text we would like first. We do this using the `createElement` and `createTextNode`.

```javascript
// creates a li element node
var li_node = document.createElement("li");

// creates a text node 
var text_node = document.createTextNode("WaterMelon $50")
```

 Now that we have created are list element and text we can use the appendChild to add the text to the li element. 

```javascript
// the text gets added to the list node
li_node.appendChild(text_node);
```

Finally, let's add this li node to the ul element with the id = "shopList". 

```javascript
// Now we have added the li node withe the text to the ul parent
document.getElementById("shopList").appendChild(li_node);
```

This was pretty magical but it leaves a lot to be desired, let's add a real working example to show how we could use it in real life. 


<p data-height="265" data-theme-id="0" data-slug-hash="JRvKVk" data-default-tab="js,result" data-user="nopity" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/JRvKVk/">shopping Cart</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

It's a simple example but shows how all the pieces come together. 


<h2 style="color:#3CCAE6"> The innerHTML Method</h2>  

The innerHTML method allows us to read the contents of what's in between an element tag and we can change the contents by using this property. 

```javascript
var domLevels = document.querySelector("#List")

// read- mode
output_before = domLevels.innerHTML;

// write mode 
 domLevels.innerHTML = "<li>Yes its a lovely day</li>"
```

Here we show the different modes. The read mode output may look similar to the write mode but keep in mind it doesn't change the content of the element it just returns that content. 

<br>

 <h1 style="color:#3CCAE6">Removing from the DOM</h1>

 There is one method that is used mostly to remove markup:

  <h2 style="color:#3CCAE6"> The removeChild() Method</h2> 

Using this we can remove children element say from a list or a paragraph. The syntax for this is similar to the `appendChild` method used earlier.
