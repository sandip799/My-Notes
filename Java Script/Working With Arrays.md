## 142. Simple Array Methods
### Slice 
- This helps make a sallow copy of the array 
- This is as same as the **Arrays.copyOfRange()** in java or this is as same as substring method that we already discussed in java
```js
let arr = ['a', 'b', 'c', 'd'];
arr.slice(2);    op - [c, d, e]
arr.slice(2, 4); op - [c, d]; //here 4 is exclusive
arr.slice(-2);   op- [d, e] //elements from backward
arr.slice(1, -2) op- [b, c] 
arr.slice() //exactly the same array
```

### Splice
- It mutates the original array
```js
let arr = ['a', 'b', 'c', 'd'];
arr.splice(-1);    op - [a, b, c, d] //delete element from the end
arr.slice(1, 2); op - [a, d]; //first- starting index, second- no of elements to delete
```

### Reverse
- This method also mutates the original array
```js
let arr = ['a', 'b', 'c', 'd'];
arr.reverse() //reverse the array also mutates the array
```

### Concat
- This helps to concatenate 2 array
```js
let arr = ['a', 'b', 'c', 'd'];
let arr2 = ['e', 'f', 'g', 'h'];
const letters = arr.concat(arr2); //parameter - an array wih[a, b, c, d, e, f, g, h]

```

### Join
- Return a string with the separator that you passed in the parameter
```js
let arr = ['a', 'b', 'c', 'd'];
let arr2 = ['e', 'f', 'g', 'h'];
const letters = arr.concat(arr2);
console.log(letters.join(' - ')); // a - b - c - d - e ....
```

### At
- This is new methods added in ES6
- This is as same as we use subscript
```
let arr = ['a', 'b', 'c', 'd'];
console.log(arr.at(-1)); op- d
```

## 144. Looping Arrays: For Each Loop
- Continue and break statement do not work work in for each loop 
- So if you need to break out of loop on a particular condition then use for of loop else for each loop