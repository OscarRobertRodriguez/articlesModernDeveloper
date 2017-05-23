---
layout: post
title:  "Regular Expression Boundary Matches"
categories: jekyll update
---
### Question:
Describe what regular expression boundary matches are and give detailed explanations of the boundary matches available in JavaScript Regular Expressions.
<hr>



There are several commonly used boundaries used in regex. You can think of them as fences show where a pattern can start searching.  

*  **^**

  This symbol allows us to start searching at the start of an input or the start of the line if the `m` charater is used. 

```javascript
  var pattern = /^cat/;

   'the dogcat and the cat' 
  // will match cat but not the cat in dogcat
```


* **$**

  This symbol allows us to search at the end of a input of line if the `m` character is used.

```javascript
  var pattern = /cat$/;

   'the dogcat and the cat' 
  // will match cat because it is the at the end of the string 

```

 Both these symbols are referred to as anchors and we can use them together to only return a string that has what where looking for.

```javascript
  var pattern = /^cat$/;

   'the dogcat and the cat' 
  // will not return anything as contains more than just cat
  
  'cat'
  // will be a match as it's only cat 
```

* **\b**

This is what we call a word boundary which means a space, tab, caret followed by a word charater will be matched.

```javascript
  var pattern = /\bwonder/g; 

  'wonder wonder whats in a wonder ball'

  //matches all the words that are wonder 
```


* **\B**

This is what we call a non word boundary which means that any character that that is followed by another charter will return a match 

```javascript
  var pattern = /\Bman/; 

  'batman'

  //will match man as it is followed by a character
```


