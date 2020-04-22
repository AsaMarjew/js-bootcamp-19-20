*https://www.youtube.com/watch?v=wRHAitGzBrg*

## 5.1: Function Basics - p5.js Tutorial
Ellipse, setup and draw function leven inside de p5 library. Deze worden automatisch aangeroepen zonder dat je dit aangeeft.
Function setup moet wel aangemaakt worden door de gebruiker.

1. Modularity = Componenenten die samengevoegd of gescheiden dienen te worden.
2. Reusability = Opnieuw te gebruiken (arguments/parameters).

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
