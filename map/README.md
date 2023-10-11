# Array Iterator Methods - map

![Hero image](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to use `map()` to iterate over an array, creating a new modified array.

## A note on callback functions
Every array iterator method in this module (with the exception of `reduce()` in the level up content) will have the same callback function signature. As a result, we will touch on it once in the context of `map()`, and the information in this section will be applicable to the rest of the iterator methods moving forward. 

```javascript
// callback function parameters
array.map(function(element, index, array) {

})
```

1. `element` - The current element
2. `index` - The index of the current element (optional)
3. `array` - The array the iterator method was called upon (optional)

Remember, the callback function we write will be called once for each element in the array. Under the hood, the engine will be passing arguments for each of these three parameters once for every iteration through the array. 

An easy way to examine what these parameters correspond to is to log the values: 

```javascript
const array = ['apple','banana','orange']

const mappedArray = array.map(function(element, index, array) {
  return `element is: ${element}, index is: ${index}, array is ${array}`
})

console.log(mappedArray)
// [ 'element is: apple, index is: 0, array is apple,banana,orange',
//   'element is: banana, index is: 1, array is apple,banana,orange',
//   'element is: orange, index is: 2, array is apple,banana,orange' ]
```

As we loop through the array, `element` is being supplied different values as an argument. The `index` is also changing as we move through the array. The `array` itself is static, as it always references the array itself! 

## map

**PURPOSE:** Create a new array from a source array, usually “transforming” its values.

The returned array is always the same length as the source array.

```javascript
const nums = [1, 2, 3]
const squared = nums.map(function(num) {
  return num * num
})

// squared --> [1, 4, 9]
```

`map` returns a new array comprised of ‘transformed’ values -  and how they have been transformed is up to the code we write in the callback function.

Callback functions typically make use of arrow function syntax:
```javascript
// using an arrow function for the callback:
const squared = nums.map(num => num * num)
```

### You Do 💪

Given an array of instructors,

```javascript
const instructors = ["Beryl", "Hunter", "Joe", "Jurgen", "Ben", "David"]
```

Use map to create a new array that adds the string " is awesome" to each array element.

Sample output: 
```javascript
[
  "Beryl is awesome",
	"Hunter is awesome",
	"Joe is awesome",
	"Jurgen is awesome",
  "Ben is awesome", 
  "David is awesome",
]
```


