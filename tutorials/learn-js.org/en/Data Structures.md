Tutorial
--------
In this tutorial, you will learn about various types of data structure. We have already experienced arrays, stack, queue, and objects in previous tutorials, and we are going to learn arrays, string, set, and map more differently. Next model can choose linked list, Tree, Heap, and graphs.

### Arrays

Array stores multiple elements in a single variable. It is dynamic, meaning their size adjusts automatically as elements are added or removed. The index of the array starts from 0. 

For example:

    let arr = [1,2,3,4,5];
    console.log(arr);       // 1,2,3,4,5

Array can store multiple values of any data type together, and users can access the values through index.

    let arr = [1,"str",{}];
    console.log(arr[0]);    // 1

### String

String is a sequence of characters. In javascript, string is immutable, so a new string will be created when modification occurs.

    let str = "Hello World";
    // String is immutable, so crates a new string
    let newStr = str + "!";

    // using array as a string by using join
    let strArr = ["Hello"];
    strArr.push(" World!");
    console.log(strArr.join(""));

### Set

Set is similar to array, but it only accepts unique values. In other words, it automatically ignores duplicate values.

    let s1 = new Set([1,2,2,3,3]);
    console.log(s1);

    let s2 = new Set("Heeeello");
    console.log(s2);

    let s3 = new Set();
    console.log(s3);

- .add(value) will add an element if the value is not present in the set
- .delete(value) will delete an element in the set
- .clear() will delete every element
- .has(value) returns true if the set has the value


### Map

Map is a collection of key-value pairs.

    let m1 = new Map();
    console.log(m1);

- .set(key, value) adds an item with key and value pair if the key is not present. If there is, it changes the value according to the input
- .delete(key) deletes an item with key; paired value is also deleted
- .get(key) returns paired value
- myMap.has(value) returns true if the value is present
- .size returns the number of elements in the map
- .forEach((value, key) => { // code }); iterates over the map


Exercise
--------
Create a map with at least three elements. Create a set and store every key and value in the map. You do not need to sort it. Print the set.

Tutorial Code
-------------
let numList = new Map();
let result = new Set();

numList.set(1,1);
numList.set(2,4);
numList.set(3,9);

// TODO: store every value in key and value in the map into the set called `result`

Expected Output
---------------
Set(5) {1, 4, 2, 9, 3}

Solution
--------
let numList = new Map();
let result = new Set();

numList.set(1,1);
numList.set(2,4);
numList.set(3,9);

numList.forEach((value, key) => {
    result.add(value);
    result.add(key);
});

console.log(result);
