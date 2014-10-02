#Sample functions
```
var makeNoise = function() {
  console.log("Pling!");
};

makeNoise();
// → Pling!

var power = function(base, exponent) {
  var result = 1;
  for (var count = 0; count < exponent; count++)
    result *= base;
  return result;
};

console.log(power(2, 10));
// → 1024
```
Tips:The return keyword without an expression after it will cause the function to return undefined.

##Parameters and scopes

The parameters to a function behave like regular variables, but their initial values are given by the caller of the function, not the code in the function itself.
