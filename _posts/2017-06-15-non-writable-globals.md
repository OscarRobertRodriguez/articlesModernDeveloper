---
layout: post
title:  "Non-writable Global with Strict Mode"
categories: jekyll update
---
### Question:
Explain what non-writable globals are and describe how they behave in relation to assignment in strict mode.
<hr>


A non-writable Global is a property or value in JavaScript that can't be overwritten for example take `Infinity`. We can't say `Infinity = 1` because it's nonwritable. In non strict mode there is no error thrown, we have to look through the code and take longer to debug it. 

With strict mode enabled though if we try to do this we get a TypeError returned  which is a good reason you should be using strict mode were it makes sense too as it will save you time. 

```javascript
 // non strict mode 
  Infinity = -5;  // no error is returned but our code doesn't work 


// strict mode 
 Infinity = -5; // throws a TypeError     
```