---
layout: post
title:  "non-configurable property"
categories: jekyll update
---

### Question:
Explain what a non-deletable or non-configurable property is and describe how it behaves in strict mode when a deletion is attempted on it.
<hr>


A non-deletable/non-configurable property is a property that the user defines as false for configurable or that is built into the javascript language and cannot be deleted. 


```javascript

var person1 = {
    name: 'Oscar';
}


 Object.defineProperty(person1, 'name', {
    configurable: false
    })
// now we cant change name 
 
  person1.name = 'jonh'; 
  // if in strict mode will throw an error 
  
  console.log(person1);  // returns Oscar 

```


Or when we try to delete a property that is set to non-configurable by default. 

```javascript
 
 delete Math.PI; 

 returns error in strict mode  

```
 