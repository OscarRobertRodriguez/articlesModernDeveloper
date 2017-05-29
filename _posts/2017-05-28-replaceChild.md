---
layout: post
title:  "replaceChild"
categories: jekyll update
---
### Question:
Explain how the `Node` `replaceChild` method works and give at least one example of its usage.
<hr>


The `replaceChild` will replace an element with another element we specify. 

```javascript
 replaceChild(newElement, TargetElement);
```

We give it the newElement and the TargetElement. We can replace text and element nodes with this property. Let me show you an example of both. 

```javascript
/*  
<!DOCTYPE html>
<html>
<head>
    <title>replace text & elem node</title>
</head>
<body>
  
  <div id="A">Hi</div>
  <div id="B">Dragon</div>

</body>
</html>
*/


  //replace element node
var divA = document.getElementById('A');
var newSpan = document.createElement('span');
newSpan.textContent = 'whats up';
divA.parentNode.replaceChild(newSpan,divA); 


  //replace text node

 var divB = document.getElementById('B').firstChild;
 var newText = document.createTextNode('buddy');
 divB.parentNode.replaceChild(newText, divB); 


```


I hope this has made this easier to understand the `replaceChild` node method. 
