---
title: arrays logic loop
layout: post
---
## functions 

1. `delete <variablename>` (using splice would be good choice for array)
1. pop()
1. shift()
1. unshift()
1. push()
1. concat()
1. [...array1, ...array2]
1. join(), join('separator')
1. slice(starting_index, ending_index_but_not_included);
1. splice(starting_index, how_many, [new array]);
1. sort()
1. reverse()
1. indexOf()
1. includes()


## removing array
~~~js
const avengers = ['Captain America', 'Iron Man', 'Thor', 'Hulk']; 
delete avengers[3]; // make index 3 undefined
['Captain America', 'Iron Man', 'Thor', undefined]
~~~

## destructuring 

~~~js
const [x, y] = [1, 2];
// we can swap value using destructing 
[x,y] = [y,x];
~~~

## pop, shift, unshift, push, concat

~~~php
avengers.pop()
avengers.shift()
avengers.unshift('thor')
avengers.push('hulk');
avengers = avengers.concat(['hulk', 'black widow']); // merging array
[...avengers, ...['hulk', 'black widow']]; // spread array -> merging alternative in es6
# array join make array into string 
avengers.join(); << 'Captain America, Iron Man, Thor, Hulk, Hawkeye, Black Widow'
# separator other than comma
avengers.join(' & '); << 'Captain America & Iron Man & Thor & Hulk & Hawkeye & Black Widow'
avengers.slice(2,4) // starts at the third item (index of 2) and finishes at the fourth (the item with index 4 is not included) << ['Thor', 'Hulk']
avengers.splice(3, 1, 'Scarlet Witch'); << ['Hulk'] // deleted element is returned 
// we can added new value using splice 
avengers.splice(4,0,'Quicksilver');
avengers.reverse()
avengers.sort()
avengers.indexOf('Iron Man'); // << 3
avengers.indexOf('Desi Man'); // << -1 
avengers.includes('Iron Man'); // << true
avengers.includes('Iron Man', 1); // << true // searching from index 1
~~~

# Sets 

Sets were introduced to the specification in ES6. A set is a data structure that represents a collection of unique values, so it cannot include any duplicate values. They are similar in concept to a mathematical set.   


~~~js
lest list = new Set();
list.add(1) // {1}
list.add(3).add(4).add(8) // {1, 3, 4, 8}
list.add(1)// {1, 3, 4, 8} // operation ignored since 1 already present 
const numbers = new Set([1,2,3]);
~~~



