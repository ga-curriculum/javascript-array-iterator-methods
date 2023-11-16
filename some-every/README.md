# ![JavaScript Array Iterator Methods - some and every](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to test if *some* or *every* element in an array meets a given condition.

## some

PURPOSE: Check if an array has at least one element that meets a specific condition.

```javascript
const cars = [
  {color: 'red', make: 'BMW', year: 2001},
  {color: 'white', make: 'Toyota', year: 2013},
  {color: 'blue', make: 'Ford', year: 2014},
  {color: 'white', make: 'Tesla', year: 2016}
];

const hasFord = cars.some((car) => {
  return car.make === 'Ford';
});
// hasFord is true
```

### 🎓 You Do 

Do I have a random elephant in my room? 

```javascript
const thingsInMyRoom = ['bed', 'lamp', 'table', 'random elephant', 'three tacos'];
const isARandomElephantInMyRoom = /* Fill code in here */
```

## every

PURPOSE: Check if every element in an array meets a certain condition.

```javascript
const cars = [
  {color: 'red', make: 'BMW', year: 2001},
  {color: 'white', make: 'Toyota', year: 2013},
  {color: 'blue', make: 'Ford', year: 2014},
  {color: 'white', make: 'Tesla', year: 2016}
];

const everyCarIsBlue = cars.every((car) => {
  return car.color === 'blue'
});

// everyCarIsBlue is false
```

### 🎓 You Do 

Do I have anything but random elephants in my room?

```javascript
const thingsInMyRoom = [
  'random elephant', 
  'random elephant', 
  'random elephant', 
  'random elephant'
];

const isEverythingInMyRoomARandomElephant = /* Fill code in here */
```

