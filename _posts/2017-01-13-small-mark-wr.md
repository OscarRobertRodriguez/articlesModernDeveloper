---
layout: post
title:  "What's small, mark and wbr?"
categories: jekyll update
---
### Question:
Describe the function of the `small`, `mark`, and `wbr` tags and give an example usage of each of these tags.
<hr>

 <h1 style="color:#3CCAE6">The `small` tag</h1>

The small tag makes the font size one size smaller it is usually used for side comments or for copyright and footer text. 


**Example**

```html 
<p> This is regular text. <small>This is small text</small></p>
```

Result:

<p> This is regular text. <small>This is small text.</small></p>


 <h1 style="color:#3CCAE6">The `mark` tag</h1>


 This tag is used to highlight text. Like <mark>this.</mark> 


<h1 style="color:#3CCAE6">The `wbr` tag</h1>


This tag is used to introduce line breaks. It will not include a hyphen at the break. This is used so you can have more control on how the browser breaks your text.

**Example**

```html 
<p>This is a veryveryveryveryveryveryveryveryveryveryveryveryveryveryveryveryveryvery<wbr>longwordthatwillbreakatspecific<wbr>placeswhenthebrowserwindowisresized.</p>
```

<p>This is a veryveryveryveryveryveryveryveryveryveryveryveryveryveryveryveryveryvery<wbr>longwordthatwillbreakatspecific<wbr>placeswhenthebrowserwindowisresized.</p>