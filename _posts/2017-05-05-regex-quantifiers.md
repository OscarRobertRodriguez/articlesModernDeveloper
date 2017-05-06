---
layout: post
title:  "Regex Quantifiers"
categories: jekyll update
---
### Question:
Explain what quantifiers are and describe at least 4 regular expression quantifiers.
<hr>


Quantifiers are symbols that are used to  target a range of matches. The best way to explain this is to just show you. 


## `*` Quantifier 
<br>
The `*` star quantifier is used to match zero or more occurrences of a pattern. 

For example : 

```regex
var pattern /\bbo*\b/;  
```

Here I am saying match any word that begins with `b` and has zero or or more `o`s. So `b`, `bo`, `boo` , `booooooooooooooooooo` would all be valid. 


## `+` Quantifier 

The plus quantifer has to have one match but can have as many afterwards. 

For example : 

```regex
var pattern = /\bboo+\b/; 
```

Here the pattern has to have at least `boo` but can have any of number of o's afterwards so `boooooooooo` is valid. 


## `?` Quantifier 

The question mark quantifer can only have one match or none. 

```regex
var pattern = /(wonder)?\s+woman/;
```

Here we have a pattern that will match `wonder woman` with as many spaces between but there doesn't have to be wonder as it will still match just `woman`.


## `{n}` Quantifer 

This quantifer allows us to specify the character or set it follows n times. 

```regex
var pattern = /^(thunder\s){3}(cats){1}/ 
```


Here we we have a pattern that will match starting with the beginning of a string `thunder thunder thunder cats` with three `thunder` and one `cat`. 



