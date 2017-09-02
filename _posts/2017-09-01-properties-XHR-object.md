---
layout: post
title:  "Properties of the XHR Object"
categories: jekyll update
---

### Question:
Name five properties of the XHR object and describe what they are used for.
<hr>

## XHR properties

The XHR object is created like this:


```javascript
// I know its pretty ugly,outdated and long but I talk about some libaries than can help 
var xhr = new XMLHttpRequest();
```

To do anything with this object as it was intended for we use built in properties to carry out our request. I will setup a standard request to show some the most common properties used. 

<p data-height="368" data-theme-id="0" data-slug-hash="vJbjbd" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="ajax tutorial" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/vJbjbd/">ajax tutorial</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


<br>

Here we send a request using the xhr object. As you can see we use several properties. 

* xhr.open()
* xhr.onload()
* xhr.response
* xhr.send()

I will discuss these one by one now. 

### <b>xhr.open('request method', 'url')</b>

We use this to open the connection between our network with the server we're trying to reach. The open method takes two properties: request method and the url. In this case we are using the url to retrive names from a json object. 

we can either use 'GET' or 'POST' which are the most common. 'GET' is used to retrieve data and 'POST' is usually used to send data but can also be used to retrieve data. 

### <b>xhr.onload()</b>

This method was introduced in the XMLHttpRequest 2.0. It is easier to work with than its older sibling `onreadystatechange`. If you don't believe me see for yourself.

### <b>onreadystatechange version</b>
```javascript
//okay not too bad but its quite wordy and a bit confusing
var xhr = new XMLHttpRequest();
xhr.onreadystatechange = function() {
    if(xhr.status === 200) {
        console.log(JSON.parse(xhr.response).data); 
    }
    else {
        console.log('Error' + xhr.errorCode); 
    }
};  
xhr.open('GET', '/response.json'); 
xhr.send(); 
```

### <b>onload version</b>
```javascript
//alot cleaner I would say
var xhr = new XMLHttpRequest();
xhr.onload = function () {
  console.log(JSON.parse(xhr.response).data);
};
xhr.onerror = function () { 
 console.log('Error' + xhr.errorCode);
} 
xhr.open('GET', '/response.json'); 
xhr.send(); 
```

The reason for this is because onload only returns if the request was successful, were onreadystatechange returns when the state changes which can be successful or error. 

### <b>xhr.response</b>

The `response` property returns the data from the server. We pair it with our XML object to retrive the data. That's it. 

### <b>xhr.send()</b>

We use the send method to send our request. If we leave this out our request isn't going anywhere. Thats it. 

### <b>xhr.responseURL</b>
This one returns the url that we gave to the request. Pretty simple. 


## Alternatives  

We can use JQuery. 

### JQuery
```javascript
// a bit simpler but not buy much
 $.ajax(
    type: 'GET',
    url: '/response.json',
    success: function(response) {
        console.log(response);
    }
    error: function() {
        console.log('Error'); 
    }
    )
```


### Axios
There another libary that we can use called axios that helps and allows us to use promises. In real environment would have to link to axios libary. 
```javascript
axios.get('/response.json')
.then(function(response) {
    console.log(response);
}).catch(function(error){
    console.log(error);
}); 
```



### Fetch
The good thing about fetch is its built into javascript so you dont have to add another libary to your project. It has support in most browsers except IE(really?) 

```javascript
// promises are cool right
fetch('https://jsonplaceholder.typicode.com/users/')
 .then(processStatus)
 .then(function(response){
  return response.json().then(function(json){
    console.log(json);
})
}).catch(function(item){
   console.log(item); 
});



var processStatus = function (response) {
    // status "0" to handle local files fetching (e.g. Cordova/Phonegap etc.)
    if (response.status === 200 || response.status === 0) {
        return Promise.resolve(response)
    } else {
        return Promise.reject(new Error(response.statusText))
    }
};
```


<br><br>
