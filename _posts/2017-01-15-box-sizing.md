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

 <h1 style="color:#3CCAE6">Changing the Box Model With Box-Sizing</h1>


The box-sizing property takes two values :

<code>
box-sizing: content-box | border-box; 
</code>

The `content-box` value is the default behavior of an elements height and width. It adds the border and padding to the width and height of the element. As you can see from the example below even though we set the width and height to 300px we now have a div that is far bigger than what we wanted.   

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

Sites started becoming more fluid or as we would say now adays responsive so there needed to be a way to have the width we set to be that actual width. `border-box` to the rescue. Now the border and padding aren't added to the width we set so what width we set is the width we get.  


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

Because box-sizing has become the default way to style most sites there needs to be a way to target all the elements and set them to this border-box sizing.

```css
<!-- this will set all elements to border-box -->
*, *:before, *:after {
  box-sizing: border-box;
}
```






