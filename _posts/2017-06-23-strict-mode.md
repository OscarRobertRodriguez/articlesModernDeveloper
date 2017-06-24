---
layout: post
title:  "strict and quirks mode"
categories: jekyll update
---

### Question:
Explain what 'strict mode' is and contrast with it with its alternative, 'quirks mode'
<hr>


Strict mode is a mode that is used in JavaScript to allow a more attentive error system to changes or silent errors that happen. For example:

```javascript
 'use strict'; 

   x = 3; 

  // returns an error because x was not declared this prevents you assigning variable to the global scope
```


If we didn't use strict mode we wouldn't get anything back but our code wouldn't work and would fail silently. 




Quirks mode happens when we don't include the doctype in our html or our html is so malformed that quirks mode takes affect. It was invented for IE5 so that browser features that were later added to could be disabled for it to run on this browser. This isn't really used anymore today unless you have to support IE5 which is unlikely. Also the Javascript aspect supports only up to IE6 which means that the root element is the document.body and the standard mode is the html-element. 