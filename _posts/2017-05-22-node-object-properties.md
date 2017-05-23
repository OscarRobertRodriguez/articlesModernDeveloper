---
layout: post
title:  "Node Properties"
categories: jekyll update
---
### Question:
Describe the different properties that exist on `Node` objects and explain the function of each property.
<hr>


The 'Node' object has several properties that are useful in navigating the DOM. Let's discuss them below. 



* baseURL 
  
 Used to get the absolute URL of a node like so: 

```javascript
 document.querySelector('img').baseURI
 //returns  https//www.images.com/bats 
```

* nodeName 
  
 returns an elements tag name or element type if not an element node 

```javascript
 document.querySelector('img').nodeName 

  // returns "IMG"
```

* nodeValue  
  
 returns the node if it's a text node or comment node will return null for everything else 

```javascript
 document.querySelector('img').nodeValue 

 /* returns null */
 
 /* <p>Hello David</p> */

document.querySelector('p').firstChild.nodeValue
  //returns "Hello David"
```


* nodeType
  
 returns a numerical value that represents the node type. 

```javascript
 document.querySelector('img').nodeType
 // returns 1 for ELEMENT_NODE
```

* parentNode 
  
 returns a numerical value that represents the node type. 

```javascript
/* 
<body>

<img src="images/are/cool" alt=""/>

<p>Hello David</p>
  
</body>
*/


 document.querySelector('img').parentNode; 
 // selects the body  
```

* parentElement 
  
 does the same thing as parentNode except will return null if parent is not an element node.

```javascript
/* 
<body>

<img src="images/are/cool" alt=""/>

<p>Hello David</p>
  
</body>
*/


 document.querySelector('img').parentElement; 
 // selects the body  
```

* firstChild 
  
 returns the firstChild node if no child nodes returns null. spaces are considered children with this property 

```javascript
/*
  <ul>
    <li>foo</li>
    <li>bar</li>
    <li>zap</li>
  </ul>
*/ 

  document.querySelector('ul').firstChild;
  //return empty space; 
```


* lastChild
  
 same as firstChild except it returns the last child

```javascript
/*
  <ul>
    <li>foo</li>
    <li>bar</li>
    <li>zap</li>
  </ul>
*/ 

  document.querySelector('ul').lastChild;
  //return empty space; 
```


* childNodes
  
 returns a numerical value that represents the node type. 

```javascript
/*
  <ul>
    <li>foo</li>
    <li>bar</li>
    <li>zap</li>
  </ul>
*/ 

  document.querySelector('ul').childNodes;
  //returns a live list of all the child nodes 
```


* previousSibling
  
 returns the previousSibling if it contains sibilings or null if no next sibling 

```javascript
 /*
  <ul>
    <li>foo</li>
    <li>bar</li>
    <li>zap</li>
  </ul>
*/ 

  document.querySelector('ul').previousSibling;
  //returns null 
```


* nextSibling 
  
 returns the next sibling if found 

```javascript
/*
  <ul>
    <li>foo</li>
    <li>bar</li>
    <li>zap</li>
  </ul>
*/ 

  document.querySelector('li').nextSibling;
  //returns null 
```


* textContent 
  
 returns a numerical value that represents the node type. 

```javascript
 document.querySelector('p').textContent 
 // returns "Hello David"
```

* ownerDocument
  
 returns a reference to the root node 

```javascript
 document.querySelector('img').nodeType
 // returns 1 for ELEMENT_NODE
```

