# flattenNestedArrayJS
Setel System Reliability Assignment: Problem 2

A JS code to flatten nested array as following: [1, [2, [[3, 4], 5], 6]] => [1, 2, 3, 4, 5, 6]

## JS Sample
The sample code below is creating a function to check the array and keep flatten the array if array is found. 
```
var arr = [1, [2, [[3, 4], 5], 6]];

function flatDeep(arr, d=1) {
   return d > 0 ? arr.reduce((acc, val) => acc.concat(Array.isArray(val) ? flatDeep(val, d - 1) : val), [])
                : arr.slice();
};

// call function to flatten the nested array
flatDeep(arr, Infinity);

// check result in console.log
console.log(flatDeep(arr, Infinity));
```
