# Array Iterator Methods - filter

![Hero image](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk


PURPOSE: Select certain elements from a source array.

### Obtain all elements that are true

```javascript
const arr = [true, false, true, false, false, true]

const filteredArr = arr.filter(function(element){
  return element
})

console.log(filteredArr) // [true, true, true]
```

### Obtain all truthy elements

```javascript
const arr = [true, false, 0, 'string', '', null, undefined, 42]

const filteredArr = arr.filter(function(element){
  return element
})

console.log(filteredArr) // [true, 'string', 42]
```

### Obtain all numbers over 50

```javascript
const nums = [100, 2, 5, 42, 99]

const numsOver50 = nums.filter(function(num){
  return num > 50
})

console.log(numsOver50) // [100, 99]

/*--- using an arrow function for the callback ---*/
const numsOver50 = nums.filter(nums => nums > 50)
```

### Obtain just the odd numbers

```javascript
const nums = [100, 2, 5, 42, 99]

const odds = nums.filter(function(num) {
  return num % 2
})

console.log(odds)

/*--- using an arrow function for the callback ---*/
const odds = nums.filter(num => num % 2)
```

### You Do 💪

Filter out all “jerks” and make a ‘jerk-free’ array named `notJerks`.

```javascript
const people = ["jerks", "nice people", "jerks", "nice people", "nice people"]
```