---
layout: post
title:  "CSS Transitions"
categories: jekyll update
---
<style>
   .square {
    border: 1px solid blue;
    width:100px;
    height: 100px;
    background-color: red;
    transition: border-radius .8s ease; 
   } 

  .square:hover {
    border-radius: 50%;
  }

  .square1 {
    opacity: 1;
    width:100px;
    height: 100px;
    background-color: red;
    transition: opacity;
  }

  .square1:hover {
    opacity:0;
  }
 

.square2 {
    opacity: 1;
    width:100px;
    height: 100px;
    background-color: red;
    transition: opacity 1s;
}


  .square2:hover {
    opacity:0;
  }

.square3 {
    opacity: 1;
    width:100px;
    height: 100px;
    background-color: red;
    transition: opacity 1s ease-in-out;
}


  .square3:hover {
    opacity:0;
  }

  .square4 {
    opacity: 1;
    width:100px;
    height: 100px;
    background-color: red;
    transition: opacity 1s ease-in 1s;
}


  .square4:hover {
    opacity:0;
  }

</style>

### Question:
Explain how CSS transitions work and use examples to demonstrate the different transition properties and their respective values.
<hr>

 <h1 style="color:#3CCAE6">How they work?</h1>


Transitions allow us to give effects to properties over a duration of time so we can get animation without using javascript. This can be used in dropdowns, image galleries to name a few. Let's say we have a square and we want to turn that into a circle on hover, we can do that with a transiton. 


<div class="square"><p style="padding:15px;color:white;">Hover over me</p></div> 




 <h1 style="color:#3CCAE6">Values of Transitons</h1>


 Let's discuss the values that the transiton properties can hold. These include in proper shorthand order and syntax :

<code>
 transiton: transition-property || transiton-duration || transition-timing-function || transition-delay
</code>

From here I will explain each value and as I go show how I will use these properties to build functional transition. 
<br>
 <h3 style="color:#3CCAE6">transition-property</h3>


The opacity in this code is the transition-property value which can be a single value or it can be set to `all` or `none` which would disable the animation.

**Code**

```css
   .square1 {
    opacity:1; 
    border:none;
    width:100px;
    height: 100px;
    background-color: red;
    transition: opacity 1s;
   }

   .square1:hover {
    opacity:0;
   } 
```


**Result**

<div class="square1"><p style="padding:15px;color:white;">Hover over me</p></div> 
<br>
If you hover over the square it disappers but it doesn't really have that animation effect that we desire so this is were we need to add other values to get it there such as transition-duration.
<br>

<h3 style="color:#3CCAE6">transition-duration</h3>

 This value allows us to set a time for the transition to from start to finish. In the previous example we didnt have this value set so it is set to zero and the animation happens instantaneous. The time is written as a number trailed with an s for example `1s` would run the animation for one second. Now let's update the code to add duration. 

**Code**

```css
 .square1 {
    opacity:1; 
    border:none;
    width:100px;
    height: 100px;
    background-color: red;
    transition: opacity 1s;
   }

   .square1:hover {
    opacity:0;
   } 
```

**Result**

<div class="square2"><p style="padding:15px;color:white;">Hover over me</p></div> 

<br>   

Cool now we got it fading out. Next let's implement the transition-timing-function. 

<h3 style="color:#3CCAE6">transition-timing-function</h3>


This property defines the ways an intermediate states of a transition are calculated. This is a bit complex value but the main thing is it makes your transition snappier. The vaules this property can take are :

<code>
ease || linear || ease-in || ease-out || ease-in-out || cubic-bezier(number,number,number,number)
</code>  

Continuing are preivous code let's add an ease-in-out timing-function. It's a little hard to tell it's working but if you compare you will see that it takes a bit longer.

**Code**

```css
 .square1 {
    opacity:1; 
    border:none;
    width:100px;
    height: 100px;
    background-color: red;
    transition: opacity 1s ease-in-out;
   }

   .square1:hover {
    opacity:0;
   } 
```

**Result**

<div class="square3"><p style="padding:15px;color:white;">Hover over me</p></div> 

<br>   

Now let's visit with the last property: the transition-delay. 


<h3 style="color:#3CCAE6">transition-delay</h3>

Creates a delay between when a transition could start and when it actually does. So if we set a delay on our previous example when we hover over the square it will take a second before it starts like so. 


**Code**

```css
 .square4 {
    opacity:1; 
    border:none;
    width:100px;
    height: 100px;
    background-color: red;
    transition: opacity 1s ease-in 1s;
   }

   .square4:hover {
    opacity:0;
   } 
```

**Result** <br>
stay hovered for it to transition
<div class="square4"><p style="padding:15px;color:white;">Hover over me</p></div> 

<br> 

<h1 style="color:#3CCAE6">Summary</h1>

We explained the transition property and how it's other properties can be used in shorthand to create an animation. 

<br><br>