---
layout: post
title:  "Character Classes"
categories: jekyll update
---

### Question:
Describe how regular expression range character sets work and give at least one example of their usage.
<hr>



## The lone ranger


In regex we might like to target a range of charaters that are part of a certain family. For example we might want to target all numbers from 1 through 5 without having to type 1,2,3,4,5 out manually. So how do we do this? 

Well we use our `[]` bracket notation with the `-` range charater like so: [1-5]. Now we are targeting all numbers from 1 through 5 with out having to do [1,2,3,4,5] out manually. Now doing this will only match the first number found but we can use a symbol like `+` to match at least one or more matches so [1-5]+  will pick match this string `12345`. If you have a string such as `12349985` then will return `1234` and `5`. 


We can also have other variations such as [a-z] to target all lowercase letters or [A-Za-z]+ to target all lowercase and uppercase letters. We can also negate the values so that we target everything but those values. 

```javascript 
  var pattern = /[^0-9]+/ig; 
  var text = '12super3499girl85'; 
  var matches = text.match(pattern);

 console.log(matches);
 // returns ['super', 'girl']; 
```















