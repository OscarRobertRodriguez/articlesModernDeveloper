---
layout: post
title:  "Mixins with Sass"
categories: jekyll update
---
### Question:
Describe what Sass mixins are and use code samples to demonstrate how they work.

<hr>

 <h1 style="color:#3CCAE6">Mixins</h1>

Mixins are like functions for our code base that allow us to have predefined styles that we can plug in where we need them so we don't have to write `width` or `height` a thousand times. 

Every mixin begins with `@mixin` and the name of that mixin, similar to how we would name a function. 


```scss
 @mixin size 
```


We will call this the size mixin but we need to give it some properites so that it can do something. 


```scss
@mixin size {
    width: 100%;
    height: 100%;
}
```


Now we can do this when we want to use it. 

```scss
@mixin size {
    width: 100%;
    height: 100%;
}


.example {
    @include size; 
}


<!-- complies too -->

.example {
    width: 100%;
    height: 100%;
}

```


 <h2 style="color:#3CCAE6">Mixin parameter</h2>

 The above `@mixin` mixin works but it's not very flexible. Lets say we want to use pixles or we just want different percentage values well we're out of luck. But have no fear parameters to the rescue. 

 
```scss

 @mixin size ($width, $height: $width) {
    width: $width;
    height: $height;
 }
```

Now when we set a width for parameter it will add the height for us but we can override that if we want too. For example :


```scss 

// excluding height
.example {
    @include size(100%);
}

// including height

.example {
    @include size(100%, 500px);
}


<!-- compiles too -->

.example {
    width: 100%;
    height: 100%;
}


.example {
    width: 100%;
    height: 500px;
}

```


 <h1 style="color:#3CCAE6">Summary</h1>

 If you didn't know about mixins before maybe now you will see the benefits to using them in your code. Adios. 

