*https://eloquentjavascript.net/01_values.html*

## The basics of computer programming (Intro)
JavaScript is available on almost every decive becease it is built into every modern web browser
ECMAScript: Ecma International organization: standardization of JavaScript

*https://github.com/getify/You-Dont-Know-JS/blob/2nd-ed/get-started/ch1.md*

## You Don't Know JS Yet: Get Started - 2nd Edition - Chapter 1: What is JavaScript?
Main pillars wich JS is organized on: scope/closures, prototypes/objects, and types/coercion. 
Node.js is een JS runt omgeving waarbij deze uitgevoerd buiten een browser.
Console/REPL (Read-Evaluate-Print-Loop).

- Procedural style organizes code in a top-down, linear progression through a pre-determined set of operations, usually collected together in related units called procedures.

- OO style organizes code by collecting logic and data together into units called classes.

- FP style organizes code into functions (pure computations as opposed to procedures), and the adaptations of those functions as values.

## Fun Fun Function - var, let and const (video)
Immideately invoked function expression = IIFE = wordt gelijk geroepen.

```
(function () {
  for (var i = 0; i < 10; i++) {
    console.log(i)
  }
})()
console.log('after loop', i)
```

Hoisted = interperter pushed de variabe declaratie naar de top of de code.

Wanneer je de var vergeet maakt js ze automatische aan. Gebruik use strict boven aan de functie om dit te verkomen.

```
"use strict";
```

let = locked scope.
const = niet aan te passen, behalve als object (zie voorbeeld) -> Minimize mutable state

```
const x = {
  y: 5
}
x.y = 6
*dit werkt*

x = {
  z: 9
  }
*dit werkt NIET*
```

Ask yourself: Moet deze variable aangepast worden? Zo niet maak het een const

*https://eloquentjavascript.net/01_values.html*

## Values, Types, and Operators (chapter 1)
Fractional numbers = written by using a bot = 9.81.
e = exponent = 2.998e8 = 299800000.
operators = + and * symbols.
Comparison = boolean = true/false
Logical operators: && = and, || = or, ? = first one is true second one is false
