##JavaScript-Developer-Bible
==========================

JavaScript Developer Bible

**A JavaScript program is a list of statements.**

Ex.
```
var foo = "Hello World";
var child_math = 5 * 5;
var name = "Misko";
console.log(name + " created the angular.js framework");
```
```
var x = [a,b,c];
```
*addEventListener Basics*

addEventListener is the way to register an event listener as specified in W3C DOM. Its benefits are as follows:

It allows adding more than a single handler for an event. This is particularly useful for DHTML libraries or Mozilla extensions that need to work well even if other libraries/extensions are used.
It gives you finer-grained control of the phase when the listener gets activated (capturing vs. bubbling)
It works on any DOM element, not just HTML elements.

```
<table id="outside">
    <tr><td id="t1">one</td></tr>
    <tr><td id="t2">two</td></tr>
</table>

// Function to change the content of t2
function modifyText() {
  var t2 = document.getElementById("t2");
  if (t2.firstChild.nodeValue == "three") {
    t2.firstChild.nodeValue = "two";
  } else {
    t2.firstChild.nodeValue = "three";
  }
}

// add event listener to table
var el = document.getElementById("outside");
el.addEventListener("click", modifyText, false);



```
