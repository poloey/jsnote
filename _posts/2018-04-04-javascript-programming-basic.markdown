---
title: javascript programming basic
layout: post
---

# built in functions     


1. length 
1. toUpperCase()
1. toLowerCase()
1. charAt()
1. indexOf()
1. lastIndexOf()
1. startsWith()
1. endsWith()
1. concat()
1. trim()
1. repeat()
1. Number.isInteger(42); // <<< true
1. typeof
1. 5..toExponential() 
1. Math.PI.toFixed(3); //"3.142" -> its a string 
1. Math.PI.toPrecision(3); //"3.14" -> its a string 
1. Number('3') // 3
1. String(3) // '3'
1. parseInt()
1. parseFloat()
1. Number.isNaN()


Technically, only objects have properties and methods. JavaScript overcomes this by creating wrapper objects for primitive data types. This all happens in the background, so for all intents and purposes it appears that primitive data types also have properties and methods.

~~~js
const name = 'Alexa'; // declare and assign a variable
name.length; // retrieve the name variable's length property << 5
name['length'] // >> 5
name.toUpperCase(); // >> 'ALEXA'
name.toLowerCase(); // >> 'alexa'
name.charAt('1') // l 
name.indexOf('A') // 0
name.indexOf('z') // -1 // not found
name.lastIndexOf('A') // 4
~~~

# es6 new function 

~~~js
name.includes('A') // true
name.includes('Z') // false
name.startsWith('A');// << true
name.startsWith('a');// << false
name.endsWith('A'); // << false 
name.endsWith('a'); // << true
'JavaScript'.concat('Ninja'); // << 'JavaScriptNinja'
'Hello'.concat(' ','World','!'); // << 'Hello World!'
'Java' + 'Script' + ' ' + 'Ninja'; // << 'JavaScript Ninja'
' Hello World '.trim(); // << 'Hello World'
'Hello'.repeat(2); << 'HelloHello'
~~~


# template literals  (Super-Powered Strings) 

~~~js
const name = `Siri`; `Hello ${ name }!`; // << 'Hello Siri!'
~~~

# Symbols
Symbols were introduced as a new primitive value in ES6. They can be used to create unique values, which helps to avoid any naming collisions. Symbols are the only primitives that don't have a literal form. The only way to create them is to use the Symbol() function:

~~~js
const uniqueid = Symbol(); 
const uniqueid2 = Symbol('some string'); 
const A = Symbol.for('shared symbol');
const B = Symbol.for('shared symbol');
~~~


## typeof 

~~~js
typeof 3.14159; // floating point decimal << 'number'
~~~

##  hexa decimal, octal, binary 

* 0xAF -> x
* 0o23 -> o
* 0b1010 -> b

## exponential notation / scientific notation / standard form 

~~~js
1e6; // means 1 multiplied by 10 to the power 6 (a million) << 1000000
2E3; // 2 multiplied by 10^3 (two thousand) << 2000
//Decimal values can be created by using a negative index value:
2.5e-3; // means 2.5 multiplied by 10 to the power -3 (0.001)
~~~

## Number function 

~~~js
Number('3') // 3 // number 3
Number.isInteger(42); // <<< true
Number.isInteger(3.142); // << false
Number.isFinite(Infinity) // false
Number.isFinite(1/0) // false
Number.isFinite(NaN) // false
Number.isFinite(43) // true
~~~

## Number  Method 

`.` after number make confused javascript whether its decimal dot or object notation. We can bypass by two dot, space and following way

~~~js
5..toExponential(); // using 2 dot. otherwise js become confused whether its a decimal value "5e+0"
5 .toExponential();  // "5e+0"
5.0.toExponential(); // "5e+0"
(5).toExponential(); // "5e+0"
const number = 5;
number.toExponential(); // "5e+0"
Math.PI.toFixed(3) // 3.142
Math.PI.toPrecision(3) // 3.14
~~~

## operators 

* `+`  
* `-`  
* `*`  
* `/`  
* `**`   -> exponential operator introduced in es2017
* `%`   -> remainder of the division 
* `+=` -> compound assignment operator 
* `-=` -> compound assignment operator 
* `*=` -> compound assignment operator 
* `/=` -> compound assignment operator 
* `%=` -> compound assignment operator 
* `number++` -> post increments
* `number--` -> post decrement 
* `++number` -> pre increment 
* `--number` -> pre decrement

## string to number  using Number function and coercing technique

~~~js
Number('5') // 5

'5' * 1 // 5
+'5' // 5
~~~

## number to string 

~~~js
String(10) // '10'
10 + '' // '10'
10..toString(); // '10'
10..toString(2); // '1010' -> binary (base 2) max base can be 36
~~~

## parsing number 

~~~php
parseInt('1010', 2) // 10 -> convert for binary and back to decimal
parseInt('omg', 36) // 31912
parseInt('23', 10) // 23
parseInt('23') // 23
parseFloat('23.23') // 23.23
~~~

## null and undefined 

~~~js
10 + null; // null behaves like zero << 10
10 + undefined; // undefined is not a number << NaN
~~~


## chapter summary 

* Comments are ignored by the program, but make your program easier to read and understand
* Data types are the basic building blocks of all JavaScript programs.
* There are six primitive data types: strings, symbols, numbers, Booleans, undefined and null.
* Non-primitive data types, such as arrays, functions and objects, all have a type of 'object'.
* Variables point to values stored in memory and are declared using the const or let keywords.
* Values are assigned to variables using the = operator.
* Strings and numbers have various properties and methods that provide information about them.
* Symbols are unique, immutable values.
* Boolean values are either true or false .
* There are only seven values that are false in JavaScript and these are known as 'falsy' values.
* Data types can be converted into other data types. 
* Type coercion is when JavaScript tries to convert a value into another data type in order to perform an operation.
* Logical operators can be used to check if compound statements are true or false.
* Values can be compared to see if they are equal, greater than or less than other values.











