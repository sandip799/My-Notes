## 103- Destructuring Arrays
- Destructing is nothing but to break the complex data structure into smaller data variables
- Link of the documentation https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment]] 
## 104- Destructuring Objects
- for destructuring arrays we use square brackets but here we use curly braces
- the variable name must be as same as property name
- again you can also change the variable name
- Link of the documentation https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment]]
## 105- Spread Operator(...)
- This operators works on all iterable, iterables are like array, string, map, set etc but not object
- and we can use this only while creating an array or passing values in function
- It takes all the elements out of the array and 
## 106- Rest Pattern And Parameter
- This is just opposite of the spread operator
- we use spread operator on right hand side of the assignment operator and rest pattern on the left hand side of the assignment operator
- most important thing is it does not include skipped element, it only include rest elements after the last assigned element and that's why it is used at last of the destructuring assignment
- there can be only one rest pattern in destructuring element
- it also worked on objects
## 108- The Nullish Colaescing Operator(??)
- Nullish includes null and undefined but not zero or the empty string
## 111- For Of Loop
- This is as same as for each loop in java
- The best thing in for of loop is we can use break or continue
- **entries()** - This contains all the elements of the array along with the index number
## 112- Looping Objects: Object Keys, Values & Entries
- **Object.keys()** - It takes object as a parameters and prints all the keys of the given object
```js
const keys = Object.keys(game);
console.log(keys);
```
- in the above example keys is an array of keys 
- **Object.values()** - it takes the object as a parameter and return the array containing all the according to the keys
## 117 - Maps Fundamental
- It is like object but the difference is in objects the key is always string but in maps the key can be of any type