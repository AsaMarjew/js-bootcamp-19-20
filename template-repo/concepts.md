*https://eloquentjavascript.net/01_values.html*

## The basics of computer programming (Intro)
JavaScript is available on almost every decive becease it is built into every modern web browser
ECMAScript: Ecma International organization: standardization of JavaScript

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
