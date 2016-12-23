---
layout: post
title:  "Meter and Progress Tags"
categories: jekyll update
---
### Question:
Describe the function of the `meter` and `progress` tags and give an example usage of each of these tags.


<h1 style="color:#3CCAE6">Meter tag</h1>

The first tag we will talk about is the meter tag which is used for things such as disk space taken and battery bar, not to get confused with progess bars for that we will use `<progress>` tag. Below are some examples:

* meter tag  without any attributes:

```html
<meter></meter>
```

<meter></meter> 
<br>

* meter tag  without any attributes:

```html
<!-- the value attribute sets how much bar is filled -->
<meter min="0" max="100" value="50">50% power</meter>
```

<meter min="0" max="100" value="50"></meter>

* meter tag  without any attributes:

```html
<!-- The low and high attributes change the color of bar if value is lower or higher -->
<meter min="0" max="100" value="40" low="50" high="90">50% power</meter>
```

<meter min="0" max="100" value="40" low="50" high="90"> low value</meter>

<h1 style="color:#3CCAE6">Progress</h1>

The progress tag looks different from the meter tag and also has a different purpose. The tag is used to show the percentage of task is completed like this:<br><br>
**80%:**
<progress value="80" max="100"></progress> 

Of course we would use javascript if we were going to use it in an application to get the progress bar to adjust values. 

<br><br>