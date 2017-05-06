---
layout: post
title:  "The Structure of JSON Documents"
categories: jekyll update
---
### Question:
Explain what constitutes a valid JSON document and list all of the data types allowed in JSON.
<hr>


JSON is related to JavaScript but differs in that JSON is a data format and JavaScript is a programming language. So what can we use in JSON for it to be valid. 


## Simple Values 

JSON supports the use of simple values such as strings, numbers, null, boolean values, objects and arrays. 

Let's discuss the proper format for JSON using simple values in a example. 


We can start a JSON file with an array or an object but for our example we will start with an object. 


```json
{
    "firstname": "oscar",
    "lastname": "awesome",
    "age": 30
}
```

Compared with JavaScript we can see differences already, can you spot them? With JavaScript the property names don't have quotation marks around them. Also we dont use variables, methods or functions in JSON like we do in JavaScript. 

We can make objects in JSON as complex as we want too. 

```json
{
    "firstname": "oscar",
    "lastname": "awesome",
    "age": 30,
    "address": {
        "street": "401 Summerstreet",
        "city": "Boston",
        "state": "Texas"
    }
}
```


We can also use arrays within objects or put objects within an array. 


```json
{
    "firstname": "oscar",
    "lastname": "awesome",
    "age": 30,
    "address": {
        "street": "401 Summerstreet",
        "city": "Boston",
        "state": "Texas"
    },
    "pets": ["dog", "cat", "snake", "gold fish"]
}
```



