## Exercise 1 

```js 
// There is a cat. 
/* There is a car. */
```

Comment line //
comment paragraph /* ... */

---

## Exercise 2 

```js
// Declare myName below this line
var myName;
```

variables => var ... It may not start with a number and contain spaces. 

---

## Exercise 3

```js
var a = 7;
var b = a;
```
read it from right to left 

---

## Exercise 4

```js
var a = 9;
```

defining 

---

## Exercise 5

```js
// Initialize these three variables
var a = 5;
var b = 10;
var c = "I am a";
```

 a and b are defined. c is undefined.
 
 ---

## Exercise 6

```js
// Declarations
var studlyCapVar;
var properCamelCase;
var titleCaseOver;

// Assignments
var studlyCapVar = 10;
var properCamelCase = "A String";
var titleCaseOver = 9000;
```

camelCase  => first letter of first word should be lowercase but the others should be capitalized. 

---

## Exercise 7

```js
var sum = 10 + 10;
```

write "+" between two items for addition

---

## Exercise 8

```js
var difference = 45 - 33;
```

write "-" between two items for subtract

---

## Exercise 9

```js
var product = 8 * 10;
```

write "*" between two items for multiplication

---

## Exercise 10

```js
var quotient = 66 / 33;
```

write "/" between two items for division

---

## Exercise 11

```js
var myVar = 87;

// Only change code below this line
myVar++;
```

put ++ to add one 

---

## Exercise 12

```js
var myVar = 11;

// Only change code below this line
myVar--;
```

put -- for decrement one

---

## Exercise 13

```js
var myDecimal = 6.5;
```

put point to give a decimal value

---

## Exercise 14

```js
var product = 2.0 * 2.5;
```

same process is available for decimal value (mathematical operation)

---

## Exercise 15

```js
var quotient = 4.4 / 2.0; 
```

same process is available for decimal value (mathematical operation)

---

## Exercise 16

```js
var remainder = 11 % 3;
```

 % gives the remainder of the division of two numbers
 
---

## Exercise 17

```js
var a = 3;
var b = 17;
var c = 12;

a += 12;
b += 9;
c += 7;
```

a = 3+12 = 15
b = 17+9 = 26
c = 7+12 =19

---

## Exercise 18

```js
var a = 11;
var b = 9;
var c = 3;

a -= 6;
b -= 15;
c -= 1;
```

a=11-6=5
b=9-15=-6
c=3-1=2

---

## Exercise 19

```js
var a = 5;
var b = 12;
var c = 4.6;

// Only modify code below this line

a *= 5;
b *= 3;
c *= 10;
```

a=25
b=36
c=46

---

## Exercise 20

```js
var a = 48;
var b = 108;
var c = 33;

// Only modify code below this line

a /= 12;
b /= 4;
c /= 11;
```

a=4
b=27
c=3

---

## Exercise 21

```js
var myFirstName = "Sena";
var myLastName = "Avci";
```

string literal??

---

## Exercise 22

```js
var myStr = "I am a \"double quoted\" string inside \"double quotes\".";
```

put \ to show your writing in Quotations marks 

---

## Exercise 23

```js
var myStr = '<a href="http://www.example.com" target="_blank">Link</a>';
```

" and ' have same meaning. you can use one of them instead of \. 

---

## Exercise 24

```js
var myStr = "FirstLine\n\t\\SecondLine\nThirdLine"
```

Escape Sequences

---

## Exercise 25

```js
var myStr = "This is the start. " + "This is the end.";
```

+ makes strings together

---

## Exercise 26

```js
var myStr = "This is the first sentence. ";
myStr += "This is the second sentence.";
```

another way (+=) to make strings together

---

## Exercise 27

```js
var myName = "Sena Avci"
var myStr = "My name is " + myName + " and I am well!";
```

here it says; My name is Sena Avci and I am well!

---

## Exercise 28

```js
var someAdjective = "amazing!";
var myStr = "Learning to code is ";
myStr += someAdjective;
```

here it says; Learning to code is amazing!

---

## Exercise 29

```js
lastNameLength = lastName.length;
```

write .length to find the length of a string value 

---

## Exercise 30

```js
firstLetterOfLastName = lastName[0];
```

JS start to count at 0.  Bracket notation is a way to get a character at a specific index within a string.

---

## Exercise 31

```js
var myStr = "Jello World";

// Only change code below this line

myStr ="Hello World"; 
```

In JS, string cannot change once created. you can change it as assign a new string.

---

## Exercise 32

```js
var lastName = "Lovelace";
var thirdLetterOfLastName = lastName[2];
```

In JS, zeroth caracter is first letter. so; third letter is second caracter. 

---

## Exercise 33

```js
var lastName = "Lovelace";
var lastLetterOfLastName = lastName[lastName.length - 1];
```

add bracket notation with .length-1 to find the last letter. 

---

## Exercise 34

```js
var lastName = "Lovelace";
var secondToLastLetterOfLastName = lastName[lastName.length - 2];
```

add bracket notation with .length-x to find the xth letter. 

---

## Exercise 35

```js 
function wordBlanks(myNoun, myAdjective, myVerb, myAdverb) {
  var result = "My" + " " + myAdjective + " " + myNoun + " " + myVerb + " " + myAdverb + "." ;
  return result;
}
wordBlanks("dog", "big", "ran", "quickly");
```

you can write new things with (" " +) in variables. 

---

## Exercise 36

```js 
var myArray = ["Sena", 26];
```

you can array the data with bracket, " " and put a comma between each entry. 
but if you want to write a number, don't use " ". If it is value, use " ". 

---

## Exercise 37

```js 
var myArray = [["ask", 21], ["never", 343]];
```

nest arrays within other arrays.

---

## Exercise 38

```js 
var myArray = [50,60,70];
var myData = myArray[0]; // equals 50
```

same way to find first caracter

---

## Exercise 39

```js 
var myArray = [18,64,99];
myArray[0] = 45; // equals [45,64,99]
```

same way to change one of caracters

---

## Exercise 40

```js
var myArray = [[1,2,3], [4,5,6], [7,8,9], [[10,11,12], 13, 14]];
var myData = myArray[2][1];
```

myData = 8

---

## Exercise 41

```js
var myArray = [["John", 23], ["cat", 2]];
myArray.push(["dog", 3]);
```

you can add new data at the end of the var with .push(). 

---

## Exercise 42

```js
var myArray = [["John", 23], ["cat", 2]];
var removedFromMyArray = myArray.pop();
```

you can remove a data at the end of the var with .pop(). 
myArray = [["John", 23]]

---

## Exercise 43

```js
var myArray = [["John", 23], ["dog", 3]];
var removedFromMyArray = myArray.shift();
```

you can remove a data at first of the var with .shift(). 
myArray = [["dog", 3]]

---

## Exercise 44

```js
var myArray = [["John", 23], ["dog", 3]];
myArray.shift();
myArray.unshift(["Paul",35]);
```

you can add a data at first of the var with .unshift(). 
myArray =  [["Paul", 35], ["dog", 3]].

---

## Exercise 45

```js
var myList = [["Ice Cream", 12], ["Chocolate", 2], ["sugar", 3], ["cake", 5], ["nuddle", 2]];
```

the name of the item,  number representing the quantity

---

## Exercise 46

```js
function reusableFunction() {
    console.log("Hi World");
}
reusableFunction();
```

you write => Hi World

---

## Exercise 47

```js
function functionWithArgs(a, b) {
  console.log(a+b);
} 
functionWithArgs(3, 6); //Outputs 9
```

When a function is defined, it is typically defined along with the parameters

---

## Exercise 48

```js
var myGlobal = 10;
function fun1() {
  oopsGlobal = 5
}   
```

you can assign number to the data with or without var and it can be seemed in all JS (global)

---

## Exercise 49

```js
function myLocalScope() {
  'use strict'; 
  var myVar = "foo";
  console.log(myVar);
}
myLocalScope();
```

the function parameters have local scope. they are only visible within that function.


---

## Exercise 50

```js
var outerWear = "T-Shirt";
function myOutfit() {
  var outerWear = "sweater"
    return outerWear;
```

function is present so outerwear is sweater. but in general it is T-shirt

---

## Exercise 51

```js
function timesFive (num) {
  return num * 5;
}
```

return the number what you want

---

## Exercise 52

```js
var sum = 0;
function addFive() {
  sum = sum + 5;
}
```



---

## Exercise 53

```js
var processed = 0;
function processArg(num) {
  return (num + 3) / 5;
}
processed = processArg(7);
```

write a function, give a number, assign to var 

---

## Exercise 54

```js
function nextInLine(arr, item) {
  arr.push(item); 
  var removed = arr.shift(); 
  return removed;  
}
```

added item, removed arr than returned it

---

## Exercise 55

```js
function welcomeToBooleans() {
return true; 
}
welcomeToBooleans();
```

welcomeToBooleans become true 
Boolean conditions is true or false 

---

## Exercise 56

```js
function trueOrFalse(wasThatTrue) {
  if (wasThatTrue) {
      return "Yes, that was true";
  }
  return "No, that was false"; 
  
```

If statements are used to make decisions in code. if your comment is ok, there will write your if statements. 

---

## Exercise 57

```js
function testEqual(val) {
  if (val == 12) { 
    return "Equal";
  }
  return "Not Equal";
}
```

equality operator == The equality operator compares two values and returns true if they're equivalent or false if they are not. 
3 == "3" => true

---

## Exercise 58

```js
function testStrict(val) {
  if (val === 7) { 
    return "Equal";
  }
  return "Not Equal";
}
```

Strict equality (===) 
3 === "3" => false

---

## Exercise 59

```js
function compareEquality(a, b) {
  if (a === b) { 
    return "Equal";
  }
  return "Not Equal";
}
```

Strict equality

---

## Exercise 60

```js

```



---

## Exercise 60

```js
function testNotEqual(val) {
  if (val != 99) {
    return "Not Equal";
  }
  return "Equal";
}
```

(!=) is the opposite of the equality operator. It means "Not Equal" and returns false where equality would return true

---

## Exercise 61

```js
function testStrictNotEqual(val) {  
  if (val !== 17) {
    return "Not Equal";
  }
  return "Equal";
}
```

(!==) is the logical opposite of the strict equality operator.
It means "Strictly Not Equal" and returns false where strict equality would return true

---

## Exercise 62

```js

function testGreaterThan(val) {
  if (val > 100) {  
    return "Over 100";
  }

  if (val > 10) {  
    return "Over 10";
  }

  return "10 or Under";
}

testGreaterThan(10);
```

(>) compares the values of two numbers. true/false

---

## Exercise 63

```js
function testGreaterOrEqual(val) {
  if (val >= 20) {  
    return "20 or Over";
  }
  
  if (val >= 10) {  
    return "10 or Over";
  }

  return "Less than 10";
}
```

greater than or equal to operator (>=) compares the values of two numbers

---

## Exercise 64

```js
function testLessThan(val) {
  if (val < 25) { 
    return "Under 25";
  }
  
  if (val < 55) {
    return "Under 55";
  }

  return "55 or Over";
}
```

(<) compares the values of two numbers. true/false. less

---

## Exercise 65

```js
function testLessOrEqual(val) {
  if (val <= 12) {  
    return "Smaller Than or Equal to 12";
  }
  
  if (val <= 24) { 
    return "Smaller Than or Equal to 24";
  }

  return "More Than 24";
}
```

less than or equal to operator (<=) compares the values of two numbers

---

## Exercise 66

```js
function testLogicalAnd(val) {
  if (val <= 50 && val >= 25) {
      return "Yes";

  }
  return "No";
```

val is less than or equal to 50 and greater than or equal to 25. 

---

## Exercise 67

```js
function testLogicalOr(val) {
  if (val < 10 || val > 20 ) {
    return "Outside";

  }
  return "Inside";
```

 "Outside" if val is not between 10 and 20. Otherwise, return "Inside".

---

## Exercise 68

```js
function testElse(val) {
  var result = ""  
  if (val > 5) {
    result = "Bigger than 5";
  }
  
 else {
    result = "5 or Smaller";
  }
    return result;
```

With an else statement, an alternate block of code can be executed.

---

## Exercise 69

```js
function testElseIf(val) {
  if (val > 10) {
    return "Greater than 10";
  }
  
  else if (val < 5) {
    return "Smaller than 5";
  }
  else {    
  return "Between 5 and 10";
}
 }
```

multiple conditions that need to be addressed => else if

---

## Exercise 70

```js
function orderMyLogic(val) {
  if (val < 5) {
    return "Less than 5";
    
  } else if (val < 10) {
    return "Less than 10";
  } else {
    return "Greater than or equal to 10";
  }
}
```

4 is assigned both of them. but the first val will be valid. 

---

## Exercise 71

```js
function testSize(num) {
 if (num < 5)  {
   return "Tiny";
 }
 else if (num < 10) {
   return "Small";
 }
  else if (num < 15) {
    return "Medium";
  }
  else if (num < 20) {
     return "Large";
  }
  else if (num >= 20) {  
    return "Huge";
  }
 else { 
  return "Change Me";
 }
 
}
```

multiple chained if / else if statements

---
























