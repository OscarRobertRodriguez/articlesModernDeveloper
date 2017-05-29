---
layout: post
title:  "Regular Expression Exact Matches"
categories: jekyll update
---
### Question:
Explain what regular expression exact matches are, and give at least one example of their usage.
<hr>


An exact match is when we want to find a specific string with no variations or execeptions to what is allowed. So were looking for a specific string and not a pattern in this case. 


```javascript
  var pattern = /The Flash/;

  /* who is The Flash? */

  /* will return a match because it reads from left to right if the question mark was in the front it would not return a match */
```