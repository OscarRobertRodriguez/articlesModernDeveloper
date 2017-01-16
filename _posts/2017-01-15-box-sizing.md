---
layout: post
title:  "Changing the Box Model With Box-Sizing"
categories: jekyll update
---

<style> 
.box {
    background-color: green;
    width:300px;
    height:300px;
    margin: 0 auto;
    padding: 40px;
    border:10px solid red;
    display: flex;
    justify-content: center;
    align-items: center;
    box-sizing: content-box;
}

.box p, .box2 p {
    font-size: 30px;
    color: white;
}

.box2 {
    background-color: green;
    width:300px;
    height:300px;
    margin: 0 auto;
    padding: 40px;
    border: 10px solid red;
    box-sizing: border-box;
      display: flex;
    justify-content: center;
    align-items: center;
}
</style>

### Question:
Describe the function of the `box-sizing` property and explain the different values that this property can take and the effect of each of those values.

<hr>

 <h1 style="color:#3CCAE6">What's the function?</h1>


The box-sizing property takes two values :

<code>
box-sizing: content-box | border-box; 
</code>

The `content-box` value is the default behavior of an elements height and width. What this means is that if you add any padding or border that will get added to with width or height expanding the box to a height or width that you didn't want, for example :

```css
 .box {
    width: 300px; 
    height:300px; 
    padding: 20px;
    border: 10px solid red;  
    box-sizing: content-box;
 }
```


<div class="box"><p>content-box</p></div>
<br>

<p>Now normally we wouldn't have to put box-sizing if we were going to use the content-box because this is the default behavior. So because of the additive quality of this property we would get a width of 360px and a height of 330px which makes things more complicated when we want specific sizes.</p> 


```css
 .box2 {
    width: 300px; 
    height:300px; 
    padding: 20px;
    border: 10px solid red;  
    box-sizing: border-box;
 }
```



<div class="box2"><p>border-box</p></div>

<br><br>


With `border-box` we subtract the padding and border from our width and height so we would do 300 - 60 = 240px width and height. 
As you can see we have a huge difference in the widths and heights of the boxes even though we have the same widths and heights set on both, only difference being the box-sizing which makes more sense most of the time the content-box. 


