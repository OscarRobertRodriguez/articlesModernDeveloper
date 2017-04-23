---
layout: post
title:  "JASON.parse"
categories: jekyll update
---
### Question:
Explain the function of the `JSON.parse` method and give an example of its usage.
<hr>

We use the `JSON.parse` method to turn JASON string back into the orginal JASON object or array. Using are last example let's parse it. 


```jason
var newContact = JASON.stringify(contact);
"{"name":"oscar","email":"oscar@gmail.com","phone":"232-2332-323"}"

JASON.parse(newContact);

{
    "name": "oscar",
    "email": "oscar@gmail.com",
    "phone": "232-2332-323"
}
```

We pass the string to parse and we get the object we had before we stringifed it . 