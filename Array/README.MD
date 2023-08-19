### Arrays Basics:

- Arrays are ordered collections of values, which can be of any type, enclosed in square brackets (`[]`).
- Arrays can store elements of mixed types, including other arrays.

### Creating Arrays:

1. **Array Literal:**

```javascript
let numbers = [1, 2, 3, 4, 5];
let fruits = ["apple", "banana", "orange"];
```

2. **Array Constructor:**

```javascript
let emptyArray = new Array();
let arrayWithValues = new Array(1, 2, 3);
```

### Common Array Methods:

1. **length:**
   - Returns the number of elements in the array.

2. **push(item):**
   - Adds an item to the end of the array.

3. **pop():**
   - Removes and returns the last item of the array.

4. **unshift(item):**
   - Adds an item to the beginning of the array.

5. **shift():**
   - Removes and returns the first item of the array.

6. **concat(array1, array2, ...):**
   - Combines arrays and returns a new array.

7. **join(separator):**
   - Joins array elements into a string using the specified separator.

8. **slice(startIndex, endIndex):**
   - Returns a shallow copy of a portion of the array.

9. **splice(startIndex, deleteCount, item1, item2, ...):**
   - Changes the contents of an array by removing or replacing elements.

10. **indexOf(item, startIndex):**
    - Returns the index of the first occurrence of an item.

11. **lastIndexOf(item, startIndex):**
    - Returns the index of the last occurrence of an item.

12. **forEach(callbackFunction(item, index, array)):**
    - Executes a provided function once for each array element.

13. **map(callbackFunction(item, index, array)):**
    - Creates a new array by applying a function to each element.

14. **filter(callbackFunction(item, index, array)):**
    - Creates a new array with all elements that pass a test.

15. **reduce(callbackFunction(accumulator, currentValue, index, array), initialValue):**
    - Applies a function against an accumulator and each element.

### Array Iteration:

- You can loop through array elements using `for` loops or array methods like `forEach`, `map`, and `filter`.

### Spread and Rest Operators (ES6+):

- Spread operator (`...`) unpacks array elements.
- Rest operator (`...`) collects function arguments into an array.

```javascript
let arr = [1, 2, 3];
let newArr = [...arr, 4, 5]; // Spread
function myFunction(...args) { // Rest
  console.log(args);
}
```

### Array Conversion:

- Use `toString()`, `join()`, or the `spread` operator to convert arrays to strings.
- Use `split()` to convert strings to arrays.

### Note:

- Arrays are versatile data structures used to store and manipulate collections of values.
- Explore the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) for more in-depth information on array methods and usage.

Arrays are fundamental to JavaScript and offer a wide range of tools for managing and processing data.


**Exercise 1: Count Even Numbers**

**Description:** Write a function that takes an array of numbers as input and returns the count of even numbers in the array.

**Sample Solution:**
```javascript
function countEvenNumbers(numbers) {
  let evenCount = numbers.filter(number => number % 2 === 0).length;
  return evenCount;
}

let numbers = [1, 2, 3, 4, 5, 6];
console.log(countEvenNumbers(numbers)); // Output: 3
```

**Exercise 2: Find Maximum Value**

**Description:** Write a function that finds and returns the maximum value in an array of numbers.

**Sample Solution:**
```javascript
function findMaxValue(numbers) {
  return Math.max(...numbers);
}

let numbers = [23, 8, 42, 15, 4, 10];
console.log(findMaxValue(numbers)); // Output: 42
```

**Exercise 3: Sum of Positive Numbers**

**Description:** Write a function that takes an array of numbers as input and returns the sum of all positive numbers in the array.

**Sample Solution:**
```javascript
function sumPositiveNumbers(numbers) {
  let positiveNumbers = numbers.filter(number => number > 0);
  let sum = positiveNumbers.reduce((acc, curr) => acc + curr, 0);
  return sum;
}

let numbers = [-3, 5, -7, 2, 9, -1];
console.log(sumPositiveNumbers(numbers)); // Output: 16
```

**Exercise 4: Array Reversal**

**Description:** Write a function that takes an array and returns a new array with the elements reversed.

**Sample Solution:**
```javascript
function reverseArray(arr) {
  return arr.slice().reverse();
}

let original = [1, 2, 3, 4, 5];
let reversed = reverseArray(original);
console.log(reversed); // Output: [5, 4, 3, 2, 1]
```

**Exercise 5: Extract Names**

**Description:** Write a function that takes an array of objects (each with a 'name' property) and returns an array of names.

**Sample Solution:**
```javascript
function extractNames(objects) {
  return objects.map(obj => obj.name);
}

let people = [
  { name: 'Alice' },
  { name: 'Bob' },
  { name: 'Charlie' }
];
console.log(extractNames(people)); // Output: ['Alice', 'Bob', 'Charlie']
```

**Exercise 6: Remove Duplicates**

**Description:** Write a function that removes duplicate values from an array.

**Sample Solution:**
```javascript
function removeDuplicates(arr) {
  return [...new Set(arr)];
}

let numbers = [1, 2, 2, 3, 4, 4, 5];
console.log(removeDuplicates(numbers)); // Output: [1, 2, 3, 4, 5]
```

**Exercise 7: Array Manipulation**

**Description:** Write a function that takes an array of strings and returns a new array with the lengths of each string.

**Sample Solution:**
```javascript
function getLengths(strings) {
  return strings.map(str => str.length);
}

let words = ['apple', 'banana', 'grape'];
console.log(getLengths(words)); // Output: [5, 6, 5]
```

**Exercise 8: Capitalize Names**

**Description:** Write a function that takes an array of names and returns a new array with the names capitalized.

**Sample Solution:**
```javascript
function capitalizeNames(names) {
  return names.map(name => name.charAt(0).toUpperCase() + name.slice(1));
}

let names = ['alice', 'bob', 'charlie'];
console.log(capitalizeNames(names)); // Output: ['Alice', 'Bob', 'Charlie']
```

**Exercise 9: Find Longest Word**

**Description:** Write a function that finds and returns the longest word in an array of strings.

**Sample Solution:**
```javascript
function findLongestWord(words) {
  return words.reduce((longest, current) => (current.length > longest.length ? current : longest), '');
}

let words = ['apple', 'banana', 'grapefruit', 'orange'];
console.log(findLongestWord(words)); // Output: 'grapefruit'
```

**Exercise 10: Array Sum**

**Description:** Write a function that takes an array of arrays containing numbers and returns a new array with the sums of each inner array.

**Sample Solution:**
```javascript
function sumOfArrays(arrays) {
  return arrays.map(innerArray => innerArray.reduce((sum, num) => sum + num, 0));
}

let arrays = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
console.log(sumOfArrays(arrays)); // Output: [6, 15, 24]
```

Feel free to modify these exercises or create your own variations to practice different array methods and concepts in JavaScript. The key is to progressively challenge yourself and deepen your understanding of array manipulation techniques.

Certainly, here are 10 more coding exercises that continue to build upon various array methods and concepts in JavaScript:

**Exercise 11: Array Intersection**

**Description:** Write a function that takes two arrays and returns a new array containing the elements that are common to both arrays.

**Sample Solution:**
```javascript
function arrayIntersection(arr1, arr2) {
  return arr1.filter(item => arr2.includes(item));
}

let array1 = [1, 2, 3, 4, 5];
let array2 = [3, 4, 5, 6, 7];
console.log(arrayIntersection(array1, array2)); // Output: [3, 4, 5]
```

**Exercise 12: Array Chunking**

**Description:** Write a function that takes an array and a chunk size as arguments and returns an array of arrays where each inner array has a maximum length of the chunk size.

**Sample Solution:**
```javascript
function chunkArray(arr, chunkSize) {
  let chunks = [];
  for (let i = 0; i < arr.length; i += chunkSize) {
    chunks.push(arr.slice(i, i + chunkSize));
  }
  return chunks;
}

let numbers = [1, 2, 3, 4, 5, 6, 7, 8];
console.log(chunkArray(numbers, 3)); // Output: [[1, 2, 3], [4, 5, 6], [7, 8]]
```

**Exercise 13: Array Frequency**

**Description:** Write a function that takes an array of values and returns an object with the frequency count of each value.

**Sample Solution:**
```javascript
function countFrequency(arr) {
  let frequency = {};
  arr.forEach(item => {
    frequency[item] = (frequency[item] || 0) + 1;
  });
  return frequency;
}

let values = ['apple', 'banana', 'apple', 'orange', 'banana', 'apple'];
console.log(countFrequency(values));
// Output: { apple: 3, banana: 2, orange: 1 }
```

**Exercise 14: Array Grouping**

**Description:** Write a function that takes an array of objects and groups them by a specified property.

**Sample Solution:**
```javascript
function groupByProperty(objects, property) {
  let grouped = {};
  objects.forEach(obj => {
    let key = obj[property];
    if (!grouped[key]) {
      grouped[key] = [];
    }
    grouped[key].push(obj);
  });
  return grouped;
}

let people = [
  { name: 'Alice', age: 25 },
  { name: 'Bob', age: 30 },
  { name: 'Charlie', age: 25 }
];
console.log(groupByProperty(people, 'age'));
// Output: { 25: [ { name: 'Alice', age: 25 }, { name: 'Charlie', age: 25 } ],
//            30: [ { name: 'Bob', age: 30 } ] }
```

**Exercise 15: Array Frequency Map**

**Description:** Write a function that takes an array of values and returns a map with the frequency count of each value.

**Sample Solution:**
```javascript
function countFrequencyMap(arr) {
  let frequencyMap = new Map();
  arr.forEach(item => {
    frequencyMap.set(item, (frequencyMap.get(item) || 0) + 1);
  });
  return frequencyMap;
}

let values = ['apple', 'banana', 'apple', 'orange', 'banana', 'apple'];
console.log(countFrequencyMap(values));
// Output: Map(3) { 'apple' => 3, 'banana' => 2, 'orange' => 1 }
```

**Exercise 16: Flatten Nested Arrays**

**Description:** Write a function that takes an array with nested arrays and returns a flat array.

**Sample Solution:**
```javascript
function flattenArray(arrays) {
  return arrays.reduce((flat, innerArray) => flat.concat(innerArray), []);
}

let nestedArrays = [[1, 2], [3, 4], [5, 6]];
console.log(flattenArray(nestedArrays)); // Output: [1, 2, 3, 4, 5, 6]
```

**Exercise 17: Capitalize Long Words**

**Description:** Write a function that takes an array of words and returns a new array with words longer than a specified length capitalized.

**Sample Solution:**
```javascript
function capitalizeLongWords(words, minLength) {
  return words.map(word => (word.length > minLength ? word.toUpperCase() : word));
}

let words = ['apple', 'banana', 'grape', 'orange'];
console.log(capitalizeLongWords(words, 5)); // Output: ['apple', 'banana', 'GRAPE', 'ORANGE']
```

**Exercise 18: Array Shuffling**

**Description:** Write a function that shuffles the elements of an array randomly.

**Sample Solution:**
```javascript
function shuffleArray(arr) {
  let shuffled = [...arr];
  for (let i = shuffled.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [shuffled[i], shuffled[j]] = [shuffled[j], shuffled[i]];
  }
  return shuffled;
}

let numbers = [1, 2, 3, 4, 5];
console.log(shuffleArray(numbers)); // Output: [3, 2, 4, 5, 1] (random order)
```

**Exercise 19: Array Average**

**Description:** Write a function that takes an array of numbers

 and returns the average value.

**Sample Solution:**
```javascript
function calculateAverage(numbers) {
  let sum = numbers.reduce((acc, curr) => acc + curr, 0);
  return sum / numbers.length;
}

let scores = [85, 90, 78, 92, 88];
console.log(calculateAverage(scores)); // Output: 86.6
```

**Exercise 20: Array Rotation**

**Description:** Write a function that rotates the elements of an array to the left by a given number of positions.

**Sample Solution:**
```javascript
function rotateArrayLeft(arr, positions) {
  let rotated = [...arr];
  for (let i = 0; i < positions; i++) {
    let firstElement = rotated.shift();
    rotated.push(firstElement);
  }
  return rotated;
}

let numbers = [1, 2, 3, 4, 5];
console.log(rotateArrayLeft(numbers, 2)); // Output: [3, 4, 5, 1, 2]
```

These additional exercises further explore various array methods and concepts, providing a diverse range of challenges to enhance your skills and understanding of JavaScript arrays.

Certainly, let's continue with more coding exercises that delve into advanced array concepts in JavaScript:

**Exercise 21: Unique Subsets**

**Description:** Write a function that takes an array of numbers and returns an array of unique subsets (combinations) of those numbers.

**Sample Solution:**
```javascript
function generateSubsets(arr) {
  let subsets = [[]];

  for (let num of arr) {
    const subsetCount = subsets.length;
    for (let i = 0; i < subsetCount; i++) {
      const newSubset = [...subsets[i], num];
      subsets.push(newSubset);
    }
  }

  return subsets;
}

let numbers = [1, 2, 3];
console.log(generateSubsets(numbers));
// Output: [[], [1], [2], [1, 2], [3], [1, 3], [2, 3], [1, 2, 3]]
```

**Exercise 22: Array Partition**

**Description:** Write a function that takes an array of numbers and an integer value `k`, and partitions the array into subarrays where the sum of the elements in each subarray is less than or equal to `k`.

**Sample Solution:**
```javascript
function partitionArray(arr, k) {
  let partitions = [];
  let currentPartition = [];

  for (let num of arr) {
    if (currentPartition.reduce((sum, n) => sum + n, 0) + num <= k) {
      currentPartition.push(num);
    } else {
      partitions.push(currentPartition);
      currentPartition = [num];
    }
  }

  if (currentPartition.length > 0) {
    partitions.push(currentPartition);
  }

  return partitions;
}

let numbers = [1, 2, 3, 4, 5];
console.log(partitionArray(numbers, 7));
// Output: [[1, 2, 3], [4], [5]]
```

**Exercise 23: Array Zip**

**Description:** Write a function that takes two arrays and interleaves their elements to create a new array.

**Sample Solution:**
```javascript
function zipArrays(arr1, arr2) {
  let zipped = [];
  let length = Math.min(arr1.length, arr2.length);

  for (let i = 0; i < length; i++) {
    zipped.push(arr1[i], arr2[i]);
  }

  return zipped.concat(arr1.slice(length), arr2.slice(length));
}

let array1 = [1, 3, 5];
let array2 = [2, 4, 6, 8];
console.log(zipArrays(array1, array2)); // Output: [1, 2, 3, 4, 5, 6, 8]
```

**Exercise 24: Array Rotation (Advanced)**

**Description:** Write a function that rotates the elements of an array to the right by a given number of positions.

**Sample Solution:**
```javascript
function rotateArrayRight(arr, positions) {
  let rotated = [...arr];
  for (let i = 0; i < positions; i++) {
    let lastElement = rotated.pop();
    rotated.unshift(lastElement);
  }
  return rotated;
}

let numbers = [1, 2, 3, 4, 5];
console.log(rotateArrayRight(numbers, 2)); // Output: [4, 5, 1, 2, 3]
```

**Exercise 25: Array Partitioning (Advanced)**

**Description:** Write a function that takes an array of numbers and returns an array with two subarrays, one containing the even numbers and the other containing the odd numbers.

**Sample Solution:**
```javascript
function partitionEvenOdd(arr) {
  let evenNumbers = arr.filter(num => num % 2 === 0);
  let oddNumbers = arr.filter(num => num % 2 !== 0);
  return [evenNumbers, oddNumbers];
}

let numbers = [1, 2, 3, 4, 5, 6, 7];
console.log(partitionEvenOdd(numbers)); // Output: [[2, 4, 6], [1, 3, 5, 7]]
```

These advanced exercises build upon the concepts of array manipulation and provide challenges that require a deeper understanding of array methods and logic. Working through these exercises will help solidify your proficiency in handling arrays effectively in JavaScript.

Absolutely, let's continue with more advanced coding exercises that involve complex array manipulations and challenges:

**Exercise 26: Array Intersection (Advanced)**

**Description:** Write a function that finds the intersection of multiple arrays (common elements in all arrays).

**Sample Solution:**
```javascript
function arrayIntersectionAdvanced(arrays) {
  return arrays.reduce((intersection, currentArray) => {
    return intersection.filter(element => currentArray.includes(element));
  });
}

let arrays = [[1, 2, 3, 4], [3, 4, 5, 6], [4, 5, 6, 7]];
console.log(arrayIntersectionAdvanced(arrays)); // Output: [4]
```

**Exercise 27: Array Flattening (Advanced)**

**Description:** Write a function that recursively flattens an array that contains nested arrays at various levels.

**Sample Solution:**
```javascript
function deepFlatten(arr) {
  return arr.reduce((flat, item) => {
    return flat.concat(Array.isArray(item) ? deepFlatten(item) : item);
  }, []);
}

let nestedArray = [1, [2, [3, 4]], 5, [6]];
console.log(deepFlatten(nestedArray)); // Output: [1, 2, 3, 4, 5, 6]
```

**Exercise 28: Array Splicing**

**Description:** Write a function that takes an array and a set of indices to remove, and returns a new array with the elements at those indices removed.

**Sample Solution:**
```javascript
function removeElementsByIndices(arr, indicesToRemove) {
  return arr.filter((_, index) => !indicesToRemove.includes(index));
}

let numbers = [1, 2, 3, 4, 5];
let indicesToRemove = [1, 3];
console.log(removeElementsByIndices(numbers, indicesToRemove)); // Output: [1, 3, 5]
```

**Exercise 29: Array Grouping by Key**

**Description:** Write a function that groups objects in an array by a specific key and returns an object where each key corresponds to an array of objects with that key.

**Sample Solution:**
```javascript
function groupByPropertyAdvanced(objects, property) {
  return objects.reduce((grouped, obj) => {
    const key = obj[property];
    if (!grouped[key]) {
      grouped[key] = [];
    }
    grouped[key].push(obj);
    return grouped;
  }, {});
}

let people = [
  { name: 'Alice', age: 25 },
  { name: 'Bob', age: 30 },
  { name: 'Charlie', age: 25 }
];
console.log(groupByPropertyAdvanced(people, 'age'));
// Output: { 25: [ { name: 'Alice', age: 25 }, { name: 'Charlie', age: 25 } ],
//            30: [ { name: 'Bob', age: 30 } ] }
```

**Exercise 30: Array Rotation (Circular)**

**Description:** Write a function that rotates the elements of an array to the right by a given number of positions, considering the rotation as circular.

**Sample Solution:**
```javascript
function rotateArrayCircular(arr, positions) {
  if (arr.length === 0) return arr;
  const effectivePositions = positions % arr.length;
  const rotated = [...arr.slice(-effectivePositions), ...arr.slice(0, -effectivePositions)];
  return rotated;
}

let numbers = [1, 2, 3, 4, 5];
console.log(rotateArrayCircular(numbers, 8)); // Output: [3, 4, 5, 1, 2]
```

**Exercise 31: Array Filtering (Chaining)**

**Description:** Write a function that takes an array of numbers, filters out the odd numbers, squares the remaining even numbers, and returns a new array.

**Sample Solution:**
```javascript
function filterAndSquare(arr) {
  return arr.filter(num => num % 2 === 0).map(num => num * num);
}

let numbers = [1, 2, 3, 4, 5, 6];
console.log(filterAndSquare(numbers)); // Output: [4, 16, 36]
```

These advanced coding exercises challenge you to apply a combination of array methods and logical thinking to solve more complex problems. Practicing these exercises will strengthen your ability to effectively manipulate arrays and creatively solve array-related challenges in JavaScript.

Certainly, let's continue with more advanced coding exercises that build upon complex array manipulations and problem-solving:

**Exercise 32: Array Mapping and Reducing**

**Description:** Write a function that takes an array of strings and returns the total character count of all strings combined.

**Sample Solution:**
```javascript
function totalCharacterCount(strings) {
  return strings.map(str => str.length).reduce((total, length) => total + length, 0);
}

let words = ['apple', 'banana', 'grape', 'orange'];
console.log(totalCharacterCount(words)); // Output: 21
```

**Exercise 33: Array Chunking (Advanced)**

**Description:** Write a function that takes an array and a chunk size as arguments and returns an array of arrays, ensuring that each inner array has a sum of elements as close to the target sum as possible.

**Sample Solution:**
```javascript
function chunkArrayClosestSum(arr, chunkSize, targetSum) {
  arr.sort((a, b) => b - a);
  let chunks = [];

  while (arr.length > 0) {
    let chunk = [arr.shift()];

    while (chunk.reduce((sum, num) => sum + num, 0) < targetSum && arr.length > 0) {
      chunk.push(arr.shift());
    }

    chunks.push(chunk);
  }

  return chunks;
}

let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9];
console.log(chunkArrayClosestSum(numbers, 3, 15));
// Output: [[9, 6], [8, 5, 2], [7, 4, 3, 1]]
```

**Exercise 34: Array Transformation**

**Description:** Write a function that takes an array of strings and returns a new array with the strings sorted by the total count of vowels (a, e, i, o, u) they contain.

**Sample Solution:**
```javascript
function sortByVowelCount(strings) {
  const vowelCount = str => str.split('').filter(char => 'aeiouAEIOU'.includes(char)).length;
  return strings.sort((a, b) => vowelCount(b) - vowelCount(a));
}

let words = ['apple', 'banana', 'grape', 'orange'];
console.log(sortByVowelCount(words)); // Output: ['apple', 'orange', 'grape', 'banana']
```

**Exercise 35: Array Intersection (Multiple Arrays)**

**Description:** Write a function that finds the intersection of multiple arrays (elements common to all arrays) without using nested loops.

**Sample Solution:**
```javascript
function multiArrayIntersection(arrays) {
  const allElements = [].concat(...arrays);
  return [...new Set(allElements)].filter(element =>
    arrays.every(arr => arr.includes(element))
  );
}

let arrays = [[1, 2, 3, 4], [3, 4, 5, 6], [4, 5, 6, 7]];
console.log(multiArrayIntersection(arrays)); // Output: [4]
```

**Exercise 36: Array Combining**

**Description:** Write a function that combines two arrays, alternating elements from each array, until both arrays are exhausted.

**Sample Solution:**
```javascript
function combineArraysAlternate(arr1, arr2) {
  let combined = [];
  let maxLength = Math.max(arr1.length, arr2.length);

  for (let i = 0; i < maxLength; i++) {
    if (i < arr1.length) combined.push(arr1[i]);
    if (i < arr2.length) combined.push(arr2[i]);
  }

  return combined;
}

let array1 = [1, 3, 5];
let array2 = [2, 4, 6, 8];
console.log(combineArraysAlternate(array1, array2)); // Output: [1, 2, 3, 4, 5, 6, 8]
```

**Exercise 37: Array Transformation (Advanced)**

**Description:** Write a function that takes an array of numbers and returns a new array with elements sorted in descending order based on the sum of their digits.

**Sample Solution:**
```javascript
function sortByDigitSum(numbers) {
  const digitSum = num => num.toString().split('').map(Number).reduce((sum, digit) => sum + digit, 0);
  return numbers.sort((a, b) => digitSum(b) - digitSum(a));
}

let values = [123, 54, 89, 27, 66];
console.log(sortByDigitSum(values)); // Output: [123, 27, 54, 66, 89]
```

**Exercise 38: Array Range**

**Description:** Write a function that generates an array of numbers within a given range, including both endpoints.

**Sample Solution:**
```javascript
function generateRange(start, end) {
  return Array.from({ length: end - start + 1 }, (_, index) => start + index);
}

console.log(generateRange(3, 8)); // Output: [3, 4, 5, 6, 7, 8]
```

**Exercise 39: Array Intersection (Multiple Arrays, Set Approach)**

**Description:** Write a function that finds the intersection of multiple arrays (common elements in all arrays) using a set-based approach.

**Sample Solution:**
```javascript
function multiArrayIntersectionSet(arrays) {
  if (arrays.length === 0) return [];
  if (arrays.length === 1) return arrays[0];
  
  let intersection = new Set(arrays[0]);
  
  for (let i = 1; i < arrays.length; i++) {
    intersection = new Set(arrays[i].filter(element => intersection.has(element)));
  }
  
  return [...intersection];
}

let arrays = [[1, 2, 3, 4], [3, 4, 5, 6], [4, 5, 6, 7]];
console.log(multiArrayIntersectionSet(arrays)); // Output: [4]
```

**Exercise 40: Array Majority Element**

**Description:** Write a function that finds the majority element in an array (the element that appears more than half the length of the array).

**Sample Solution:**
```javascript
function findMajorityElement(arr) {
  const counts = {};
  const halfLength = Math.floor(arr.length / 2);

  for (let num of arr) {
    counts[num] = (counts[num] || 0) + 1;
    if (counts[num] > halfLength) return num;
  }

  return null;
}

let numbers = [2, 2, 3, 2, 4, 2, 5];
console.log(findMajorityElement(numbers)); // Output: 
```javascript
2
```

**Exercise 41: Array Transforming**

**Description:** Write a function that takes an array of strings and returns an array where each string is repeated a number of times based on its length.

**Sample Solution:**
```javascript
function repeatBasedOnLength(strings) {
  return strings.flatMap(str => Array.from({ length: str.length }, () => str));
}

let words = ['apple', 'banana', 'grape'];
console.log(repeatBasedOnLength(words));
// Output: ['apple', 'apple', 'apple', 'banana', 'banana', 'grape', 'grape', 'grape', 'grape']
```

**Exercise 42: Array Frequency Distribution**

**Description:** Write a function that takes an array of numbers and returns an object where each unique number is a key, and the value is the frequency of that number.

**Sample Solution:**
```javascript
function frequencyDistribution(arr) {
  return arr.reduce((freq, num) => {
    freq[num] = (freq[num] || 0) + 1;
    return freq;
  }, {});
}

let numbers = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4];
console.log(frequencyDistribution(numbers));
// Output: { 1: 1, 2: 2, 3: 3, 4: 4 }
```

**Exercise 43: Array Shifting**

**Description:** Write a function that takes an array and a number of positions to shift, and returns a new array with elements shifted to the right.

**Sample Solution:**
```javascript
function shiftArray(arr, positions) {
  const effectivePositions = positions % arr.length;
  return [...arr.slice(-effectivePositions), ...arr.slice(0, -effectivePositions)];
}

let numbers = [1, 2, 3, 4, 5];
console.log(shiftArray(numbers, 2)); // Output: [4, 5, 1, 2, 3]
```

**Exercise 44: Array Pair Sums**

**Description:** Write a function that takes an array of numbers and a target sum, and returns an array of pairs that add up to the target sum.

**Sample Solution:**
```javascript
function findPairSums(arr, targetSum) {
  const pairs = [];

  const visited = new Set();
  for (let num of arr) {
    const complement = targetSum - num;
    if (visited.has(complement)) {
      pairs.push([num, complement]);
    }
    visited.add(num);
  }

  return pairs;
}

let numbers = [2, 4, 3, 6, 5, 1];
let target = 7;
console.log(findPairSums(numbers, target)); // Output: [[4, 3], [6, 1]]
```

**Exercise 45: Array Prefix Sums**

**Description:** Write a function that takes an array of numbers and returns an array of prefix sums, where each element is the sum of all preceding elements.

**Sample Solution:**
```javascript
function calculatePrefixSums(arr) {
  let prefixSums = [arr[0]];
  for (let i = 1; i < arr.length; i++) {
    prefixSums[i] = prefixSums[i - 1] + arr[i];
  }
  return prefixSums;
}

let numbers = [1, 2, 3, 4, 5];
console.log(calculatePrefixSums(numbers)); // Output: [1, 3, 6, 10, 15]
```

These advanced coding exercises continue to challenge your array manipulation skills and problem-solving abilities in JavaScript. Each exercise provides a unique perspective on how to creatively use array methods to solve complex tasks.

Absolutely, let's continue exploring more advanced array manipulation and problem-solving exercises in JavaScript:

**Exercise 46: Array Difference**

**Description:** Write a function that takes two arrays and returns an array containing elements that are in the first array but not in the second array.

**Sample Solution:**
```javascript
function arrayDifference(arr1, arr2) {
  return arr1.filter(element => !arr2.includes(element));
}

let array1 = [1, 2, 3, 4, 5];
let array2 = [3, 4, 5, 6, 7];
console.log(arrayDifference(array1, array2)); // Output: [1, 2]
```

**Exercise 47: Array Symmetric Difference**

**Description:** Write a function that takes two arrays and returns an array containing elements that are in either of the arrays, but not in both arrays.

**Sample Solution:**
```javascript
function arraySymmetricDifference(arr1, arr2) {
  const diff1 = arr1.filter(element => !arr2.includes(element));
  const diff2 = arr2.filter(element => !arr1.includes(element));
  return [...diff1, ...diff2];
}

let array1 = [1, 2, 3, 4, 5];
let array2 = [3, 4, 5, 6, 7];
console.log(arraySymmetricDifference(array1, array2)); // Output: [1, 2, 6, 7]
```

**Exercise 48: Array Combinations**

**Description:** Write a function that takes an array of numbers and a target sum, and returns an array of all unique combinations of numbers that add up to the target sum.

**Sample Solution:**
```javascript
function findCombinationSum(arr, targetSum) {
  const combinations = [];

  function backtrack(startIndex, currentSum, currentCombination) {
    if (currentSum === targetSum) {
      combinations.push([...currentCombination]);
      return;
    }

    for (let i = startIndex; i < arr.length; i++) {
      if (currentSum + arr[i] <= targetSum) {
        currentCombination.push(arr[i]);
        backtrack(i, currentSum + arr[i], currentCombination);
        currentCombination.pop();
      }
    }
  }

  backtrack(0, 0, []);
  return combinations;
}

let numbers = [2, 3, 6, 7];
let target = 7;
console.log(findCombinationSum(numbers, target));
// Output: [[2, 2, 3], [7]]
```

**Exercise 49: Array Sum Closest to Target**

**Description:** Write a function that takes an array of numbers and a target sum, and returns the sum of the closest combination of numbers to the target sum.

**Sample Solution:**
```javascript
function findClosestSum(arr, targetSum) {
  arr.sort((a, b) => a - b);

  let closestSum = Infinity;
  let minDiff = Infinity;

  for (let i = 0; i < arr.length - 2; i++) {
    let left = i + 1;
    let right = arr.length - 1;

    while (left < right) {
      let currentSum = arr[i] + arr[left] + arr[right];
      let currentDiff = Math.abs(currentSum - targetSum);

      if (currentDiff < minDiff) {
        minDiff = currentDiff;
        closestSum = currentSum;
      }

      if (currentSum < targetSum) {
        left++;
      } else {
        right--;
      }
    }
  }

  return closestSum;
}

let numbers = [1, 2, 3, 4, 5];
let target = 10;
console.log(findClosestSum(numbers, target)); // Output: 10 (4 + 5 + 1)
```

**Exercise 50: Array Zigzag Conversion**

**Description:** Write a function that takes a string and an integer `n` representing the number of rows, and converts the string into a zigzag pattern with `n` rows.

**Sample Solution:**
```javascript
function convertToZigzag(s, numRows) {
  if (numRows === 1) return s;

  const rows = Array.from({ length: numRows }, () => []);
  let currentRow = 0;
  let direction = -1;

  for (let char of s) {
    rows[currentRow].push(char);
    if (currentRow === 0 || currentRow === numRows - 1) {
      direction *= -1;
    }
    currentRow += direction;
  }

  return rows.flat().join('');
}

let input = 'PAYPALISHIRING';
let numRows = 3;
console.log(convertToZigzag(input, numRows));
// Output: 'PAHNAPLSIIGYIR'
```

These advanced coding exercises continue to challenge your array manipulation skills and problem-solving abilities in JavaScript. Each exercise provides a unique perspective on how to creatively use array methods to solve complex tasks.

Certainly, let's continue exploring more advanced array manipulation and problem-solving exercises in JavaScript:

**Exercise 51: Longest Consecutive Sequence**

**Description:** Write a function that takes an array of numbers and returns the length of the longest consecutive subsequence of numbers in the array.

**Sample Solution:**
```javascript
function longestConsecutiveSequence(nums) {
  const numSet = new Set(nums);
  let longestStreak = 0;

  for (let num of numSet) {
    if (!numSet.has(num - 1)) {
      let currentNum = num;
      let currentStreak = 1;

      while (numSet.has(currentNum + 1)) {
        currentNum += 1;
        currentStreak += 1;
      }

      longestStreak = Math.max(longestStreak, currentStreak);
    }
  }

  return longestStreak;
}

let numbers = [100, 4, 200, 1, 3, 2];
console.log(longestConsecutiveSequence(numbers)); // Output: 4 (1, 2, 3, 4)
```

**Exercise 52: Array 2D Rotation**

**Description:** Write a function that rotates a 2D matrix (an array of arrays) 90 degrees clockwise.

**Sample Solution:**
```javascript
function rotateMatrix(matrix) {
  const n = matrix.length;
  const rotated = new Array(n).fill(null).map(() => new Array(n).fill(null));

  for (let row = 0; row < n; row++) {
    for (let col = 0; col < n; col++) {
      rotated[col][n - row - 1] = matrix[row][col];
    }
  }

  return rotated;
}

let matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];
console.log(rotateMatrix(matrix));
// Output: [ [7, 4, 1], [8, 5, 2], [9, 6, 3] ]
```

**Exercise 53: Array Spiral Order**

**Description:** Write a function that takes a 2D matrix and returns an array containing its elements in spiral order.

**Sample Solution:**
```javascript
function spiralOrder(matrix) {
  const result = [];

  while (matrix.length > 0) {
    result.push(...matrix.shift());
    for (let row of matrix) {
      if (row.length > 0) {
        result.push(row.pop());
      }
    }
    if (matrix.length > 0) {
      result.push(...matrix.pop().reverse());
    }
    for (let i = matrix.length - 1; i >= 0; i--) {
      if (matrix[i].length > 0) {
        result.push(matrix[i].shift());
      }
    }
  }

  return result;
}

let matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];
console.log(spiralOrder(matrix)); // Output: [1, 2, 3, 6, 9, 8, 7, 4, 5]
```

**Exercise 54: Array Sorting (Custom Order)**

**Description:** Write a function that takes an array of strings and a custom order string, and sorts the array according to the order defined in the custom order string.

**Sample Solution:**
```javascript
function customSort(strings, order) {
  const orderMap = new Map([...order].map((char, index) => [char, index]));
  return strings.sort((a, b) => (orderMap.get(a) || Infinity) - (orderMap.get(b) || Infinity));
}

let words = ['banana', 'apple', 'cherry', 'date'];
let customOrder = 'nphltcdaiebr';
console.log(customSort(words, customOrder)); // Output: ['banana', 'cherry', 'apple', 'date']
```

**Exercise 55: Array Submatrix**

**Description:** Write a function that takes a 2D matrix and two pairs of indices representing the top-left and bottom-right corners of a submatrix, and returns the submatrix.

**Sample Solution:**
```javascript
function submatrix(matrix, topLeft, bottomRight) {
  const sub = [];
  for (let row = topLeft[0]; row <= bottomRight[0]; row++) {
    sub.push(matrix[row].slice(topLeft[1], bottomRight[1] + 1));
  }
  return sub;
}

let matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];
let topLeft = [0, 1];
let bottomRight = [1, 2];
console.log(submatrix(matrix, topLeft, bottomRight));
// Output: [ [2, 3], [5, 6] ]
```

**Exercise 56: Array Matrix Multiplication**

**Description:** Write a function that takes two matrices and returns the result of their multiplication.

**Sample Solution:**
```javascript
function matrixMultiplication(matrix1, matrix2) {
  const result = new Array(matrix1.length).fill(null).map(() => new Array(matrix2[0].length).fill(0));

  for (let i = 0; i < matrix1.length; i++) {
    for (let j = 0; j < matrix2[0].length; j++) {
      for (let k = 0; k < matrix2.length; k++) {
        result[i][j] += matrix1[i][k] * matrix2[k][j];
      }
    }
  }

  return result;
}

let matrix1 = [
  [1, 2],
  [3, 4]
];
let matrix2 = [
  [5, 6],
  [7, 8]
];
console.log(matrixMultiplication(matrix1, matrix2));
// Output: [ [19, 22], [43, 50] ]
```

**Exercise 57: Array Rotated Sorted Search**

**Description:** Write a function that performs a binary search on a rotated sorted array and returns the index of a target element if found, otherwise returns -1.

**Sample Solution:**
```javascript
function rotatedSortedSearch(nums, target) {
  let left = 0;
  let right = nums.length - 1;

  while (left <= right) {
    let mid = Math.floor((left + right) / 2);

    if (nums[mid] === target) {
      return mid;
    }

    if (nums[left] <= nums[mid]) {
      if (nums[left] <= target && target < nums[mid]) {
        right = mid - 1;
      } else {
        left = mid + 1;
      }
    } else {
      if (nums[mid] < target && target <= nums[right]) {
        left = mid + 1;
      } else {
        right = mid - 1;
      }
    }
  }

  return -1;
}

let rotatedArray = [4, 5, 6, 7, 0, 1, 2];
let target = 0;
console.log(rotatedSortedSearch(rotatedArray, target)); // Output: 4 (index of target 0)
```

**Exercise 58: Array Leaders**

**Description:** Write a function that takes an array of numbers and returns an array containing all the leaders in the array. A leader is an element that is greater than all the elements to its right.

**Sample Solution:**
```javascript
function findLeaders(arr) {
  const leaders = [];
  let maxRight = -1;

  for (let i = arr.length - 1; i >= 0; i--) {
    if (arr[i] > maxRight) {
      leaders.unshift(arr[i]);
      maxRight = arr[i];
    }
  }

  return leaders;
}

let numbers = [16, 17, 4, 3, 5, 2];
console.log(findLeaders(numbers)); // Output: [17, 5, 2]
```

**Exercise 59: Array Peaks and Valleys**

**Description:** Write a function that takes an array of integers and rearranges it into an alternating sequence of peaks and valleys. A peak is an element greater than its neighbors, and a valley is an element less than its neighbors.

**Sample Solution:**
```javascript
function rearrangePeaksValleys(arr) {
  arr.sort((a, b) => a - b);

  for (let i = 1; i < arr.length; i += 2) {
    [arr[i], arr[i - 1]] = [arr[i - 1], arr[i]];
  }

  return arr;
}

let numbers = [5, 3, 1, 2, 3];
console.log(rearrangePeaksValleys(numbers)); // Output: [3, 5, 1, 3, 2]
```

**Exercise 60: Array Longest Increasing Subsequence**

**Description:** Write a function that takes an array of numbers and returns the length of the longest increasing subsequence in the array.

**Sample Solution:**
```javascript
function longestIncreasingSubsequence(nums) {
  const dp = new Array(nums.length).fill(1);

  for (let i = 0; i < nums.length; i++) {
    for (let j = 0; j < i; j++) {
      if (nums[i] > nums[j]) {
        dp[i] = Math.max(dp[i], dp[j] + 1);
      }
    }
  }

  return Math.max(...dp);
}

let numbers = [10, 22, 9, 33, 21, 50, 41, 60, 80];
console.log(longestIncreasingSubsequence(numbers)); // Output: 6
```

These advanced coding exercises continue to challenge your array manipulation skills and problem-solving abilities in JavaScript. Each exercise provides a unique perspective on how to creatively use array methods to solve complex tasks. As you tackle these exercises, you'll gain a deeper understanding of array algorithms and sharpen your coding skills.
Of course, let's continue with more advanced array manipulation and problem-solving exercises:

**Exercise 61: Subarray Sum Equals K**

**Description:** Write a function that takes an array of integers and an integer k, and returns the total number of continuous subarrays whose sum equals k.

**Sample Solution:**
```javascript
function subarraySum(nums, k) {
  const sumMap = new Map();
  let count = 0;
  let sum = 0;

  sumMap.set(0, 1);

  for (let num of nums) {
    sum += num;
    if (sumMap.has(sum - k)) {
      count += sumMap.get(sum - k);
    }
    sumMap.set(sum, (sumMap.get(sum) || 0) + 1);
  }

  return count;
}

let numbers = [1, 1, 1];
let k = 2;
console.log(subarraySum(numbers, k)); // Output: 2 (Two subarrays [1, 1] and [1, 1])
```

**Exercise 62: Array Partitioning**

**Description:** Write a function that takes an array of numbers and an integer k, and rearranges the array such that all elements smaller than k are placed before elements greater than or equal to k.

**Sample Solution:**
```javascript
function partitionArray(arr, k) {
  let left = 0;
  let right = arr.length - 1;

  while (left <= right) {
    while (arr[left] < k) {
      left++;
    }
    while (arr[right] >= k) {
      right--;
    }
    if (left <= right) {
      [arr[left], arr[right]] = [arr[right], arr[left]];
      left++;
      right--;
    }
  }

  return arr;
}

let numbers = [9, 7, 3, 5, 6, 8, 1, 2];
let k = 5;
console.log(partitionArray(numbers, k)); // Output: [3, 1, 2, 5, 6, 8, 9, 7]
```

**Exercise 63: Word Search**

**Description:** Write a function that takes a 2D board and a word, and returns true if the word exists in the board by connecting adjacent letters horizontally or vertically.

**Sample Solution:**
```javascript
function exist(board, word) {
  const directions = [[-1, 0], [1, 0], [0, -1], [0, 1]];

  function dfs(row, col, index) {
    if (index === word.length) {
      return true;
    }

    if (
      row < 0 ||
      row >= board.length ||
      col < 0 ||
      col >= board[0].length ||
      board[row][col] !== word[index]
    ) {
      return false;
    }

    const original = board[row][col];
    board[row][col] = '#';

    for (let [dx, dy] of directions) {
      if (dfs(row + dx, col + dy, index + 1)) {
        return true;
      }
    }

    board[row][col] = original;
    return false;
  }

  for (let i = 0; i < board.length; i++) {
    for (let j = 0; j < board[0].length; j++) {
      if (dfs(i, j, 0)) {
        return true;
      }
    }
  }

  return false;
}

let board = [
  ['A', 'B', 'C', 'E'],
  ['S', 'F', 'C', 'S'],
  ['A', 'D', 'E', 'E']
];
let word = 'ABCCED';
console.log(exist(board, word)); // Output: true
```

**Exercise 64: Array Target Sum**

**Description:** Write a function that takes an array of integers and a target sum, and returns all pairs of numbers that add up to the target sum.

**Sample Solution:**
```javascript
function findTargetSumPairs(nums, target) {
  const numCount = new Map();
  const pairs = [];

  for (let num of nums) {
    const complement = target - num;
    if (numCount.has(complement)) {
      pairs.push([num, complement]);
    }
    numCount.set(num, (numCount.get(num) || 0) + 1);
  }

  return pairs;
}

let numbers = [2, 4, 3, 6, 5, 1];
let target = 7;
console.log(findTargetSumPairs(numbers, target)); // Output: [[4, 3], [6, 1]]
```

**Exercise 65: Longest Palindromic Substring**

**Description:** Write a function that takes a string and returns the longest palindromic substring within the string.

**Sample Solution:**
```javascript
function longestPalindromicSubstring(s) {
  let longest = '';

  for (let i = 0; i < s.length; i++) {
    let oddPalindrome = expandAroundCenter(s, i, i);
    let evenPalindrome = expandAroundCenter(s, i, i + 1);

    let currentLongest = oddPalindrome.length > evenPalindrome.length ? oddPalindrome : evenPalindrome;

    if (currentLongest.length > longest.length) {
      longest = currentLongest;
    }
  }

  return longest;
}

function expandAroundCenter(s, left, right) {
  while (left >= 0 && right < s.length && s[left] === s[right]) {
    left--;
    right++;
  }
  return s.substring(left + 1, right);
}

let input = 'babad';
console.log(longestPalindromicSubstring(input)); // Output: 'bab' or 'aba'
```

These exercises continue to delve into advanced array manipulation and problem-solving scenarios in JavaScript. By working through these exercises, you'll gain a deeper understanding of complex algorithms and strategies for efficiently solving a variety of array-related challenges.
Absolutely, let's continue exploring more advanced array manipulation and problem-solving exercises:

**Exercise 66: Container With Most Water**

**Description:** Write a function that takes an array of non-negative integers representing vertical lines and returns the maximum area formed between any two lines.

**Sample Solution:**
```javascript
function maxArea(height) {
  let max = 0;
  let left = 0;
  let right = height.length - 1;

  while (left < right) {
    max = Math.max(max, Math.min(height[left], height[right]) * (right - left));
    if (height[left] < height[right]) {
      left++;
    } else {
      right--;
    }
  }

  return max;
}

let heights = [1, 8, 6, 2, 5, 4, 8, 3, 7];
console.log(maxArea(heights)); // Output: 49
```

**Exercise 67: Largest Rectangle in Histogram**

**Description:** Write a function that takes an array of non-negative integers representing the heights of a histogram, and returns the area of the largest rectangle that can be formed within the histogram.

**Sample Solution:**
```javascript
function largestRectangleArea(heights) {
  const stack = [];
  let maxArea = 0;

  for (let i = 0; i <= heights.length; i++) {
    while (stack.length > 0 && (i === heights.length || heights[i] < heights[stack[stack.length - 1]])) {
      const height = heights[stack.pop()];
      const width = stack.length === 0 ? i : i - stack[stack.length - 1] - 1;
      maxArea = Math.max(maxArea, height * width);
    }
    stack.push(i);
  }

  return maxArea;
}

let heights = [2, 1, 5, 6, 2, 3];
console.log(largestRectangleArea(heights)); // Output: 10
```

**Exercise 68: Trapping Rain Water**

**Description:** Write a function that takes an array of non-negative integers representing the heights of walls and calculates how much rainwater can be trapped.

**Sample Solution:**
```javascript
function trap(height) {
  let left = 0;
  let right = height.length - 1;
  let leftMax = 0;
  let rightMax = 0;
  let trappedWater = 0;

  while (left < right) {
    if (height[left] < height[right]) {
      if (height[left] >= leftMax) {
        leftMax = height[left];
      } else {
        trappedWater += leftMax - height[left];
      }
      left++;
    } else {
      if (height[right] >= rightMax) {
        rightMax = height[right];
      } else {
        trappedWater += rightMax - height[right];
      }
      right--;
    }
  }

  return trappedWater;
}

let heights = [0, 1, 0, 2, 1, 0, 1, 3, 2, 1, 2, 1];
console.log(trap(heights)); // Output: 6
```

**Exercise 69: Jump Game**

**Description:** Write a function that takes an array of non-negative integers where each element represents your maximum jump length. Determine if you can reach the last index.

**Sample Solution:**
```javascript
function canJump(nums) {
  let maxReach = 0;

  for (let i = 0; i < nums.length; i++) {
    if (i > maxReach) {
      return false;
    }
    maxReach = Math.max(maxReach, i + nums[i]);
  }

  return true;
}

let jumpArray = [2, 3, 1, 1, 4];
console.log(canJump(jumpArray)); // Output: true
```

**Exercise 70: Jump Game II**

**Description:** Write a function that takes an array of non-negative integers where each element represents your maximum jump length. Return the minimum number of jumps needed to reach the last index.

**Sample Solution:**
```javascript
function jump(nums) {
  let steps = 0;
  let currentJumpEnd = 0;
  let maxReach = 0;

  for (let i = 0; i < nums.length - 1; i++) {
    maxReach = Math.max(maxReach, i + nums[i]);
    if (i === currentJumpEnd) {
      steps++;
      currentJumpEnd = maxReach;
    }
  }

  return steps;
}

let jumpArray = [2, 3, 1, 1, 4];
console.log(jump(jumpArray)); // Output: 2 (2 -> 3 -> 4)
```

These advanced exercises continue to challenge your array manipulation skills and problem-solving abilities in JavaScript. As you work through these exercises, you'll encounter a range of scenarios that require careful consideration of array elements and creative algorithm design.
Certainly, let's continue exploring more advanced array manipulation and problem-solving exercises:

**Exercise 71: Merge Intervals**

**Description:** Write a function that takes an array of intervals (pairs of start and end times) and merges overlapping intervals.

**Sample Solution:**
```javascript
function mergeIntervals(intervals) {
  if (intervals.length <= 1) {
    return intervals;
  }

  intervals.sort((a, b) => a[0] - b[0]);

  const merged = [intervals[0]];
  for (let i = 1; i < intervals.length; i++) {
    const currentInterval = intervals[i];
    const lastMergedInterval = merged[merged.length - 1];

    if (currentInterval[0] <= lastMergedInterval[1]) {
      lastMergedInterval[1] = Math.max(lastMergedInterval[1], currentInterval[1]);
    } else {
      merged.push(currentInterval);
    }
  }

  return merged;
}

let intervals = [[1, 3], [2, 6], [8, 10], [15, 18]];
console.log(mergeIntervals(intervals));
// Output: [[1, 6], [8, 10], [15, 18]]
```

**Exercise 72: Subsets**

**Description:** Write a function that takes an array of distinct integers and returns all possible subsets.

**Sample Solution:**
```javascript
function subsets(nums) {
  const allSubsets = [[]];

  for (let num of nums) {
    const subsetsWithNum = [];

    for (let subset of allSubsets) {
      subsetsWithNum.push([...subset, num]);
    }

    allSubsets.push(...subsetsWithNum);
  }

  return allSubsets;
}

let numbers = [1, 2, 3];
console.log(subsets(numbers));
// Output: [[], [1], [2], [3], [1, 2], [1, 3], [2, 3], [1, 2, 3]]
```

**Exercise 73: Next Permutation**

**Description:** Write a function that takes an array of integers and returns the next permutation in lexicographical order.

**Sample Solution:**
```javascript
function nextPermutation(nums) {
  let i = nums.length - 2;

  while (i >= 0 && nums[i] >= nums[i + 1]) {
    i--;
  }

  if (i >= 0) {
    let j = nums.length - 1;
    while (j >= 0 && nums[j] <= nums[i]) {
      j--;
    }
    [nums[i], nums[j]] = [nums[j], nums[i]];
  }

  reverse(nums, i + 1);

  function reverse(arr, start) {
    let left = start;
    let right = arr.length - 1;
    while (left < right) {
      [arr[left], arr[right]] = [arr[right], arr[left]];
      left++;
      right--;
    }
  }
}

let numbers = [1, 2, 3];
nextPermutation(numbers);
console.log(numbers); // Output: [1, 3, 2]
```

**Exercise 74: Sort Colors**

**Description:** Write a function that takes an array of integers representing red, white, and blue (0, 1, and 2 respectively) and sorts them in-place so that the array is grouped by color.

**Sample Solution:**
```javascript
function sortColors(nums) {
  let low = 0;
  let high = nums.length - 1;
  let i = 0;

  while (i <= high) {
    if (nums[i] === 0) {
      [nums[i], nums[low]] = [nums[low], nums[i]];
      low++;
      i++;
    } else if (nums[i] === 2) {
      [nums[i], nums[high]] = [nums[high], nums[i]];
      high--;
    } else {
      i++;
    }
  }
}

let colors = [2, 0, 2, 1, 1, 0];
sortColors(colors);
console.log(colors); // Output: [0, 0, 1, 1, 2, 2]
```

**Exercise 75: First Missing Positive**

**Description:** Write a function that takes an array of integers and returns the first missing positive integer that does not appear in the array.

**Sample Solution:**
```javascript
function firstMissingPositive(nums) {
  for (let i = 0; i < nums.length; i++) {
    while (nums[i] > 0 && nums[i] <= nums.length && nums[nums[i] - 1] !== nums[i]) {
      [nums[nums[i] - 1], nums[i]] = [nums[i], nums[nums[i] - 1]];
    }
  }

  for (let i = 0; i < nums.length; i++) {
    if (nums[i] !== i + 1) {
      return i + 1;
    }
  }

  return nums.length + 1;
}

let numbers = [3, 4, -1, 1];
console.log(firstMissingPositive(numbers)); // Output: 2
```

These exercises continue to explore advanced array manipulation and problem-solving in JavaScript. By tackling these exercises, you'll develop a deeper understanding of more complex algorithms and data manipulation techniques that can be applied to a wide range of scenarios.
Certainly, let's continue with more advanced array manipulation and problem-solving exercises:

**Exercise 76: Rotate Image**

**Description:** Write a function that takes a 2D matrix (an array of arrays) and rotates it by 90 degrees clockwise.

**Sample Solution:**
```javascript
function rotate(matrix) {
  const n = matrix.length;

  // Transpose the matrix
  for (let i = 0; i < n; i++) {
    for (let j = i; j < n; j++) {
      [matrix[i][j], matrix[j][i]] = [matrix[j][i], matrix[i][j]];
    }
  }

  // Reverse each row
  for (let i = 0; i < n; i++) {
    matrix[i].reverse();
  }
}

let matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];
rotate(matrix);
console.log(matrix);
// Output: [ [7, 4, 1], [8, 5, 2], [9, 6, 3] ]
```

**Exercise 77: Valid Sudoku**

**Description:** Write a function that takes a 9x9 Sudoku board filled with digits and returns true if the Sudoku is valid, according to the rules.

**Sample Solution:**
```javascript
function isValidSudoku(board) {
  const rows = new Array(9).fill(null).map(() => new Set());
  const columns = new Array(9).fill(null).map(() => new Set());
  const boxes = new Array(9).fill(null).map(() => new Set());

  for (let i = 0; i < 9; i++) {
    for (let j = 0; j < 9; j++) {
      const num = board[i][j];
      if (num === '.') continue;

      if (rows[i].has(num) || columns[j].has(num) || boxes[Math.floor(i / 3) * 3 + Math.floor(j / 3)].has(num)) {
        return false;
      }

      rows[i].add(num);
      columns[j].add(num);
      boxes[Math.floor(i / 3) * 3 + Math.floor(j / 3)].add(num);
    }
  }

  return true;
}

let sudokuBoard = [
  ['5', '3', '.', '.', '7', '.', '.', '.', '.'],
  ['6', '.', '.', '1', '9', '5', '.', '.', '.'],
  ['.', '9', '8', '.', '.', '.', '.', '6', '.'],
  ['8', '.', '.', '.', '6', '.', '.', '.', '3'],
  ['4', '.', '.', '8', '.', '3', '.', '.', '1'],
  ['7', '.', '.', '.', '2', '.', '.', '.', '6'],
  ['.', '6', '.', '.', '.', '.', '2', '8', '.'],
  ['.', '.', '.', '4', '1', '9', '.', '.', '5'],
  ['.', '.', '.', '.', '8', '.', '.', '7', '9']
];
console.log(isValidSudoku(sudokuBoard)); // Output: true
```

**Exercise 78: Median of Two Sorted Arrays**

**Description:** Write a function that takes two sorted arrays and returns the median of the two arrays.

**Sample Solution:**
```javascript
function findMedianSortedArrays(nums1, nums2) {
  const merged = [];
  let i = 0;
  let j = 0;

  while (i < nums1.length && j < nums2.length) {
    if (nums1[i] <= nums2[j]) {
      merged.push(nums1[i]);
      i++;
    } else {
      merged.push(nums2[j]);
      j++;
    }
  }

  while (i < nums1.length) {
    merged.push(nums1[i]);
    i++;
  }

  while (j < nums2.length) {
    merged.push(nums2[j]);
    j++;
  }

  const middle = Math.floor(merged.length / 2);

  if (merged.length % 2 === 0) {
    return (merged[middle - 1] + merged[middle]) / 2;
  } else {
    return merged[middle];
  }
}

let nums1 = [1, 3];
let nums2 = [2];
console.log(findMedianSortedArrays(nums1, nums2)); // Output: 2.0
```

**Exercise 79: Longest Common Subsequence**

**Description:** Write a function that takes two strings and returns the length of the longest common subsequence of the two strings.

**Sample Solution:**
```javascript
function longestCommonSubsequence(text1, text2) {
  const dp = new Array(text1.length + 1).fill(null).map(() => new Array(text2.length + 1).fill(0));

  for (let i = 1; i <= text1.length; i++) {
    for (let j = 1; j <= text2.length; j++) {
      if (text1[i - 1] ===

 text2[j - 1]) {
        dp[i][j] = dp[i - 1][j - 1] + 1;
      } else {
        dp[i][j] = Math.max(dp[i - 1][j], dp[i][j - 1]);
      }
    }
  }

  return dp[text1.length][text2.length];
}

let text1 = 'abcde';
let text2 = 'ace';
console.log(longestCommonSubsequence(text1, text2)); // Output: 3 (LCS: 'ace')
```

These advanced exercises continue to challenge your array manipulation skills and problem-solving abilities in JavaScript. They cover a wide range of topics, from matrix rotations to string manipulation and sequence matching. By engaging with these exercises, you'll deepen your understanding of advanced algorithms and develop effective strategies for solving complex problems using arrays.
Certainly, let's continue with more advanced array manipulation and problem-solving exercises:

**Exercise 80: Maximum Subarray**

**Description:** Write a function that takes an array of integers and returns the maximum sum of a contiguous subarray.

**Sample Solution:**
```javascript
function maxSubArray(nums) {
  let maxSum = nums[0];
  let currentSum = nums[0];

  for (let i = 1; i < nums.length; i++) {
    currentSum = Math.max(nums[i], currentSum + nums[i]);
    maxSum = Math.max(maxSum, currentSum);
  }

  return maxSum;
}

let numbers = [-2, 1, -3, 4, -1, 2, 1, -5, 4];
console.log(maxSubArray(numbers)); // Output: 6 (Subarray: [4, -1, 2, 1])
```

**Exercise 81: Product of Array Except Self**

**Description:** Write a function that takes an array of integers and returns an array where each element is the product of all elements in the original array except itself.

**Sample Solution:**
```javascript
function productExceptSelf(nums) {
  const result = new Array(nums.length).fill(1);
  let leftProduct = 1;
  let rightProduct = 1;

  for (let i = 0; i < nums.length; i++) {
    result[i] *= leftProduct;
    leftProduct *= nums[i];
  }

  for (let i = nums.length - 1; i >= 0; i--) {
    result[i] *= rightProduct;
    rightProduct *= nums[i];
  }

  return result;
}

let numbers = [1, 2, 3, 4];
console.log(productExceptSelf(numbers)); // Output: [24, 12, 8, 6]
```

**Exercise 82: Find the Duplicate Number**

**Description:** Write a function that takes an array of integers where each integer is between 1 and n (inclusive) and appears once or multiple times. Return the duplicate number.

**Sample Solution:**
```javascript
function findDuplicate(nums) {
  let slow = nums[0];
  let fast = nums[0];

  do {
    slow = nums[slow];
    fast = nums[nums[fast]];
  } while (slow !== fast);

  let ptr1 = nums[0];
  let ptr2 = slow;

  while (ptr1 !== ptr2) {
    ptr1 = nums[ptr1];
    ptr2 = nums[ptr2];
  }

  return ptr1;
}

let numbers = [3, 1, 3, 4, 2];
console.log(findDuplicate(numbers)); // Output: 3
```

**Exercise 83: Single Number II**

**Description:** Write a function that takes an array of integers where each integer appears three times except for one, which appears exactly once. Return the single integer that appears once.

**Sample Solution:**
```javascript
function singleNumber(nums) {
  let ones = 0;
  let twos = 0;

  for (let num of nums) {
    ones = (ones ^ num) & ~twos;
    twos = (twos ^ num) & ~ones;
  }

  return ones;
}

let numbers = [2, 2, 3, 2];
console.log(singleNumber(numbers)); // Output: 3
```

**Exercise 84: H-Index**

**Description:** Write a function that takes an array of citations (each citation is a non-negative integer) and returns the h-index of the array. The h-index is defined as the maximum number h such that there are at least h papers with h or more citations.

**Sample Solution:**
```javascript
function hIndex(citations) {
  citations.sort((a, b) => b - a);

  for (let i = 0; i < citations.length; i++) {
    if (citations[i] < i + 1) {
      return i;
    }
  }

  return citations.length;
}

let citations = [3, 0, 6, 1, 5];
console.log(hIndex(citations)); // Output: 3
```

These exercises cover various advanced topics in array manipulation and algorithm design. By working through these exercises, you'll continue to enhance your problem-solving skills and gain deeper insights into how to approach complex problems using arrays in JavaScript.

Absolutely, let's continue with more advanced array manipulation and problem-solving exercises:

**Exercise 85: Longest Consecutive Sequence**

**Description:** Write a function that takes an array of integers and returns the length of the longest consecutive elements sequence.

**Sample Solution:**
```javascript
function longestConsecutive(nums) {
  const numSet = new Set(nums);
  let longestStreak = 0;

  for (let num of numSet) {
    if (!numSet.has(num - 1)) {
      let currentNum = num;
      let currentStreak = 1;

      while (numSet.has(currentNum + 1)) {
        currentNum += 1;
        currentStreak += 1;
      }

      longestStreak = Math.max(longestStreak, currentStreak);
    }
  }

  return longestStreak;
}

let numbers = [100, 4, 200, 1, 3, 2];
console.log(longestConsecutive(numbers)); // Output: 4 (Longest sequence: [1, 2, 3, 4])
```

**Exercise 86: Valid Parentheses**

**Description:** Write a function that takes a string containing just the characters '(', ')', '{', '}', '[' and ']', and determines if the input string is valid.

**Sample Solution:**
```javascript
function isValidParentheses(s) {
  const stack = [];

  for (let char of s) {
    if (char === '(' || char === '{' || char === '[') {
      stack.push(char);
    } else {
      if (stack.length === 0) {
        return false;
      }
      const top = stack.pop();
      if (
        (char === ')' && top !== '(') ||
        (char === '}' && top !== '{') ||
        (char === ']' && top !== '[')
      ) {
        return false;
      }
    }
  }

  return stack.length === 0;
}

let input = '{[()]}';
console.log(isValidParentheses(input)); // Output: true
```

**Exercise 87: Word Ladder**

**Description:** Write a function that takes two words, beginWord and endWord, and a list of wordList. Return the length of the shortest transformation sequence from beginWord to endWord, such that:

- Only one letter can be changed at a time.
- Each transformed word must exist in the wordList.

**Sample Solution:**
```javascript
function ladderLength(beginWord, endWord, wordList) {
  if (!wordList.includes(endWord)) {
    return 0;
  }

  const wordSet = new Set(wordList);
  const queue = [[beginWord, 1]];

  while (queue.length > 0) {
    const [currentWord, steps] = queue.shift();

    if (currentWord === endWord) {
      return steps;
    }

    for (let i = 0; i < currentWord.length; i++) {
      for (let j = 97; j <= 122; j++) {
        const newWord = currentWord.slice(0, i) + String.fromCharCode(j) + currentWord.slice(i + 1);

        if (wordSet.has(newWord)) {
          queue.push([newWord, steps + 1]);
          wordSet.delete(newWord);
        }
      }
    }
  }

  return 0;
}

let begin = 'hit';
let end = 'cog';
let wordList = ['hot', 'dot', 'dog', 'lot', 'log', 'cog'];
console.log(ladderLength(begin, end, wordList)); // Output: 5
```

**Exercise 88: Expression Add Operators**

**Description:** Write a function that takes a string containing only digits 0-9 and a target value, and returns all possibilities to add binary operators (+, -, or *) between the digits so that the expression evaluates to the target value.

**Sample Solution:**
```javascript
function addOperators(num, target) {
  const result = [];

  function backtrack(path, index, currentVal, lastAdded) {
    if (index === num.length) {
      if (currentVal === target) {
        result.push(path);
      }
      return;
    }

    for (let i = index; i < num.length; i++) {
      if (i !== index && num[index] === '0') {
        break;
      }

      const currentNum = parseInt(num.substring(index, i + 1));

      if (index === 0) {
        backtrack(path + currentNum, i + 1, currentNum, currentNum);
      } else {
        backtrack(path + '+' + currentNum, i + 1, currentVal + currentNum, currentNum);
        backtrack(path + '-' + currentNum, i + 1, currentVal - currentNum, -currentNum);
        backtrack(path + '*' + currentNum, i + 1, currentVal - lastAdded + lastAdded * currentNum, lastAdded * currentNum);
      }
    }
  }

  backtrack('', 0, 0, 0);

  return result;
}

let num = '123';
let target = 6;
console.log(addOperators(num, target));
// Output: ['1*2*3', '1+2+3']
```

These exercises continue to challenge your array manipulation skills and problem-solving abilities in JavaScript. By tackling these advanced exercises, you'll refine your approach to algorithm design

 and learn how to solve complex problems using arrays and various algorithmic techniques.
Certainly, let's continue exploring more advanced array manipulation and problem-solving exercises:

**Exercise 89: Jump Game III**

**Description:** Write a function that takes an array of non-negative integers where each element represents the maximum jump length. Return true if you can reach the last index starting from the first index, otherwise return false. Additionally, at most one step can be made to an index containing zero.

**Sample Solution:**
```javascript
function canReachEnd(nums) {
  let maxReach = 0;

  for (let i = 0; i < nums.length; i++) {
    if (i > maxReach) {
      return false;
    }
    maxReach = Math.max(maxReach, i + nums[i]);
  }

  return true;
}

let jumpArray = [4, 2, 3, 0, 3, 1, 2];
console.log(canReachEnd(jumpArray)); // Output: true
```

**Exercise 90: Set Matrix Zeroes**

**Description:** Write a function that takes an `m x n` matrix and if an element is 0, set its entire row and column to 0. Do it in-place.

**Sample Solution:**
```javascript
function setZeroes(matrix) {
  const m = matrix.length;
  const n = matrix[0].length;
  const rowsToZero = new Set();
  const colsToZero = new Set();

  for (let i = 0; i < m; i++) {
    for (let j = 0; j < n; j++) {
      if (matrix[i][j] === 0) {
        rowsToZero.add(i);
        colsToZero.add(j);
      }
    }
  }

  for (let row of rowsToZero) {
    for (let j = 0; j < n; j++) {
      matrix[row][j] = 0;
    }
  }

  for (let col of colsToZero) {
    for (let i = 0; i < m; i++) {
      matrix[i][col] = 0;
    }
  }
}

let matrix = [
  [1, 1, 1],
  [1, 0, 1],
  [1, 1, 1]
];
setZeroes(matrix);
console.log(matrix);
// Output: [ [1, 0, 1], [0, 0, 0], [1, 0, 1] ]
```

**Exercise 91: Product of Array Except Self II**

**Description:** Write a function that takes an array of integers and returns an array where each element is the product of all elements in the original array except itself. You cannot use division in the solution.

**Sample Solution:**
```javascript
function productExceptSelf(nums) {
  const result = new Array(nums.length).fill(1);
  let leftProduct = 1;
  let rightProduct = 1;

  for (let i = 0; i < nums.length; i++) {
    result[i] *= leftProduct;
    leftProduct *= nums[i];
  }

  for (let i = nums.length - 1; i >= 0; i--) {
    result[i] *= rightProduct;
    rightProduct *= nums[i];
  }

  return result;
}

let numbers = [1, 2, 3, 4];
console.log(productExceptSelf(numbers)); // Output: [24, 12, 8, 6]
```

**Exercise 92: Sort an Almost Sorted Array**

**Description:** Write a function that takes an array where each element is at most `k` positions away from its sorted position. Sort and return the array.

**Sample Solution:**
```javascript
function sortKSortedArray(arr, k) {
  const minHeap = new MinHeap();

  for (let i = 0; i <= k; i++) {
    minHeap.insert(arr[i]);
  }

  let index = 0;
  for (let i = k + 1; i < arr.length; i++) {
    arr[index++] = minHeap.remove();
    minHeap.insert(arr[i]);
  }

  while (!minHeap.isEmpty()) {
    arr[index++] = minHeap.remove();
  }
}

class MinHeap {
  constructor() {
    this.heap = [];
  }

  insert(value) {
    this.heap.push(value);
    this.bubbleUp(this.heap.length - 1);
  }

  remove() {
    if (this.isEmpty()) {
      return null;
    }

    if (this.heap.length === 1) {
      return this.heap.pop();
    }

    const minValue = this.heap[0];
    this.heap[0] = this.heap.pop();
    this.bubbleDown(0);
    return minValue;
  }

  isEmpty() {
    return this.heap.length === 0;
  }

  bubbleUp(index) {
    while (index > 0) {
      const parentIndex = Math.floor((index - 1) / 2);
      if (this.heap[index] < this.heap[parentIndex]) {
        [this.heap[index], this.heap[parentIndex]] = [this.heap[parentIndex], this.heap[index]];
        index = parentIndex;
      } else {
        break;
      }
    }
  }

  bubbleDown(index) {
    while (index < this.heap.length) {
      const leftChildIdx = 2 * index + 1;
      const rightChildIdx = 2 * index + 2;
      let smallest = index;

      if (leftChildIdx < this.heap.length && this.heap[leftChildIdx] < this.heap[smallest]) {
        smallest = leftChildIdx;
      }

      if (rightChildIdx < this.heap.length && this.heap[rightChildIdx] < this.heap[smallest]) {
        smallest = rightChildIdx;
      }

      if (smallest !== index) {
        [this.heap[index], this.heap[smallest]] = [this.heap[smallest], this.heap[index]];
        index = smallest;
      } else {
        break;
      }
    }
  }
}

let kSortedArray = [3, 1, 2, 0, 5, 4];
let kValue = 2;
sortKSortedArray(kSortedArray, kValue);
console.log(kSortedArray); // Output: [0, 1, 2, 3, 4, 5]
```

These exercises continue to deepen your understanding of advanced array manipulation and problem-solving techniques in JavaScript. Each exercise presents a unique challenge and scenario that allows you to practice and expand your skills in solving complex problems using arrays and other algorithmic concepts.
Certainly, let's continue exploring more advanced array manipulation and problem-solving exercises:

**Exercise 93: Longest Increasing Subsequence**

**Description:** Write a function that takes an array of integers and returns the length of the longest increasing subsequence.

**Sample Solution:**
```javascript
function lengthOfLIS(nums) {
  const dp = new Array(nums.length).fill(1);

  for (let i = 1; i < nums.length; i++) {
    for (let j = 0; j < i; j++) {
      if (nums[i] > nums[j]) {
        dp[i] = Math.max(dp[i], dp[j] + 1);
      }
    }
  }

  return Math.max(...dp);
}

let numbers = [10, 9, 2, 5, 3, 7, 101, 18];
console.log(lengthOfLIS(numbers)); // Output: 4 (LIS: [2, 3, 7, 101])
```

**Exercise 94: Trapping Rain Water**

**Description:** Write a function that takes an array of non-negative integers representing an elevation map where the width of each bar is 1. Compute how much water it can trap after raining.

**Sample Solution:**
```javascript
function trap(height) {
  let left = 0;
  let right = height.length - 1;
  let leftMax = 0;
  let rightMax = 0;
  let totalWater = 0;

  while (left < right) {
    if (height[left] < height[right]) {
      if (height[left] > leftMax) {
        leftMax = height[left];
      } else {
        totalWater += leftMax - height[left];
      }
      left++;
    } else {
      if (height[right] > rightMax) {
        rightMax = height[right];
      } else {
        totalWater += rightMax - height[right];
      }
      right--;
    }
  }

  return totalWater;
}

let elevationMap = [0, 1, 0, 2, 1, 0, 1, 3, 2, 1, 2, 1];
console.log(trap(elevationMap)); // Output: 6
```

**Exercise 95: Merge k Sorted Lists**

**Description:** Write a function that takes an array of linked lists, each linked list is sorted in ascending order. Merge all the linked lists into one sorted linked list and return it.

**Sample Solution:**
```javascript
class ListNode {
  constructor(val, next = null) {
    this.val = val;
    this.next = next;
  }
}

function mergeKLists(lists) {
  const minHeap = new MinHeap();

  for (let list of lists) {
    let current = list;
    while (current) {
      minHeap.insert(current.val);
      current = current.next;
    }
  }

  let dummyHead = new ListNode();
  let current = dummyHead;

  while (!minHeap.isEmpty()) {
    current.next = new ListNode(minHeap.remove());
    current = current.next;
  }

  return dummyHead.next;
}

class MinHeap {
  // ... (same MinHeap implementation as shown before)
}

let list1 = new ListNode(1, new ListNode(4, new ListNode(5)));
let list2 = new ListNode(1, new ListNode(3, new ListNode(4)));
let list3 = new ListNode(2, new ListNode(6));
console.log(mergeKLists([list1, list2, list3]));
// Output: 1 -> 1 -> 2 -> 3 -> 4 -> 4 -> 5 -> 6
```

**Exercise 96: Median of Two Sorted Arrays II**

**Description:** Write a function that takes two sorted arrays and returns the median of the two arrays.

**Sample Solution:**
```javascript
function findMedianSortedArrays(nums1, nums2) {
  if (nums1.length > nums2.length) {
    return findMedianSortedArrays(nums2, nums1);
  }

  const totalLength = nums1.length + nums2.length;
  const partition1 = Math.floor(nums1.length / 2);
  let partition2 = Math.floor(totalLength / 2) - partition1;

  let leftMax1 = partition1 > 0 ? nums1[partition1 - 1] : Number.NEGATIVE_INFINITY;
  let leftMax2 = partition2 > 0 ? nums2[partition2 - 1] : Number.NEGATIVE_INFINITY;
  let rightMin1 = partition1 < nums1.length ? nums1[partition1] : Number.POSITIVE_INFINITY;
  let rightMin2 = partition2 < nums2.length ? nums2[partition2] : Number.POSITIVE_INFINITY;

  while (leftMax1 > rightMin2 || leftMax2 > rightMin1) {
    if (leftMax1 > rightMin2) {
      partition1--;
      partition2++;
    } else {
      partition1++;
      partition2--;
    }

    leftMax1 = partition1 > 0 ? nums1[partition1 - 1] : Number.NEGATIVE_INFINITY;
    leftMax2 = partition2 > 0 ? nums2[partition2 - 1] : Number.NEGATIVE_INFINITY;
    rightMin1 = partition1 < nums1.length ? nums1[partition1] : Number.POSITIVE_INFINITY;
    rightMin2 = partition2 < nums2.length ? nums2[partition2] : Number.POSITIVE_INFINITY;
  }

  if (totalLength % 2 === 0) {
    return (Math.max(leftMax1, leftMax2) + Math.min(rightMin1, rightMin2)) / 2;
  } else {
    return Math.min(rightMin1, rightMin2);
  }
}

let nums1 = [1, 3];
let nums2 = [2];
console.log(findMedianSortedArrays(nums1, nums2)); // Output: 2.0
```

These advanced exercises continue to stretch your problem-solving skills and deepen your understanding of array manipulation, linked lists, and other algorithmic concepts. By engaging with these exercises, you'll further develop your ability to approach and solve complex problems using arrays and other relevant data structures.
Of course, let's continue with more advanced array manipulation and problem-solving exercises:

**Exercise 97: Subarray Sum Equals K**

**Description:** Write a function that takes an array of integers and an integer k. Return the total number of continuous subarrays whose sum equals k.

**Sample Solution:**
```javascript
function subarraySum(nums, k) {
  let count = 0;
  let sum = 0;
  const sumMap = new Map();
  sumMap.set(0, 1);

  for (let num of nums) {
    sum += num;
    if (sumMap.has(sum - k)) {
      count += sumMap.get(sum - k);
    }
    sumMap.set(sum, (sumMap.get(sum) || 0) + 1);
  }

  return count;
}

let numbers = [1, 1, 1];
let kValue = 2;
console.log(subarraySum(numbers, kValue)); // Output: 2
```

**Exercise 98: Sliding Window Maximum**

**Description:** Write a function that takes an array of integers and a window size k. Return an array of the maximum value in each window of size k as it slides through the array.

**Sample Solution:**
```javascript
function maxSlidingWindow(nums, k) {
  const result = [];
  const deque = [];

  for (let i = 0; i < nums.length; i++) {
    while (deque.length > 0 && deque[0] < i - k + 1) {
      deque.shift();
    }

    while (deque.length > 0 && nums[deque[deque.length - 1]] < nums[i]) {
      deque.pop();
    }

    deque.push(i);

    if (i >= k - 1) {
      result.push(nums[deque[0]]);
    }
  }

  return result;
}

let numbers = [1, 3, -1, -3, 5, 3, 6, 7];
let windowSize = 3;
console.log(maxSlidingWindow(numbers, windowSize)); // Output: [3, 3, 5, 5, 6, 7]
```

**Exercise 99: Kth Largest Element in an Array**

**Description:** Write a function that takes an array of integers and an integer k. Return the kth largest element in the array.

**Sample Solution:**
```javascript
function findKthLargest(nums, k) {
  const partition = (left, right) => {
    const pivot = nums[right];
    let i = left - 1;

    for (let j = left; j < right; j++) {
      if (nums[j] >= pivot) {
        i++;
        [nums[i], nums[j]] = [nums[j], nums[i]];
      }
    }

    [nums[i + 1], nums[right]] = [nums[right], nums[i + 1]];
    return i + 1;
  };

  let left = 0;
  let right = nums.length - 1;

  while (left <= right) {
    const pivotIndex = partition(left, right);
    if (pivotIndex === k - 1) {
      return nums[pivotIndex];
    } else if (pivotIndex < k - 1) {
      left = pivotIndex + 1;
    } else {
      right = pivotIndex - 1;
    }
  }
}

let numbers = [3, 2, 1, 5, 6, 4];
let kValue = 2;
console.log(findKthLargest(numbers, kValue)); // Output: 5
```

**Exercise 100: Longest Substring with At Most K Distinct Characters**

**Description:** Write a function that takes a string and an integer k. Return the length of the longest substring that contains at most k distinct characters.

**Sample Solution:**
```javascript
function lengthOfLongestSubstringKDistinct(s, k) {
  const charCount = new Map();
  let left = 0;
  let maxLength = 0;

  for (let right = 0; right < s.length; right++) {
    const char = s[right];
    charCount.set(char, (charCount.get(char) || 0) + 1);

    while (charCount.size > k) {
      const leftChar = s[left];
      charCount.set(leftChar, charCount.get(leftChar) - 1);
      if (charCount.get(leftChar) === 0) {
        charCount.delete(leftChar);
      }
      left++;
    }

    maxLength = Math.max(maxLength, right - left + 1);
  }

  return maxLength;
}

let input = 'eceba';
let kValue = 2;
console.log(lengthOfLongestSubstringKDistinct(input, kValue)); // Output: 3
```

These advanced exercises delve deeper into various array manipulation and problem-solving concepts. By tackling these exercises, you'll further hone your skills in algorithm design and problem-solving, making you better equipped to solve complex problems using arrays and related data structures.


### your understanding of array methods and enhance your skills:

1. How can you create an array in JavaScript?
2. What's the difference between `Array.push()` and `Array.pop()` methods?
3. Explain the usage of `Array.map()` method with an example.
4. How does the `Array.filter()` method work? Provide an example.
5. What does the `Array.reduce()` method do? Give an example of its usage.
6. How can you check if an element exists in an array using `Array.includes()`?
7. Explain the purpose of the `Array.find()` method with an example.
8. What's the difference between `Array.indexOf()` and `Array.lastIndexOf()`?
9. How do you remove elements from an array using `Array.splice()`?
10. Explain how the `Array.slice()` method works with an example.
11. How can you join elements of an array into a string using `Array.join()`?
12. What's the purpose of the `Array.concat()` method? Provide an example.
13. How do you sort elements in an array using the `Array.sort()` method?
14. Explain the concept of a callback function in relation to array methods.
15. How can you iterate through an array using the `Array.forEach()` method?
16. What's the difference between `for...of` and `for...in` loops when iterating over arrays?
17. How does the `Array.every()` method work? Give an example.
18. Explain the usage of the `Array.some()` method with a practical scenario.
19. How can you reverse the order of elements in an array using `Array.reverse()`?
20. What does the `Array.splice()` method return, and how can you use it?
21. How do you find the maximum and minimum values in an array using array methods?
22. Explain how the `Array.map()` method can be used to transform an array of strings to uppercase.
23. How can you remove duplicate elements from an array using `Array.from()`?
24. How does the `Array.unshift()` method work? Provide an example.
25. Describe the differences between `Array.forEach()` and `Array.map()` methods.
