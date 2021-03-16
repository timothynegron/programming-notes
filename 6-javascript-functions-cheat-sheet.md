# JavaScript Functions Cheat Sheet

### About

Just a document for quickly referencing the most used built in JavaScript functions.

---

### Topics

1. Functions for Arrays
2. Functions for Arrays or Strings
3. Functions for Strings
4. Advance Functions

# Functions for Arrays

### splice()

* array.splice(index, how many after index to remove)
* array.splice(starting index, ending index)
* Alters the array calling the function.

###### Examples:
```javascript
array.splice(i, 1); // Only removes the starting index i
array.splice(i, 3); // removes three starting with index i
```

### shift()

* array.shift(no need to put value in here)
* Removes 0 index from the beginning of the array.
* Shifts entire array down.
* i.e. value in index 1 goes to index 0, etc...

###### Example:

```javascript
array.shift(); // removes first index and shifts entire array down.
```

### unshift()

* array.unshift(value to go to beginning of the array)
* Shifts entire array up.
* Values in index 0 goes to index 1, etc...

###### Examples:
```javascript
array.unshift(10); // stores value at beginning of array
array.unshift(z); // stores value in z at beginning of array
array.unshift(x[i]); // stores value in x[i] at beginning of array
array.unshift('hello'); // stores string value at beginning of array
```

### push()

* array.push(value goes to end of the array)
* Stores value at the end of the array

###### Examples:

```javascript
array.push(10); // stores 10 at end of array
array.push(z); // stores value in z at end of array
array.push(x[i]); // stores value in x[i] at end of array
array.push('hello'); // stores string value at end of array
```

### pop()

* array.pop()
* Removes last element the array.

###### Example:

```javascript
array.pop(); // Removes last element
```

### Join()

* Takes an array and **returns a string**.

###### Examples:

```javascript
array.join() // returns a string of the array with commas separating each value.
array.join('') // returns a string of the array with no commas.
array.join(' ') // returns a string with a space separating each value.
array.join(', ') // etc...
```

# Functions for Arrays or Strings

### slice()

* array.slice(starting index, ending index)
* str.slice(starting index, ending index)
* Works on strings and arrays.
* Does not alter the array calling the function.
* Returns a shallow copy of an array with the result.

###### Examples:

```javascript
array.slice(2) // returns shallow copy removing first two elements
array.slice(2, 4) // returns shallow copy removing index 2 and 3
```

### concat()

* str.concat(combine with str)
* str.concat(add in between, combine with str)
* array.concat(combine with array)
* Returns a shallow copy.
* For arrays can data type does not matter.

###### Examples:

```javascript
str1.concat(str2) // Combines both strings
str.concat(' ', str2) // Combines both strings but adds a space
array1.concat(array2); // Combines both arrays
```

### includes()

* Returns a boolean value.
* Looks for value in parenthesis

###### Examples:

```javascript
array.inclues('t') // Returns true if there is a t in the array
```

# Functions for Strings

### split()

* Returns an array containing string element(s).

###### Examples:

```javascript
str.split() // Returns array of the whole string in 0 index
str.split('') // Returns array separating all string indexes
str.split(' ') // Returns array separating the string by space, removes space
str.split('o') // Returns array separating the string by letter o, removes o
```

### replace()

* replace(string to replace, replace with)
* Returns a string that is replaced with another.
* Replaces on the first one it finds.
  
###### Examples:

```javascript
str.replace('t', '') // Replaces the first t with empty string (removes t)
str.replace('t', ' ') // Replaces the first t with a space
str.replace('1', '3') // Replaces the first '1' with a '3'
```

### replaceAll()

* replaceAll(string to replace, replace with)
* New function, not widely supported yet.

###### Examples:

```javascript
str.replaceAll('t', '') // Replaces all t's with empty string (removes all t's)
str.replaceAll('t', ' ') // Replaces all t's with a space
str.replaceAll('1', '3') // Replaces all '1's with '3's
```

# Advance Functions

### reduce()

* Arrays only.
* Iterates through array.
* Math operators.
* Returns accumulated value.
* "Used for accumalators"

###### Examples:

```javascript
const array1 = [1, 2, 3, 4];
const reducer = (accumulator, currentValue) => accumulator + currentValue;

// 1 + 2 + 3 + 4
console.log(array1.reduce(reducer));
// expected output: 10

// 5 + 1 + 2 + 3 + 4
console.log(array1.reduce(reducer, 5));
// expected output: 15


// Another example...
const sum = arrayOfNumbers.reduce(
    (sum, num) => sum + num,
    0 // Starting value
)
```

### map()

* Arrays only.
* Iterates through array.
* Returns array with new values.
* "Go to each index and do something"

###### Examples:

```javascript
const array1 = [1, 4, 9, 16];

// pass a function to map
const map1 = array1.map(x => x * 2);

console.log(map1);
// expected output: Array [2, 8, 18, 32]
```

### filter

* Arrays only.
* Iterates through array.
* Returns values that meet condition.
* "Used to return arrays with some values missing"

###### Examples:

```javascript
const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

console.log(result);
// expected output: Array ["exuberant", "destruction", "present"]
```
