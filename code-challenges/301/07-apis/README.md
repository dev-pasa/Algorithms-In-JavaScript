array.map( fn(v,i) {} ) Much likearray.forEach(), the array.map() function iterates over an array and runs a call back for each element. The callback receives the value and the index of the array element as a parameter.

The difference is that .map() will always return you a new array of the same length as the original array comprised of your return values

Squaring a number
  let numbers = [2,3,4,5];
  
  let squares = numbers.map( function(n,i) {
    return n * n;
  });
  
  // or as a snazzy arrow function ...
  // let squares = numbers.map( n => n * 2 );
  
  console.log(squares); // [ 4, 9, 16, 25 ]

Changing the data shape
  let people = [
    { name: "John", role: "Dad" },
    { name: "Cathy", role: "Mom" },
    { name: "Zach", role: "Kid" },
    { name: "Allie", role: "Kid" },
  ];
  
  let folks = people.map( (person,i) => {
    return person.name;
  });
  
  console.log(folks); // [ "John", "Cathy", "Zach", "Allie" ]

**If you do nothing ... **

  let numbers = [2,3,4,5];
  
  let squares = numbers.map( function(n,i) {
  });
  
  console.log(squares); // [undefined, undefined, undefined, undefined, undefined]
  
Caveats and Notes
The original array is never mutated
You always get back a new array
The array returned is always the same length as the original