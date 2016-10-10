---
layout: post
title:  "The document Object"
categories: jekyll update
---

### Question:
Describe the function of the `document` object and use examples to demonstrate its usage.

<hr>

<h1 style="color:#3CCAE6">All about the Document Object</h1>

<blockquote>
  <p>All nodes lead back to the document </p>
  <small>Said by somebody</small>
</blockquote>

<br>

We use the `document` object to reference the document in the browser window. It sits at the top of any DOM tree so this makes it the parent to all nodes. Because of this we can use the `document` object with properties and methods to target any element on a webpage. 

<h1 style="color:#3CCAE6">Live By Example</h1>

There are various methods and properties available to the document object I will go over a few. 

Here is a run down of some example uses :

```javascript
// returns the number of images in the document
document.images.length;

// returns a nodeList of all forms nodes/elements
document.forms[];

/* allows us to target the username field by targeting the element with name="userName" */

document.forms['loginForm'].elements['userName'];

// allows to reference an element by using it's id for reference

document.getElementById("mainHeading");

```

As you can see we use the `document` object frequently in the DOM which befits it since DOM stands for "Document Object Model". This is the peaunt butter and jelly without it we would have a much hard time manipulating the DOM. 

<h1 style="color:#3CCAE6">Summary</h1>

We describe the purpose of the `document` object and while brief surely it has given you a good idea how it is used when going through the DOM. Think of it this way if you need to find something in the DOM always start it with the `document` object just like you always end a sentence with a period. 

<br>
<br>


