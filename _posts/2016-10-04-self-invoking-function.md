---
layout: post
title:  "Self-Invoking Functions"
categories: jekyll update
---

### Question:
Explain what a self-invoking function is and describe the use of such a function, including a demonstration.

<hr>

<h1 style="color:#3CCAE6">Function Declarations</h1>
Before we get into self-invoking functions let's talk about the  basic function used in JavaScript.
A function in the most simple terms takes a parameter or parameters and outputs a value based on the calculation that function does.
A function declaration looks like this in JavaScript:

```javascript
// function declaration
function greet(name) {
    console.log("Hello " + name);
}
greet("oscar"); // invoked by using the "()" after function name
```
Above we have a function declaration that goes by the name of `greet` - holds the parameter called name. We use `name` with console.log to return "Hello + name" which we invoke it
with `greet('oscar');`.

<br>
<div class="panel panel-warning">
    <div class="panel-heading">
    <h3 class="panel-title">Important Note:</h3>
    </div>
    <div class="panel-body">
    JavaScript functions will always run immediately when you put ( ) after their name.
    For example:<br>
     greet(); // will run immediately<br>
     greet; // will not run immediately and can be used as a callback
    </div>
</div>

<h1 style="color: #3CCAE6">Function Expressions</h1>

Function expressions are functions but with a variable assignment. Expressions can be named or be anonymous and they never start with the word "function".

```javascript
// function expression
var greet = function(name) {
    console.log("Hello " + name );
}
// named function expression
var greetFunc = function greet(name) {
    console.log("Hello " + name );
}
```
Although they usually can be used interchangeably they differ in the way they are hoisted. When the execution context is run declarations are put into memory and can be reached anywhere.
Expressions are seen as variables so when they are hoisted they are set to `undefined` - only called when invoked.

The only downside to this is that you must not invoke your function before
you have declared it or you will get an error but there are many plus sides to using expressions over declarations as it only makes for a more readable code but better code.

Now that we understand these differences between these functions it will be clearer in the next section what self-invoking functions are.

<h1 style="color: #3CCAE6">Self-Invoking Functions</h1>

Self-Invoking functions also known as Immediately Invoked Function Expressions or `IIFE` for short are functions that run on the fly.

```javascript
// An IIFE
(function(name) {
    var greeting = " Hello what's up ";
    console.log(greeting + name);
}("oscar"));
```
Here we got the same code as in the previous examples but here we invoke and pass a parameter at the end of the function. Also, notice that the whole function is wrapped in parentheses
keeping everything inside locked within the scope. IIFEs are used in a lot of modern JavaScript libraries because of this and in data security.

```javascript
var greeting = "I'm global";  // global variable

(function(name) {
    var greeting = " Hello whats up "; // same variable but is safe
    console.log(greeting + name);
}("oscar"));
```

In the above code, we see that there is a global variable with the same name as the one within our function but because it's an IIFE its scope is the lock to that function.
Had we used an expression or a declaration it would not be safe and we would end up with "I'm global oscar" instead.


<a href="https://jsbin.com/gawojep/edit?js,console" class="btn btn-link" target="_blank" style="font-size:16px">Checkout this Jsbin to show this example</a><br>

<h1 style="color: #3CCAE6">Summary</h1>
We covered a lot but hopefully you have a better understanding of self-invoking functions and why they are so useful when it comes to building modular code.