*https://eloquentjavascript.net/04_data.html*

## Data Structures: Objects and Arrays - chapter 4
Numbers, Booleans, and strings are the atoms that data structures are built from. Many types of information require more than one atom, though. Objects allow us to group values—including other objects—to build more complex structures.
Data sets = a chunk of digital data, ike an array.
Properties = de eigenschappen van een waarde. myString.length etc.
Methods = Properties that contain functions are generally called methods of the value they belong to.
This example demonstrates two methods you can use to manipulate arrays:
```
let sequence = [1, 2, 3];
sequence.push(4);
sequence.push(5);
console.log(sequence);
// → [1, 2, 3, 4, 5]
console.log(sequence.pop());
// → 5
console.log(sequence);
// → [1, 2, 3, 4]
```
The push method adds values to the end of an array, and the pop method does the opposite, removing the last value in the array and returning it.
Objects = Values of the type object are arbitrary collections of properties. One way to create an object is by using braces as an expression.
```
let day1 = {
  squirrel: false,
  events: ["work", "touched tree", "pizza", "running"]
};
console.log(day1.squirrel);
// → false
console.log(day1.wolf);
// → undefined
day1.wolf = false;
console.log(day1.wolf);
// → false
```
Mutability = You can change their properties, causing a single object value to have different content at different times. This is not posible with numbers, strings and booleans. (?)
```
let object1 = {value: 10};
let object2 = object1;
let object3 = {value: 10};

console.log(object1 == object2);
// → true
console.log(object1 == object3);
// → false

object1.value = 15;
console.log(object2.value);
// → 15
console.log(object3.value);
// → 10
```
