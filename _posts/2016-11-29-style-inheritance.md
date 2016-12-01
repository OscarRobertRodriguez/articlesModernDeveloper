---
layout: post
title:  "CSS Style Inheritance"
categories: jekyll update
---
### Question:
Describe what style inheritance is and use examples to fully describe how it works.


<h1 style="color:#3CCAE6">Rules of Style Inheritance</h1>

Style Inheritance is a common theme when we are dealing with CSS, let's discuss several rules of this everyday concept.

<h2 style="color:#3CCAE6">1. Styles can be inherited from a parent</h2>

Certain styles can be inherited from a parent such as font-family, color, padding, etc. There are styles such as border though that will not be inherited which is good because then we would probably end up with border where we dont want any. Of course we change this by using the `style="border:inherit;"` to allow the paragraph to inherit the border from the parent div. 

<br> Example showing inheritance 
<div style="font-family: sans-serif;border: 1px solid blue; padding: 15px;">



I'm text that's part of the div.
<br>

<p>

This is just an example. See I'm a paragraph that inherited from my parent the div. 
</p>
</div>
Notice how the paragraph doesn't inherit the parents border lets change that.

<br> Example showing paragraph `border:inherit` style
<div style="font-family: sans-serif;border: 1px solid blue; padding: 15px;">



I'm text that's part of the div.
<br>

<p style="border:inherit">

I'm a paragraph and I inherited the divs border property because I was told too or else I wouldn't have done it otherwise.
</p>
</div>

<h2 style="color:#3CCAE6">2. Later styles Rule All</h2>

We have covered this topic before but it is an important concept to be aware of so let's touch on it here. What ever style comes last which means that is read last by the browser that style will be the one that shows up on the webpage. This is the core of style inheritance. 

<style type="text/css">
    #main {
        background: yellow;
    }
    #para {
        background:red;
    }
</style>
<br>Example of Later styles rule
<div id="main">
  I'm part of the body.

    <p id="para">I am a paragraph with a style that came last in the styles so I overrode the other div's yellow background</p>

</div>
<br>

This also applies to stylesheets in the order that you list them in your html header so the last stylesheet will override any styles in previous sheets.

<h2 style="color:#3CCAE6">3.Different sources are allowed for styles</h2>

There can be different sources as we touched upon in our last rule that means as long as later styles don't override previous styles you can have changes coming in various formats such as:

* external stylesheets
* on-page style definitions
* inline styles
* inherited styles from a parent

<h2 style="color:#3CCAE6">4.You can style elements that are nested</h2>

Using this as an example you can see how you can target nested elements with the style 



```css
div div {
 this will target all divs that are nested in another div
}

ul li {
    will target all li element within ul tag
}

li a {
    will target all a tags within li elements
}


```


<h2 style="color:#3CCAE6">5.You can target an element in various ways</h2>

Examples:

```css
.class {
 using a class 
}

#id {
 using an id
}

div {
    using plain html this will target all divs
}
```

This was a quick showing of how you can target elements in ways to style them using ids, classes and plain html or a combination of several. 


<h1 style="color:#3CCAE6">Summary</h1>

These are the main pillars of style inheritance and now you should have a good a idea what the rules are. 
