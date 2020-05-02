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

## FreeCodeCamp: Basic JavaScript
Data types: undefined, null, boolean, string, symbol, number, and object.

.push()
Add element at the back of an array.
```
var arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
// arr2 now equals ["Stimpson", "J", "cat", ["happy", "joy"]]
```

.pop()
Used to "pop" a value off of the end of an array. We can store this "popped off" value by assigning it to a variable.
```
var threeArr = [1, 4, 6];
var oneDown = threeArr.pop();
console.log(oneDown); // Returns 6
console.log(threeArr); // Returns [1, 4]
```

.shift()
Removes the first element of the array.
```
var ourArray = ["Stimpson", "J", ["cat"]];
var removedFromOurArray = ourArray.shift();
// removedFromOurArray now equals "Stimpson" and ourArray now equals ["J", ["cat"]].
```

.unshift()
Adds an element to the beginning of the array.
```
var ourArray = ["Stimpson", "J", "cat"];
ourArray.shift(); // ourArray now equals ["J", "cat"]
ourArray.unshift("Happy");
// ourArray now equals ["Happy", "J", "cat"]
```

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

## Notes from classes
var x = wel reasignen
let x = wel readignen
const x = mag niet veranderd worden

```
let x = 3
function new (){
  x = 4
}
```
Zo vaak mogelijk const gebruiken alleen wanneer het nodig is een let gebruiken.
Het verschil tussen let en var is de bescherming. Var is altijd opnieuw aan te passen:
```
var naam = "Asa"
var naam = "Tom"

let naam = "Asa"
let naam = "Tom"  <-- Dit kan niet
naam = "Tom"      <-- Dit wel
```
Makkelijke manier om te printen:
```
printName = (name) => {console.log(name)}
```

Executing a function is called invoking
- named
- invoked result in variable
- anonymous: kan niet hergebruikt worden
- arrow: bij es6 =>

Higher order
```
callback function: addEventListener(  'click',  functie)
                                      actie     aanroep
```
Objects
```
const object = {
  key1: 'value',
  key2: 12,
  key3: [1, 2, 3]
}
```
propert = key1: 'value'

Json lijkt op objecten -> data storage
mutable = wel aanpasbaar
immutable = niet aanpasbaar/overschrijfbaar

objecten aanpassen:
```person.firstName = 'AndereNaam' ```
-> je kunt niet het gehee object aanpassen alleen per property.

dingen uit het object halen:
```console.log(person.interests[1])```

Methods = a function binnen een object
```greeting: function (){
  alert ('Hi ' + this.name);
}
```

Execution context, hoisting, scope, closures
lege pagina: about.blank  -> open console
console.log(window)       -> window {parent.window.innerHeight  -> 731
console.log(this)

window  - global: browser eigenschappen
this    - binnen object
global  - global

declaratie  en   assignment
var course  =   'block tech'; 

ge-hoist = gegevens worden naar boven gezet in het script (eigenlijk is het dat er ruimte wordt gereserveerd voor bepaalde gegevens)

Global execution context
creation phase:
- maken global object
- maken this
- memory space for variables en functions
- assign variabes a deafault value in the memory (undifined)
Hierna enter je execution phase

Function declaration  =aangemaakt
Function call         =geroepen
Function execution context:
```function skills() {
  console.log(argumets);
}

skills ('Frontend', 'Backend')
```
arguments is een array-like van parameters.

Scope = the current context of execution.
Hoisting = Functions worden naar boven getrokken zo wordt de code gelezen.
Closures = 2 functions in elkaar: outer function, inner functions. Closures allows the inner fucntion to access the variables inside of its outer function. Zie het als gobal var en fncties, ze kunnen alsnog bij de global var.
Spoce = current context:
        - global scope (gehele script) vs. local scope (binnen blok waar gedeclareerd).
        - function scope (binnen functie) vs. bock scope (if-statement, for-loop).
