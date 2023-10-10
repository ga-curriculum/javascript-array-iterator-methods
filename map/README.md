# Array Iterator Methods - map

![Hero image](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

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
const instructors = ["Beryl", "Ian", "Hunter", "Joe", "Jurgen", "Ben", "David"]
```

Use map to create a new array that adds the string " is awesome" to each array element.

Sample output: 
```javascript
[
  "Beryl is awesome",
	"Ian is awesome",
	"Hunter is awesome",
	"Joe is awesome",
	"Jurgen is awesome",
  "Ben is awesome", 
  "David is awesome",
]
```


