## Exercise 1

```js 
let yourArray = [true, 3, '3', 2, null] // change this line
```
---

## Exercise 2

```js 
let myArray = ["a", "b", "c", "d"];
// change code below this line
myArray[1] = "ask";
//change code above this line
console.log(myArray);
```
---

## Exercise 3

```js 
function mixedNumbers(arr) {
  // change code below this line
arr.push(7, 'VIII', 9);
arr.unshift('I', 2, 'three')
  // change code above this line
  return arr;
}

// do not change code below this line
console.log(mixedNumbers(['IV', 5, 'six']));
```
---

## Exercise 4

```js 
function popShift(arr) {
  let popped = arr.pop();  // change this line
  let shifted = arr.shift(); // change this line
  return [shifted, popped];
}

// do not change code below this line
console.log(popShift(['challenge', 'is', 'not', 'complete']));
```
---
## Exercise 5

```js 
function sumOfTen(arr) {
  // change code below this line
  arr.splice(1,2);
  // change code above this line
  return arr.reduce((a, b) => a + b);
}

// do not change code below this line
console.log(sumOfTen([2, 5, 1, 5, 2, 1]));
```
---

## Exercise 6

```js 
function htmlColorNames(arr) {
  // change code below this line
arr.splice(0,2, 'DarkSalmon', 'BlanchedAlmond'); 

  // change code above this line
  return arr;
} 
 
// do not change code below this line
console.log(htmlColorNames(['DarkGoldenRod', 'WhiteSmoke', 'LavenderBlush', 'PaleTurqoise', 'FireBrick']));
```
---


## Exercise 7

```js 
function forecast(arr) {
  // change code below this line

  return arr.slice(2,4);
}

// do not change code below this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```
---

## Exercise 8

```js 
function copyMachine(arr, num) {
  let newArr = [];
  while (num >= 1) {
    // change code below this line
newArr.push([...arr]);
    // change code above this line
    num--;
  }
  return newArr;
}

// change code here to test different cases:
console.log(copyMachine([true, false, true], 2));
```
---

## Exercise 9

```js 
function spreadOut() {
  let fragment = ['to', 'code'];
  let sentence = ['learning', ...fragment, 'is', 'fun'];// change this line
  return sentence;
}

// do not change code below this line
console.log(spreadOut());
```
---

## Exercise 10

```js 
function quickCheck(arr, elem) {
  // change code below this line
if(arr.indexOf(elem) >= 0) {
    return true;
  } else {
    return false;
  }
  // change code above this line
}

// change code here to test different cases:
console.log(quickCheck(['squash', 'onions', 'shallots'], 'mushrooms'));
```
---

## Exercise 11

```js 
function filteredArray(arr, elem) {
  let newArr = [];
  // change code below this line
for (let i = 0; i<arr.length; i++) {
    if (arr[i].indexOf(elem) < 0) {
      newArr.push(arr[i]);
    }
  }
  // change code above this line
  return newArr;
}

// change code here to test different cases:
console.log(filteredArray([[3, 2, 3], [1, 6, 3], [3, 13, 26], [19, 3, 9]], 3));
```
---

## Exercise 12

```js 
let myNestedArray = [ //level 1
  // change code below this line
  ['unshift', false, 1, 2, 3, 'complex', 'nested'], //level 2
  [ 
    ['loop', 'shift', 6, 7, 1000, 'method', 'deep'], //level 3
    [ 
      ['concat', false, true, 'deeper', 'spread', 'array'], //level 4
      [
        ['deepest', 'mutate', 1327.98, 'splice', 'slice', 'push'] //level 5
      ]
    ]
  ],
  ['iterate', 1.3849, 7, '8.4876', 'arbitrary', 'depth']
  // change code above this line
];
```
---

## Exercise 13

```js 
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28
};

// change code below this line
foods.bananas = 13;
foods.grapes = 35;
foods.strawberries = 27;
// change code above this line

console.log(foods);
```
---

## Exercise 14

```js 
let userActivity = {
  id: 23894201352,
  date: 'January 1, 2017',
  data: {
    totalUsers: 51,
    online: 42
  }
};

// change code below this line
userActivity["data"]["online"] = 45;
// change code above this line

console.log(userActivity);
```
---

## Exercise 15

```js 
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
};
// do not change code above this line

function checkInventory(scannedItem) {
  // change code below this line
  return foods[scannedItem];
}

// change code below this line to test different cases:
console.log(checkInventory("apples"));
```
---

## Exercise 16

```js 
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
};

// change code below this line
delete foods.oranges;
delete foods.plums;
delete foods.strawberries;
// change code above this line

console.log(foods);
```
---


## Exercise 17

```js 
let users = {
  Alan: {
    age: 27,
    online: true
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: true
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function isEveryoneHere(obj) {
  // change code below this line
 if(obj.hasOwnProperty('Alan', 'Jeff', 'Sarah', 'Ryan')) {
    return true;
  } else {
    return false;
  }
  // change code above this line
}

console.log(isEveryoneHere(users));
```
---

## Exercise 18

```js 
let users = {
  Alan: {
    age: 27,
    online: false
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: false
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function countOnline(obj) {
  // change code below this line
let n = 0;
  for (let user in obj) if (obj[user].online) n++;
    return n;
  // change code above this line
}

console.log(countOnline(users));
```
---

## Exercise 19

```js 
let users = {
  Alan: {
    age: 27,
    online: false
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: false
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function getArrayOfUsers(obj) {
  // change code below this line
 return Object.keys(obj);
  // change code above this line
}

console.log(getArrayOfUsers(users));
```
---

## Exercise 20

```js 
let user = {
  name: 'Kenneth',
  age: 28,
  data: {
    username: 'kennethCodesAllDay',
    joinDate: 'March 26, 2016',
    organization: 'freeCodeCamp',
    friends: [
      'Sam',
      'Kira',
      'Tomo'
    ],
    location: {
      city: 'San Francisco',
      state: 'CA',
      country: 'USA'
    }
  }
};

function addFriend(userObj, friend) {
  // change code below this line  
userObj.data.friends.push(friend);
return userObj.data.friends;
  // change code above this line
}

console.log(addFriend(user, 'Pete'));
```
---

