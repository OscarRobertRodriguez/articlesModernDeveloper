---
layout: post
title:  "Accessibility in Web Development - Role Attributes"
categories: jekyll update
---
### Question:
Describe the function of the `role` attribute and give example code snippets that demonstrate its usage.

<hr>

<h1 style="color:#3CCAE6">The role of the `role` attribute</h1>


Why use a role attribute? Is it just another piece of markup that bloats our html with unnecessary verbage. For most visitors to a site it will not bother them but with people with disablities say for people who are visually impaired it is good to include these values and we should as it is the right thing to do. 


Let's say we are using links as buttons we'll we can do that but people with screen readers won't know there meant to be used as buttons so we give them the role of button. 


```html 
<a href="#" role="button" >Delete</a>
```


We can also use roles to define tags that make up the main sections. These are called landmark roles such as giving our main content or a header tag the role of `banner`. Other landmark roles include :

* `banner`
* `complementary`
* `contentinfo`
* `form`
* `main`
* `navigation`
* `search`
* `application`



<h2 style="color:#3CCAE6">Widget Roles</h2>

Widget roles are the aria roles primarly used with tags to denote how that tag is used such as using `role="alert"`  to show the screen reader to read this information immediately. 

There are other roles such as this to give tags more semantic meaning to denote what they are used for. 

<h2 style="color:#3CCAE6">Composite Roles</h2>

Composite roles are used as wrappers for widget roles to denote what the widget contains. Such as `role="menu"` containing  `role="menuitem"`. 

```html 
<nav role="menu">
    <a role="menuitem">Option 1</a>
    <a role="menuitem">Option 2</a>
    <a role="menuitem">Option 3</a>
    <a role="menuitem">Option 4</a>
</nav>
```