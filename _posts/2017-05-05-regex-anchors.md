---
layout: post
title:  "Regex Quantifiers"
categories: jekyll update
---
### Question:
Explain what regular expression anchors are and give at least two examples of their usage.
<hr>



Anchors are used to match positions of characters so that we only make sure a string has only what we want. 


For example the `^` can be put in front of a word and ending with the `$`. 
what this does is only match a string with the value of `super` any thing else in the string won't pass. 

```regex
var pattern = /^super$/; 
```


There are other anchors that we can use such as the word boundary character `\b`. This means that where ever there is a space start counting there if afterwards there is a character. 

```regex
var pattern = /\bwonder/; 
```

This will match `wonder` if it has no letters before it but a just a space. This is useful were we have a large amount of text but just want to find word that are `wonder`. 