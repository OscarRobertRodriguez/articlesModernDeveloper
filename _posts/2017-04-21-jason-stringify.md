---
layout: post
title:  "JASON.stringify"
categories: jekyll update
---
### Question:
Explain the function of the `JSON.stringify` method and give an example of its usage.
<hr>

We use the `JSON.stringify` method to pass JASON data between servers as it's a more efficent way of doing things. Let's say we have a JASON string that we want to send. 

```jason
var contact = {
    "name": "oscar",
    "email": "oscar@gmail.com",
    "phone": "232-2332-323"
}
```

Then we call the stringify method.

```jason
var contact = {
    "name": "oscar",
    "email": "oscar@gmail.com",
    "phone": "232-2332-323"
}

JASON.stringify(contact);
```

This will result in a JASON string that will appear like this. 


```jason
"{"name":"oscar","email":"oscar@gmail.com","phone":"232-2332-323"}"
```



