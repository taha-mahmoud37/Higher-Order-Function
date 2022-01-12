
## Higher Order Function in JavaScript

 If you are learning JavaScript, you may hear about functional programming.


Higher-Order Function is a lot used in JavaScript. If you have been programming you may have already used them without even knowing 
<br>

In order to understand this concept, you should first understand what Functional Programming is and the concept of First-Class Functions.
<br>
<br>

### Functional Programming
Functional Programming is a form of programming in which you can pass functions as parameters to other functions and also return them as values. 

there are many programming languages that supported functional programming like Haskell, JavaScript, Python, Scala, Erlang, Lisp, ML, Clojure, OCaml.
<br>
<br>
### First-Class Functions
In JavaScript, anything is an object so JavaScript treats functions as first-class citizens.

To prove functions are objects in JavaScript, we can do this

For example:

```
// We can add properties to functions like we do with objects
greeting.name = 'Islam';
// Prints 'Islam'
console.log(greeting.name);
``` 

but this is considered a bad practice, you should not add random properties to the functions, you can use an object if you want do that.
<br/>
<br/>

### Assigning Functions to Variables
you can assign functions to variables on JavaScript.

For example:

```
const square = function(x) {
  return x * x;
}
// prints 25
square(5); 

``` 
<br>
###  Passing Functions as Parameters
We can pass functions as parameters to other functions.

For example:

```
function hello() {
  console.log("hello");
}
function welcome() {
  console.log("welcome");
}
function greet(type, sayHello, sayWelcome) {
  if(type === 'hello') {
    sayHello();
  } else if(type === 'welcome') {
    sayWelcome();
  }
}
// prints 'welcome?'
greet('welcome', hello, welcome);

``` 
<br>

## Higher-Order Functions
A higher-Order function is a function that receives a function as an argument or returns the function as output.


there are some Higher-Order functions built into the language like, map(), filter(), forEach(), reduce(), and sort().


Some examples of the built-in higher-order function and compare it with normal solutions. 
<br>
<br>

### First example about map()
The map() method is used if we want to perform the same change on each element of the array. it takes a function as a parameter that function is passed (element, index, array) as parameters.


- Without Higher-order function.

```
const arr1 = [1, 2, 3];
const arr2 = [];
for(let i = 0; i < arr1.length; i++) {
  arr2.push(arr1[i] * 2);
}
// prints [ 2, 4, 6 ]
console.log(arr2);

``` 


- With Higher-order function map.

```
const arr1 = [1, 2, 3];
const arr2 = arr1.map(item =>  item * 2 );
console.log(arr2);
``` 

<br>


### Second example about filter()

filter allows us to pick which elements of the array that pass the test. a filter takes function that return a Boolean value (true/false). As for map,  this function is passed (element, index, wholeArray).

 
- Without Higher-order function.

```
const persons = [
  { name: 'Peter', age: 16 },
  { name: 'Mark', age: 18 },
  { name: 'John', age: 27 },
  { name: 'Jane', age: 14 },
  { name: 'Tony', age: 24},
];
const fullAge = [];
for(let i = 0; i < persons.length; i++) {
  if(persons[i].age >= 18) {
    fullAge.push(persons[i]);
  }
}
console.log(fullAge);
``` 


- With Higher-order function filter.

```
const persons = [
  { name: 'Peter', age: 16 },
  { name: 'Mark', age: 18 },
  { name: 'John', age: 27 },
  { name: 'Jane', age: 14 },
  { name: 'Tony', age: 24},
];
const fullAge = persons.filter(person => person.age >= 18);
console.log(fullAge);

``` 
 
<br>

### Third example about reduce()

reduce is used to change the shape of the array. the reduce method accepts two parameters.

1) The reducer function
2) optional initialValue


The reducer function accepts four parameters: accumulator, currentValue, currentIndex, sourceArray.


 If an initialValue is provided, then the accumulator will be equal to the initialValue and the currentValue will be equal to the first element in the array.


If no initialValue is provided, then the accumulator will be equal to the first element in the array and the currentValue will be equal to the second element in the array.



- With Higher-order function reduce.


```
const arr = [5, 7, 1, 8, 4];
const sum = arr.reduce(function(accumulator, currentValue) {
  return accumulator + currentValue;
});
// prints 25
console.log(sum);

``` 

Every time you call the reduce function accumulator keeps the result of the previous operation returned from the reducer function and the currentValue is set to the current value of the array.


<br>

## conclusion

We have talked about what Higher-order functions is and some built-in Higher-order function. 

In a nutshell, Higher-order functions are just like regular functions with an added ability of receiving and returning other functions are arguments and output.



By the way, you can check these links if you want to dive into a higher-order function and you can find more than a way to understand that concept in a better way.

- https://bit.ly/3qqTvIY

- https://bit.ly/3mE6gPg

- https://bit.ly/3Jk2Bjb
<br>


This is a YouTube channel I highly recommend for this concept and it explains that with some fun.

- https://bit.ly/3mBQODa
<br>
<br>

By the end, Thank you for reading that and I hope you find this article useful.