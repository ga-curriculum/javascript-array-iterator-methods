# Array Iterator Methods - Level Up - Reduce

![Hero image](./assets/hero.png)

PURPOSE: Reduce an array into a single value. Note that the “single value” can be a single object, array, string - anything.

Reduce is unique from the other array iterator methods we've seen so far in that it has a more complex callback function syntax: 

The function is called with the following arguments: 

```javascript
array.reduce((accumulator, currentValue, currentIndex, array) => { function body }, initialValue)
```

1. `accumulator` - The value returned from the previous callback function. On the first call, this value is set to `initialValue`. 
The accumulator argument is crucial - it is how `reduce()` is able to keep track of a value throughout the entire iteration process. 

2. `currentValue` - The value of the current element. This operates the same as the `element` argument in other array iterator methods like `map` and `filter`.

3. `currentIndex` (optional) - The index position of the `currentValue`.

4. `array` (optional) - The array `reduce()` was called on.


### Sum up the numbers in an array

```javascript
const nums = [25, 5, 100, 10]

let sum = nums.reduce(function(accumulator, num) {
  return accumulator + num
}, 0)

// sum equals 140

/*--- using an arrow function for the callback ---*/
let sum = nums.reduce((acc, num) => acc + num, 0)
```

### Count votes

```javascript
let votes = ['Yes', 'No', 'Yes', 'Yes', 'No']

let tally = votes.reduce(function(acc, vote){
  if(acc[vote]){
    acc[vote] = acc[vote] + 1
  } else {
    acc[vote] = 1
  }
  return acc
}, {})

// tally is { 'Yes': 3, 'No': 2 }
```

Reduce is a swiss army knife - versatile, elegant, and always nice to have on hand. That said, if you’ve ever been out camping or at a poorly stocked AirBnB and had to rely on a swiss army knife to open bottles or cut everything for a meal, you’ll know that it is rarely the BEST tool for every job - rather it’s just the one that can handle a lot of tasks sort of well. 

So, while it is true that `reduce` COULD be used to handle the same tasks as almost all of the other examples you’ve seen in this lecture, best practice is to stay focused on what `reduce` truly shines at, which is reducing an array down to a single value - an object, a number, a string, etc. 

Just remember: reduce is a jack of all trades, master of one! 