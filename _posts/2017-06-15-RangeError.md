---
layout: post
title:  "RangeError"
categories: jekyll update
---
### Question:
Describe the built-in RangeError type and give at least one example in which this error type will be thrown.
<hr>


The RangeError is a incorrect use of a number error for a given property most commonly occurs with Number properties like Number.toFixed(). 


```javascript
 // if i were to do this 
 Number.toFixed(-1);
 // oh oh it throws a rangeError because there can't be any negative number give to this property 
```
