---
layout: post
title:  "Same-site Cookies"
categories: jekyll update
---

### Question:
Explain what same-site cookies are and describe how they work and how to set them up.
<hr>

Same-site cookies where developed by Google to combat Cross-site Request Forgery (CSRF/XSRF) attacks. This is done by matching the cookies origin. If the origin doesn't match the cookie's, it won't work. This helps prevent a thief from getting your cookie and messing with your accounts. 

## How to make 

To make a same-site cookie it is about the same as making a regular cookie but with a small change.

```javascript
  document.cookie = 'my_cookie=cool-cookie;sameSite=lax';
```

The `sameSite=lax` allows us to make a same-site cookie but with a re'lax'ed settings so it only blocks cookies that deal with POST request.

We can also use the 'strict' option to block all cookies that do not share the same origin but this is not necessary most of the time as you will lose some functionality. 

```javascript
  document.cookie = 'my_cookie=cool-cookie;sameSite=strict'; 
```