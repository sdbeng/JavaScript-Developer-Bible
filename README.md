##JavaScript-Developer-Bible
==========================

JavaScript Developer Bible. Thank you to eloquentjs and foobar source for letting me share this concepts.

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
#Variables basics
```
var JohnsDebt = 120;
JohnsDebt = JohnsDebt - 20;
console.log(JohnsDebt);
// → 100
```
#Undefined
var foo; //undefined

#Environment
The collection of variables and their values that exist at a given time is called the environment. When a program starts up, this environment is not empty. It always contains variables that are part of the language standard, and most of the time, it has variables that provide ways to interact with the surrounding system. For example, in a browser, there are variables and functions to inspect and influence the currently loaded website and to read mouse and keyboard input.

##Console.log
Though variable names cannot contain period characters, console.log clearly has one. This is because console.log isn’t a simple variable. It is actually an expression that retrieves the log property from the value held by the console variable.
```
var hackx = 33;
console.log("the value of hackx is", x);
// → the value of hackx is 33
```
##Return values
```
console.log(Math.min(2, 7) + 100);
// → 102
```
##While Loops
```
var number = 0;
while (number <= 12) {
  console.log(number);
  number = number + 2;
}
// → 0
// → 2
//   … etcetera
```
##

#addEventListener Basics

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
#Unit testing - Jasmine

Jasmine is a behavior-driven development framework for testing JavaScript code. It does not depend on any other JavaScript frameworks. It does not require a DOM. And it has a clean, obvious syntax so that you can easily write tests.

```
describe("A suite", function() {
  it("contains spec with an expectation", function() {
    expect(true).toBe(true);
  });
});
```
After downloading a particular version and unzipping, opening SpecRunner.html will run the included specs. You’ll note that both the source files and their respective specs are linked in the <head> of the SpecRunner.html. To start using Jasmine, replace the source/spec files with your own.

##Suites: describe Your Tests
A test suite begins with a call to the global Jasmine function describe with two parameters: a string and a function. The string is a name or title for a spec suite – usually what is being tested. The function is a block of code that implements the suite.

##Specs
Specs are defined by calling the global Jasmine function it, which, like describe takes a string and a function. The string is the title of the spec and the function is the spec, or test. A spec contains one or more expectations that test the state of the code. An expectation in Jasmine is an assertion that is either true or false. A spec with all true expectations is a passing spec. A spec with one or more false expectations is a failing spec.

##It's just functions
Since describe and it blocks are functions, they can contain any executable code necessary to implement the test. JavaScript scoping rules apply, so variables declared in a describe are available to any it block inside the suite.

More updates soon.
