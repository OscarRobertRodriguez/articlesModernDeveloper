---
layout: post
title:  "Media Queries"
categories: jekyll update
---

### Question:
Define media queries and describe the different kinds of media queries that exist. Give code samples of each kind of media query.

<hr>

 <h1 style="color:#3CCAE6">Media queries?</h1>

Media queries are like that sign you see at a carnival that says you have to be this tall for this ride. If your too short then you can't ride and will go find something else to ride. With media queries, we can apply the same logic in that if the page is not a certain width or type the style will not be applied. 

So basically they are if statements which result in a true or false value and based on this value the code either will be applied or not within its brackets. Media queries are mostly used for responsive web design to get a page to change its layout based on its size. 

There are two ways we can write a media query: in the header of the HTML document or in the CSS document.

<strong>Link Element query:</strong>

```html 
<!-- CSS media query on a link element -->
<link rel="stylesheet" media="screen and (min-width: 480px)" href="example.css">
```


<strong>Stylesheet query:</strong> 

```html 
<!-- Css media query within a stylesheet -->
@media screen and (min-width: 480px) {
    body {
        background-color: lightgreen; 
    }
}
```

You might be wondering what does the `screen` do so let's dive into that.

 <h2 style="color:#3CCAE6">Types of Media Queries</h2>


 There are different types of media queries that are used to give us another way to only an applied style to that type. For example, we can say : 

```css
 @media print {
     <!-- code goes here -->
 }
```
The above code will apply specified styling when we print the page this might include removing all images such as ads.

The types as oinclude:

* **screen** - Used for computer screens, tablets, smart-phones etc. 
* **speech** - Used for screenreaders
* **all**  - Used for all media type devices
* **print** - Used for printers 


 <h2 style="color:#3CCAE6">Logical Operators</h2>

 In JavaScript, we use logical operators and we also use them in media queries with some difference. They are `and`, `only`, `not`, `or`. From the previous example we used, we can see that we used `and`. They allow us to apply more than one statement that must evaluate to true for the inner block to run.

 * **and** - will evaluate all multiple statements must all be true to run 
    Example:<br> 

```css
@media print and (min-width: 800px) and (orientation: landscape) {
<!-- code here -->
}
```

* **or** - creates two different media queries that are treated separately  
    Example:<br> 

```css
@media (max-width: 600px), (min-width: 800px) {
html {background-color: red;}
} 
```

* **only** - used to prevent non-supporting browsers to not load the stylesheet but usefulness is questionable will most likely be deprecated.

* **not** - it might not always make the most sense to use this logically but just like we would use `not` in JavaScript if it's not those statements then it will run that code block.2016-09-02-Cascade.md

```css
@media not all and (max-width: 600px) {  /* code will run if width is greater than 600px */
    html { background-color: red; }
}
``` 

 <h2 style="color:#3CCAE6">Ordering Queries</h2>

 When using queries most likely you need more than one as you need to cover all screen sizes. Well, you can by adding multiple queries but start with the low numbers first when dealing with width or other number values to create more order to code. 

```css
@media (max-width: 400px) {
    html { background:red; }
}
@media (min-width: 401px) and (max-width: 800px) {
    html { background: green; }
}
@media (min-width:801px) {
    html { background: blue; }
}
```

Overriding media queries can also be done but they must be in the correct order for it to work properly from low to high. This may be preferred in some cases as you have to write less code.  

```css
@media (min-width: 400px) {
    html {background: red; }
}
@media (min-width: 600px) {
    html {background: green; }
}
@media (min-width: 800px) {
    html {background: blue; }
}
```

We could also develop a mobile query first it would look like this: 

```css
html {background: red; } /* this is the mobile code */

@media (min-width:600px) {       /* as the screen get larger we use are media query code */
    html { background: green; }
}
```

It would be the same if your doing desktop first, all you need to do is change min to max width. 




 <h2 style="color:#3CCAE6">Live By The Code</h2>


This code won't work correctly as an embed so click on edit on code pen, then resize the browser window to see the color changes. This is a basic sample but all CSS can be used to give the whole site a different look based on width. 

 <p data-height="290" data-theme-id="0" data-slug-hash="wzVLqp" data-default-tab="css,result" data-user="nopity" data-embed-version="2" data-pen-title="Media Queries" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/wzVLqp/">Media Queries</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

 <h2 style="color:#3CCAE6">Summary</h2>
This was a quick overview of media quieres but I hope it has made your understanding a bit clearer.