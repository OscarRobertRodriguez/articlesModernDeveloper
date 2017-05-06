---
layout: post
title:  "Character Classes"
categories: jekyll update
---

### Question:
Describe what character are and list and explain the different character classes available.
<hr>


A character class is a list of characters that can be matched. This list is created by using `[]` brackets. For example :

```regex
var pattern = /[abc]/;
```

This will match any `a`, `b` or `c` character within a string. We can also specify a range let's say we wanted to only target letter from a to q we can do that easily with a character class. 

```regex
var pattern = /[a-q]/; 
```

There thats all it takes.

Within a character class the `^` takes on a new meaning. It negates so 

```regex
var patter = /[^a-q]/; 
```

means to target match every thing except the letter between a-q. 

The `$` symbol within a character class loses its special powers with a character class and just refers to the `$` symbol itself.


## Special character classes

These aren't really special but there used so much that they have been given there own values. 

For example  we usually want to target all digits we can do that with just this. 

```regex
var pattern = /\d/;
```

That will target any digit it's the same thing as writing `[0-9]`. 

There is also the `\s` which matches any horizontal tab, newline, form feed, carrriage return, and the space. So basically this `[\t\n\f\r]`. 

There are many more of these characters that do something similar so I won't discuss them here. I hope this has helped you. 







