---
layout: post
title:  "The TypeError"
categories: jekyll update
---
### Question:
Describe the built-in TypeError type and give at least one example in which this error type will be thrown.
<hr>


TypeErrors are usually throw when there is function trying to be invoked on an object that doesn't exist or typos in the code. 

```javascript
 [1,2,3,4,5].speedForce(); 
 // returns VM920:1 Uncaught TypeError: [1,23,34,4].speedforce is not a function
 // 
 [1,2,3,4,5].slices(1); 
  // returns a TypeError also  needs to be slice maybe i'm just hungry 
```

That or misspelling a function method will throw this erorr so don't just know when you see this check your code for misspeling if your software hasn't done it already. 