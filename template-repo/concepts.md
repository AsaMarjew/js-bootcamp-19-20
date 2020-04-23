# Introduction to JavaScript

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

# Objects and Arrays

*https://www.youtube.com/watch?v=VIQoUghHSxU*

## 7.1: What is an array? - p5.js Tutorial
Array = a list of variables in between [] and begins by 0.
```
var nums = [100, 25, 12, 72];
nums[2];
//output: 12
```
Example
```
var words = ['red', 'green', 'blue', 'yellow']
var index = 0;

function setup() {              //Execute automate
  createCanvas(400, 400);
}

function draw() {
  background(0);
  
  fill(255);
  textSize(32);
  text(words[index], 12, 200);
}

function mousePressed() {
  index = index + 1;            //On pressed add 1
  
  if (index == words.length){   //Error handling
    index = 0;                  //Index value reset
  }
}
```

*https://www.youtube.com/watch?v=-e5h4IGKZRY*

## 2.3: JavaScript Objects - p5.js Tutorial
Organize variables in different catagory's 
Dot syntax
```
var circle = {
  x: 0,
  y: 100,
  diameter: 50
};

ellipse(circle.x, circle.y, circle.diameter, circle.ciameter);
```
