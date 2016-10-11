---
layout: post
title:  "What's that for: Inline-block"
categories: jekyll update
---

<h1 style="color:#3CCAE6">Question:</h1>
Explain what an HTML `inline-block` element is, give an example of how to make an element `inline-block`. (research question)

<hr>

Before we discuss what `inline-block` means let's talk about the flow in an HTML document in relation to inline and block elements. When we make a web page we have our basic structure like shown below.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <title>Document</title>
</head>
<body>

</body>
</html>
```
Now we might add an `h1` tag and a couple of paragraphs with some links and span tags sprinkled in between the body.

```html
 <h1>Text Site</h1>
    <p>Lorem ipsum dolor sit amet, <img src="#">consectetur adipisicing elit. Odit, ducimus.</p>

    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
    quis nostrud exercitation ullamc<span>o laboris nisi</span> ut aliquip ex ea commodo
    consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
    cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
    proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>

    <p><a href="2016-09-02-Cascade.md">Click Here</a></p>

```

<h1 style="color:#3CCAE6">Block Elements</h1>

Each element has a default display value the `p, div, form, h1-h6` tags display as block elements among others. This means they stack on top of each other in the document - each element on its own line.
However other elements

<img src="../images/block and inline.png" height="300px" style="width: 600px;margin: 0 auto;display: block;">

Every block you see above is a "block" element taking the full width and each on its own line like a stack of blocks. Block element characteristics are as follows :

* Take full width unless a width is set
* Can have margins and padding
* Will expand naturally to let child elements fit unless height is specified
* will be placed below previous elements in the document
* ignores the vertical-align property


<h1 style="color:#3CCAE6">Inline Elements</h1>

Inline elements are the `img,a,span` tag in the example being the most common. Looking at the previous illustration we see that inline elements don't take up the full width and rest inside the p tags flowing with the text.
 Inline elements are the opposite of Block elements in that they don't stack on top of each other including :

* flows with text content
* does not drop to next line
* ignores top and bottom margin settings but can take left and right margins and any padding
* ignores width and height properties
* if floated will become a block element

The difference between block and inline elements is that block builds the structure while inline blocks are more text-based. Now that we got the basics down you might be wondering
where `inline-block` fits in.

<h1 style="color:#3CCAE6">Whats up with Inline-block?</h1>


If an inline and block element had a baby we would get an inline-block. Elements with this box behave as though they were inline but we can set width and height, top and bottom
margins and padding. This can be useful in making navigation bars and creating layouts that you would normally use floats for which we will demonstrate in a moment.

 The way this is achieved is by using the `display` property to change the default box
used with the HTML element. Let's not go in depth with this property but show how we would do this in CSS :

```css
// basic syntax

li {
 display:inline-block;
}
```

<h1 style="color:#3CCAE6">Live By Example</h1>

Let's show the usefulness of this property in building a navigation bar for a website :


<p data-height="265" data-theme-id="0" data-slug-hash="Xjzvxm" data-default-tab="css,result" data-user="nopity"
data-embed-version="2" data-preview="true" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/Xjzvxm/">navbar using Inline-block</a>
by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

The code pen above illustrates the usefulness of `inline-block` instead of the alternative use of floats to create a navigation bar.

<br>
<div class="alert alert-dismissible alert-info">
<button type="button" class="close" data-dismiss="alert">&times;</button>
<strong>Heads up!</strong> <br>Inline blocks are white space dependent so any space between list items will create space between elements. If you need to correct this for a navbar
set the ul element to font size of zero as I did in the codepen above.
</div>
<br>

<h1 style="color:#3CCAE6">Summary</h1>

I have shown you what inline blocks are useful for and shown you how to use them with the `display` property I hope this article clear up any confusion you may have had before.

<br>
<br>









