## Exercise 1

```js
{
  const x = ; // experiment with different values 
  const truthiness_x = Boolean(x);

  if (truthiness_x) {
    console.log("truthy: " + typeof x + ", " + x);
  } else {
    console.log("falsey: " + typeof x + ", " + x);
  };
};
values to try:

a: true       --> "truthy: boolean, true"
a: false      --> "falsey: boolean, false"
a: 0          --> "falsey: number, 0"
a: 1           --> "truthy: number, 1"
a: null       --> "falsey: object, null"
a: undefined  --> "falsey: undefined, undefined"
a: ''         --> "falsey: string, "
a: ' '        --> "truthy: string,  "
a: 'tiil'     --> "truthy: string, tiil"
a: 2          --> "truthy: number, 2"
a: 345        --> "truthy: number, 345"
a: NaN        --> "falsey: number, NaN"
a: Infinity   --> "truthy: number, Infinity"
a: -Infinity  --> "truthy: number, -Infinity"
a: -3         --> "truthy: number, -3"
a: -0.0       --> "falsey: number, 0"

```
---

## Exercise 2

```js
{
  const a = ;
  
  const truthiness = Boolean(a);
  
  console.log(typeof a + ", " + a + ", " + truthiness + "y");
};
the values:

1: false      --> boolean, false, falsey

2: null       --> object, null, falsey

3: undefined  --> undefined, undefined, falsey

4: ''         --> string, , falsey
4: ""         --> string, , falsey
4: ``         --> string, , falsey

5: NaN        --> number, NaN, falsey

6: 0          --> number, 0, falsey
6: 0.0        --> number, 0, falsey
6: +0         --> number, 0, falsey
6: -0         --> number, 0, falsey

```
---

## Exercise 2

```js
 
  const x = ; // experiment with different values 

  const coerce_truthiness = Boolean(x);
  const ternary_truthiness = (x) ? "truthy" : "falsey" ;
  
  const tern_option = (x) ? "first" : "second" ;
  const tern_numbers = (x) ? 1 : 2 ;
  const tern_boolean = (x) ? true : false ;

  console.log("x: " + typeof x + ", " + x);
  console.log("coerced: " + coerce_truthiness);
  console.log("ternaried: " + ternary_truthiness);
  console.log("option: " + tern_option);
  console.log("numbers: " + tern_numbers);
  console.log("booleans: " + tern_boolean);
};
Ternary operators can only have two options.

values to try:

a: true       --> 
x: boolean, true
coerced: true
ternaried: truthy
option: first
numbers: 1
booleans: true

a: false      --> 
x: boolean, false
coerced: false
ternaried: falsey
option: second
numbers: 2
booleans: false

a: 0          --> 
x: number, 0
coerced: false
ternaried: falsey
option: second
numbers: 2
booleans: false

a: 1          --> 
x: number, 1
coerced: true
ternaried: truthy
option: first
numbers: 1
booleans: true

a: null       --> 
x: object, null
coerced: false
ternaried: falsey
option: second
numbers: 2
booleans: false

a: undefined  --> 
x: undefined, undefined
coerced: false
ternaried: falsey
option: second
numbers: 2
booleans: false

a: ''         --> 
x: string, 
coerced: false
ternaried: falsey
option: second
numbers: 2
booleans: false

a: ' '        --> 
x: string,  
coerced: true
ternaried: truthy
option: first
numbers: 1
booleans: true

a: 'tiil'     --> 
x: string, tiil
coerced: true
ternaried: truthy
option: first
numbers: 1
booleans: true

a: 2          --> 
x: number, 2
coerced: true
ternaried: truthy
option: first
numbers: 1
booleans: true

a: 345        --> 
x: number, 345
coerced: true
ternaried: truthy
option: first
numbers: 1
booleans: true

a: NaN        --> 
x: number, NaN
coerced: false
ternaried: falsey
option: second
numbers: 2
booleans: false

a: Infinity   --> 
x: number, Infinity
coerced: true
ternaried: truthy
option: first
numbers: 1
booleans: true

a: -Infinity  --> 
x: number, -Infinity
coerced: true
ternaried: truthy
option: first
numbers: 1
booleans: true

a: -3         --> 
x: number, -3
coerced: true
ternaried: truthy
option: first
numbers: 1
booleans: true

a: -0.0       --> 
x: number, 0
coerced: false
ternaried: falsey
option: second
numbers: 2
booleans: false

```
---

## Exercise 3

```js
 { 
  const a = ; // experiment with different values 
  const b = ; // experiment with different values 

  const and = a && b;
  const replication = (a) ? b : a ;
  
  console.log("a: "+typeof a+", "+a+", "+!!a+"y");
  console.log("b: "+typeof b+", "+b+", "+!!b+"y");
  
  console.log("and: " + and);
  console.log("replication: " + replication);
};



a: true, b:false      --> 

a: boolean, true, truey
b: boolean, false, falsey
and: false
replication: false

a: false, b:true      --> 

a: boolean, false, falsey
b: boolean, true, truey
and: false
replication: false

a: 0, b:1             --> 

a: number, 0, falsey
b: number, 1, truey
and: 0
replication: 0

a: 1, b:0             --> 

a: number, 1, truey
b: number, 0, falsey
and: 0
replication: 0

a: null, b:false      --> 

a: object, null, falsey
b: boolean, false, falsey
and: null
replication: null

a: false, b:null      --> 

a: boolean, false, falsey
b: object, null, falsey
and: false
replication: false

a: '', b:' '          --> 

a: string, , falsey
b: string,  , truey
and: 
replication:

a: ' ', b:''          --> 

a: string,  , truey
b: string, , falsey
and: 
replication:

a: 2, b:3             --> 

a: number, 2, truey
b: number, 3, truey
and: 3
replication: 3

a: 3, b:2             --> 

a: number, 3, truey
b: number, 2, truey
and: 2
replication: 2
 
 ```
---

## Exercise 4

```js
{ 
  const a = ; // experiment with different values 
  const b = ; // experiment with different values 

  const or = a || b;
  const replication = (a) ? a : b ;
  
  console.log("a: "+typeof a+", "+a+", "+!!a+"y");
  console.log("b: "+typeof b+", "+b+", "+!!b+"y");
  
  console.log("or: " + or);
  console.log("replication: " + replication);
};

a: true, b:false      --> 

a: boolean, true, truey
b: boolean, false, falsey
or: true
replication: true

a: false, b:true      --> 

a: boolean, false, falsey
b: boolean, true, truey
or: true
replication: true

a: 0, b:1             --> 

a: number, 0, falsey
b: number, 1, truey
or: 1
replication: 1

a: 1, b:0             --> 

a: number, 1, truey
b: number, 0, falsey
or: 1
replication: 1

a: null, b:false      --> 

a: object, null, falsey
b: boolean, false, falsey
or: false
replication: false

a: false, b:null      --> 

a: boolean, false, falsey
b: object, null, falsey
or: null
replication: null

a: '', b:' '          --> 

a: string, , falsey
b: string,  , truey
or:  
replication:

a: ' ', b:''          --> 

a: string,  , truey
b: string, , falsey
or:  
replication:

a: 2, b:3             --> 

a: number, 2, truey
b: number, 3, truey
or: 2
replication: 2

a: 3, b:2             --> 

a: number, 3, truey
b: number, 2, truey
or: 3
replication: 3


 ```
---

## Exercise 5

```js
{ 
  const a = ; // experiment with different values 

  const not = !a;
  const coercion_replication = !Boolean(a);
  const ternary_replication = (a) ? false : true ;

  console.log("a: "+typeof a+", "+a+", "+!!a+"y");
  console.log("not operator: " + not);
  console.log("with coercion: " + coercion_replication);  
  console.log("with ternary: " + ternary_replication);  
};

a: true       --> 

a: boolean, true, truey
not operator: false
with coercion: false
with ternary: false

a: false      --> 

a: boolean, false, falsey
not operator: true
with coercion: true
with ternary: true

a: 0          --> 

a: number, 0, falsey
not operator: true
with coercion: true
with ternary: true

a: 1          --> 

a: number, 1, truey
not operator: false
with coercion: false
with ternary: false

a: null       --> 

a: object, null, falsey
not operator: true
with coercion: true
with ternary: true

a: undefined  --> 

a: undefined, undefined, falsey
not operator: true
with coercion: true
with ternary: true

a: ''         --> 

a: string, , falsey
not operator: true
with coercion: true
with ternary: true

a: ' '        --> 

a: string,  , truey
not operator: false
with coercion: false
with ternary: false

a: 'tiil'     --> 

a: string, till, truey
not operator: false
with coercion: false
with ternary: false

a: 2          --> 

a: number, 2, truey
not operator: false
with coercion: false
with ternary: false

a: 345        --> 

a: number, 345, truey
not operator: false
with coercion: false
with ternary: false

a: NaN        --> 

a: number, NaN, falsey
not operator: true
with coercion: true
with ternary: true

a: Infinity   --> 

a: number, Infinity, truey
not operator: false
with coercion: false
with ternary: false

a: -Infinity  --> 

a: number, -Infinity, truey
not operator: false
with coercion: false
with ternary: false

a: -3         --> 

a: number, -3, truey
not operator: false
with coercion: false
with ternary: false

a: -0.0       --> 

a: number, 0, falsey
not operator: true
with coercion: true
with ternary: true

 ```
---
















