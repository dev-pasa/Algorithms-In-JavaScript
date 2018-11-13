Array.forEach allows you to iterate through an array. Where a normal for loop is "iterative", forEach is more declarative or functional in nature.

It is implemented as a method on your array instance.

  let myArray = ['a', 'b', 'c'];
  myArray.forEach( ... )
It takes a callback as a parameter, which in turn receives the value and the iterator, and runs it on every element.

  let myArray = ['a','b','c'];

  myArray.forEach( function(value, i) {
    console.log(i);       // 0, 1, 2
    console.log(value);   // a, b, c
  })