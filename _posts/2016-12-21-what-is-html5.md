---
layout: post
title:  "What is HTML5?"
categories: jekyll update
---
### Question:
Explain what HTML5 is. List and describe some of its features.


<h1 style="color:#3CCAE6">HTML5</h1>

The new kid on the block is HTML5 and its also has some pretty cool trick up its sleeve. Before, web developers would use divs to group content which although it worked left the code broken semantically. 

Newly introduced tags for more semantic markup include :

* **header** - used for title or logo of a page
* **footer** - holds copyright, nav links in footer of page or article
* **nav** - for navigation of site
* **section** - used to group content with a similar theme
* **article** - stand alone content usually within a section tag 
* **aside** - standalone information usually to the side of 


<p data-height="947" data-theme-id="0" data-slug-hash="aBXPyB" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="semantic" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/aBXPyB/">semantic</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<h1 style="color:#3CCAE6">But wait there's some more cool tags</h1>

There was a lot of other tags added also I will list some :

* **audio** - used to play audio
* **video** - for videos
* **canvas** - used for graphics 
* **svg** - used for graphics also but has scaling advantage
* **figure** - used for images 
* **figcaption** - used for displaying title below image 


Let's look at the last two as there too many to go over but I will explain the figcaption and figure in detail. 

These two tags are a pair we use them together to get more information from a photo, keeping it semantically in detail.

```html 
<figure>
  <img src="" alt="My cat" />
  <figcaption>
    <span>Success!</span>
  </figcaption>
</figure>
```


<figure style="margin: 0 auto; width:400px;">
  <img src="http://s2.quickmeme.com/img/ea/eaa7c1421e50bdc599027acc0c62089ec9fb5b9e1695878eadc29c3244dfb4db.jpg" alt="My cat" style="width: 300px;height: 300px" />
  <figcaption>
    <span style="margin-left: 100px;"><strong>Success!</strong></span>
  </figcaption>
</figure>

<br>
<br>

As we can see we have confirmation on how these tags work and that's a nice photo too. 

<h1 style="color:#3CCAE6">Summary</h1>

That was a quick walk through of HTML5, and I wonder what HTML6 will add but we will have to wait awhile for that. 