---
layout: post
title:  "appendChild"
categories: jekyll update
---
### Question:
Explain how the `Node` `appendChild` method works and give at least one example of its usage.
<hr>


The `appendChild` property is used to append an element node to a parent node. 


```javascript
 
 /*
   <ul>
       <li>foo</li>
       <li>bar</li>
       <li>zar</li>
   </ul>
 */

var ul = document.querySelector('ul');
var elem = document.createElement('li');
var text = document.createTextNode('car');

elem.append(text);  // <div>car</div>

 ul.appendChild(elem); 

 /* result

    <ul>
       <li>foo</li>
       <li>bar</li>
       <li>zar</li>
       <li>car</li>
   </ul>

  */

```
