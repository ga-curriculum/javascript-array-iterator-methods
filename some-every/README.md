# Array Iterator Methods - some and every

![Hero image](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to test if some or every element in an array passes a given test.

## some

PURPOSE: Check if an array has at least one element that meets a specific condition.

```javascript
const cars = [
  {color: 'red', make: 'BMW', year: 2001},
  {color: 'white', make: 'Toyota', year: 2013},
  {color: 'blue', make: 'Ford', year: 2014},
  {color: 'white', make: 'Tesla', year: 2016}
]

const hasFord = cars.some(function(car) {
  return car.make === 'Ford'
})
// hasFord is true

/*--- using an arrow function for the callback ---*/
const hasFord = cars.some(car => car.make === 'Ford')
```

### You Do 💪

Do I have an evil monkey in my room? 

```javascript
const thingsInMyRoom = ["evil monkey", "bed", "lamp", "three tacos"]
const isAnEvilMonkeyInMyRoom = /* Fill code in here */
```

## every

PURPOSE: Check if every element in an array meets a certain condition.

```javascript
const cars = [
  {color: 'red', make: 'BMW', year: 2001},
  {color: 'white', make: 'Toyota', year: 2013},
  {color: 'blue', make: 'Ford', year: 2014},
  {color: 'white', make: 'Tesla', year: 2016}
]

const everyCarIsBlue = cars.every(function(car) {
  return car.color === 'blue'
})

// everyCarIsBlue is false

/*--- using an arrow function for the callback ---*/
const everyCarIsBlue = cars.every(car => car.color === 'blue')
```

### You Do 💪
Do I have anything but evil monkeys in my room?

```javascript
const thingsInMyRoom = [
  "evil donkey", 
  "evil monkey", 
  "evil monkey", 
  "evil monkey"
]

const isEverythingInMyRoomAnEvilMonkey = /* Fill code in here */
```

