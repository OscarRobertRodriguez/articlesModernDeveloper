---
layout: post
title:  "hasChildNodes"
categories: jekyll update
---
### Question:
Explain how the `Node` `appendChild` method works and give at least one example of its usage.
<hr>


The `hasChildNodes` property is used to see if an element has children nodes it will return a boolean value. 

```javascript
 
 /*
   <ul>
       <li></li>
       <li></li>
       <li></li>
   </ul>

  */
 
  var ul = document.querySelector('ul');

  console.log(ul.hasChildNodes());  
  // returns true 
```
