## Exercise 72

```js 
var names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"];
function golfScore(par, strokes) {
 
  if (strokes === 1) {
    return "Hole-in-one!";
  }
  else if (strokes <= (par - 2)) {
    return "Eagle";
  }
  else if (strokes === (par-1)) {
    return "Birdie";
  }
  else if (strokes === par) {
    return "Par";
  }
  else if (strokes === (par+1)) {
    return "Bogey";
  }
  else if (strokes === (par+2)) {
    return "Double Bogey";
  }
  else if(strokes >= (par+3)) {
    return "Go Home!";
  }
  return "Change Me";
```

don't forget the paranthesis! 

---

## Exercise 73

```js 
function caseInSwitch(val) {
  var answer = "";
  switch(val) {
    case 1:
    answer = "alpha";
    break;
    case 2:
    answer = "beta";
    break;    
    case 3:
    answer = "gamma";
    break;    
    case 4:
    answer = "delta";
    break;    
  }
```

If you have many options to choose from, use a switch statement


---

## Exercise 74

```js 
function switchOfStuff(val) {
  var answer = "";
  switch(val) {
    case 'a':
    answer = "apple";
    break;    
    case 'b':
    answer = "bird";
    break;    
    case 'c':
    answer = "cat";
    break;
    default:
    answer = "stuff";
    break;
  }
```

you can add the default statement which will be executed if no matching case statements are found.


---

## Exercise 75

```js 
function sequentialSizes(val) {
  var answer = "";
  switch(val) {
    case 1:
    case 2:
    case 3:
    answer = "Low";
    break;
    case 4:
    case 5:
    case 6:
    answer = "Mid";
    break;
    case 7:
    case 8:
    case 9:
    answer = "High"
    break;
  }
```

If you have multiple inputs with the same output, the following case statement(s) are executed until a break is encountered.


---

## Exercise 76

```js 
function chainToSwitch(val) {
  var answer = "";  
  switch(val) {
    case "bob":
    answer = "Marley";
    break;
    case 42:
    answer = "The Answer";
    break;
    case 1:
    answer = "There is no #1";
    break;
    case 99:
    answer = "Missed me by this much!";
    break;
    case 7:
    answer = "Ate Nine";
    break;         

  }

```

you can use switch statement instead of if/else if. 

---
## Exercise 77

```js 
function isLess(a, b) {
return (a<b);
}
```

boolean but you haven't to use if/else if statements. 

---
## Exercise 78

```js 
function abTest(a, b) {
  if(a<0 || b<0) {  
  return undefined;
  }  
  return Math.round(Math.pow(Math.sqrt(a) + Math.sqrt(b), 2));
}
```

When a return statement is reached, the execution of the current function stops and control returns to the calling location.


---
## Exercise 79

```js 
??????
```

---
## Exercise 80

```js 
// Example
var ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};

var myDog = {
  "name": "Ask",
  "legs": 4,
  "tails": 1,
  "friends": ["me!"]
};
```

Objects are similar to arrays, except that instead of using indexes to access and modify their data, you access the data in objects through what are called properties.


---
## Exercise 81

```js 
var testObj = {
  "hat": "ballcap",
  "shirt": "jersey",
  "shoes": "cleats"
};

var hatValue = testObj.hat;      
var shirtValue = testObj.shirt;   
```

There are two ways to access the properties of an object: dot notation (.) and bracket notation ([]), similar to an array.


---
## Exercise 82

```js 
var testObj = {
  "an entree": "hamburger",
  "my side": "veggies",
  "the drink": "water"
};
var entreeValue = testObj["an entree"];   
var drinkValue = testObj["the drink"]; 
```

the second way to access the properties of an object is bracket notation ([]). If the property of the object you are trying to access has a space in its name, you will need to use bracket notation.


---
## Exercise 83

```js 
var testObj = {
  12: "Namath",
  16: "Montana",
  19: "Unitas"
};

var playerNumber = 16;      
var player = testObj[playerNumber];
```

Another use of bracket notation on objects is to access a property which is stored as the value of a variable. This can be very useful for iterating through an object's properties or when accessing a lookup table.


---
## Exercise 84

```js 

var ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};

ourDog.name = "Happy Camper";


var myDog = {
  "name": "Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"]
};
myDog.name = "Happy Coder"
```

After you've created a JavaScript object, you can update its properties at any time just like you would update any other variable. You can use either dot or bracket notation to update.


---
## Exercise 85

```js 
var myDog = {
  "name": "Happy Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"]
};
myDog.bark = "woof";
```

you can add new properties to existing JavaScript objects the same way you would modify them.


---
## Exercise 86

```js 

var myDog = {
  "name": "Happy Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"],
  "bark": "woof"
};
delete myDog.tails;

```

We can also delete properties from objects like this.

---
## Exercise 87

```js 
function phoneticLookup(val) {
  var result = "";

 var lookup = {
   "alpha" : "Adams",
   "bravo": "Boston",
  "charlie": "Chicago",
    "delta": "Denver",
   "echo": "Easy",
   "foxtrot": "Frank",
  }
result = lookup[val];
  return result;
}
```

Objects can be thought of as a key/value storage, like a dictionary. If you have tabular data, you can use an object to "lookup" values. This is most useful when you know that your input data is limited to a certain range.


---
## Exercise 88

```js 
var myObj = {
  gift: "pony",
  pet: "kitten",
  bed: "sleigh"
};

function checkObj(checkProp) {
  if(myObj.hasOwnProperty(checkProp)){  
  return myObj[checkProp];
}
else {
  return "Not Found";
}
}
```

Sometimes it is useful to check if the property of a given object exists or not. We can use the .hasOwnProperty(propname) method of objects to determine if that object has the given property name. .hasOwnProperty() returns true or false if the property is found or not.

---
## Exercise 89

```js 
var myMusic = [
  {
    "artist": "Billy Joel",
    "title": "Piano Man",
    "release_year": 1973,
    "formats": [ 
      "CD",
      "8T",
      "LP"
    ],
    "gold": true
  },
{  
"artist": " Joel",
    "title": "Man",
    "release_year": 1979,
    "formats": [ 
      "CD",
      "8T",
      "mp3"]
}
]; 
```

You will need to place a comma after every object in the array, unless it is the last object in the array.


---
## Exercise 90

```js 

var myStorage = {
  "car": {
    "inside": {
      "glove box": "maps",
      "passenger seat": "crumbs"
     },
    "outside": {
      "trunk": "jack"
    }
  }
};

var gloveBoxContents = myStorage.car.inside["glove box"];
```

The sub-properties of objects can be accessed by chaining together the dot or bracket notation.


---
## Exercise 91

```js 

var myPlants = [
  { 
    type: "flowers",
    list: [
      "rose",
      "tulip",
      "dandelion"
    ]
  },
  {
    type: "trees",
    list: [
      "fir",
      "pine",
      "birch"
    ]
  }  
];

var secondTree = myPlants[1].list[1];
```

As we have seen in earlier examples, objects can contain both nested objects and nested arrays. Similar to accessing nested objects, Array bracket notation can be chained to access nested arrays.


---
## Exercise 92

```js 

var collection = {
    "2548": {
      "album": "Slippery When Wet",
      "artist": "Bon Jovi",
      "tracks": [ 
        "Let It Rock", 
        "You Give Love a Bad Name" 
      ]
    },
    "2468": {
      "album": "1999",
      "artist": "Prince",
      "tracks": [ 
        "1999", 
        "Little Red Corvette" 
      ]
    },
    "1245": {
      "artist": "Robert Palmer",
      "tracks": [ ]
    },
    "5439": {
      "album": "ABBA Gold"
    }
};
// Keep a copy of the collection for tests
var collectionCopy = JSON.parse(JSON.stringify(collection));

// Only change code below this line
function updateRecords(id, prop, value) {
  if (value === '') {
    delete collection[id][prop]; // If the value is empty remove the prop
  } else if (prop !== "tracks") {
    collection[id][prop] = value;
  } else {
    if (!collection[id].hasOwnProperty('tracks')) {
      collection[id].tracks = [];
      collection[id].tracks.push(value);
    } else {
      collection[id].tracks.push(value);
    }
  }
  
  return collection;
}
```

---
## Exercise 93

```js 
var myArray = [];
var i = 0;
while(i<5) {
  myArray.push(i);
  i++;
}
```


---
## Exercise 94

```js 
var myArray = [];
for (var i = 1; i<6; i++) {
  myArray.push(i);
}
```

For loops are declared with three optional expressions separated by semicolons:


---
## Exercise 95

```js 
var myArray = [];
for (var i = 1; i < 10; i += 2) {
  myArray.push(i);
}
```

By changing our final-expression, we can count by even numbers.


---
## Exercise 96

```js 
var myArray = [];
for (var i = 9; i > 0; i -= 2) {
  myArray.push(i);
}
```

[9,7,5,3,1]
---
## Exercise 97

```js 
var myArr = [ 2, 3, 4, 5, 6];
var total = 0;

for (var i = 0; i < myArr.length; i++) {
  total += myArr[i];
}
```

A common task in JavaScript is to iterate through the contents of an array. 

---
## Exercise 98

```js 

```

---
## Exercise 99

```js 

```

---
## Exercise 100

```js 

```

---
## Exercise 72

```js 

```

---
## Exercise 72

```js 

```

---
