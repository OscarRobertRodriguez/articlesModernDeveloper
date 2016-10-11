---
layout: post
title:  "Should I Stay or Should I Go: DOM Insertion/Substraction"
categories: jekyll update
---

### Question:
Explain the different ways of inserting or removing markup into and from the DOM (such as using the `innerHTML` property or the `appendChild` or `removeChild` methods).

<hr>

 <h1 style="color:#3CCAE6">Adding to the DOM</h1>

 Let's first talk about the various ways we can add to our markup. There are various properties that allow us to do this: the `appendChild` and the `innerHTML` but we must also talk about `createElement` and `createTextNode` if we are going to do anything useful with `appendChild`. Let's first talk about the currently discussed method.

 <h2 style="color:#3CCAE6"> The appendChild() Method</h2>  

 Using the appendChild method we can add any element we want to the DOM, we do this using an `onClick` function that will add an item to a shopping cart when we click on it. However to do this we must first create that item and text we would like first. We do this using the `createElement` and `createTextNode`.

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

Finally let's add this li node to the ul element with the id = "shopList". 

```javascript
// Now we have added the li node withe the text to the ul parent
document.getElementById("shopList").appendChild(li_node);
```

This was pretty magical but it leaves alot to be desired, let's add a real working example to show how we could use it in real life. 

