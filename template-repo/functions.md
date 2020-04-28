*https://www.youtube.com/watch?v=wRHAitGzBrg*

## 5.1: Function Basics - p5.js Tutorial
Ellipse, setup and draw function leven inside de p5 library. Deze worden automatisch aangeroepen zonder dat je dit aangeeft.
Function setup moet wel aangemaakt worden door de gebruiker.

1. Modularity = Componenenten die samengevoegd of gescheiden dienen te worden.
2. Reusability = Opnieuw te gebruiken (arguments/parameters).

*https://eloquentjavascript.net/03_functions.html*

## Functions chapter 3
Some functions produce a value and some only result is a side effect. A return statement determines the value the function returns.
Global variables are bindingd defined outfide of any function.
Local bindings reference only inside a function. 
When multiple bindings have the same name—in that case, code can see only the innermost one. For example, when the code inside the halve function refers to n, it is seeing its own n, not the global n.
Nesting = function inside functions.

Arrow Functions
```
const square1 = (x) => { return x * x; };
const square2 = x => x * x;
```
Call Stack = the way the flow of contro is happening inside a script.

Closure = A function that references bindings from local scopes around it.
In the example, multiplier is called and creates an environment in which its factor parameter is bound to 2. The function value it returns, which is stored in twice, remembers this environment. So when that is called, it multiplies its argument by 2.
```
function multiplier(factor) {
  return number => number * factor;
}

let twice = multiplier(2);
console.log(twice(5));
// → 10
```

Recursion = a function that calls itself.
```
function power(base, exponent) {
  if (exponent == 0) {
    return 1;
  } else {
    return base * power(base, exponent - 1);
  }
}

console.log(power(2, 3));
// → 8
```

*https://www.youtube.com/watch?v=H4awPsyugS0*

## 16.5: Higher Order Functions in JavaScript - Topics of JavaScript/ES6
Higher level function = function die een functie aanroept.
Array's: map(), sort(), reduce(), filter().

```
function sing(callback) {
  console.log('la la la');
  if (callback instanceof Function) {
    callback();
  }
}

function meow() {
  console.log('meow meow');
}
```
Aanroepen als:
```
sing(meow)

output:
la la la 
meow meow
```

***instanceof function?***

```
function multiplier(factor) {
  return function(x) {
    return x * factor;
  }
}

console:
let doubler = multiplier(2);
doubler(4);

output:
8
```
Korte manier om op te schrijven:
```
function multiplier(factor) {
  x => x * factor;
}
```
