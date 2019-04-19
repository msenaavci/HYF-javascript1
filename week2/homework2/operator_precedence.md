# Operator Precedence

you'll be presented with a single line expression.  your task is to break it into steps according to operator precedence.  The main objective for these exercises is that you become comfortable stepping through and working with complex JS expressions, not that your learn everything about how all operators work.  Understanding implicit coercion is very important but will be covered in depth later on.  

learning objectives
* which operators exist in JS
* operator precedence
* breaking down long expressions (super helpful for debugging, reading & writing code)
* statements vs. expressions



### Index
* [completed examples](#completed-examples)
* exercises
  * [types & casting](#types-and-casting)
  * [logical operators](#logical-operators)
  * [arithmetic operators](#arithmetic-operators)
  * [all primitive operators](#all-primitive-operators)
* [resources](#resources)

---

## Completed Examples

### 1


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=Number%28Boolean%28String%28a%29%29%29%0AString%28_%29%0ABoolean%28_%29%0ANumber%28_%29)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20Number%28Boolean%28String%28a%29%29%29%3B%0A%0Aconst%20val_1%20%3D%20String%28a%29%3B%0Aconst%20step_1%20%3D%20Number%28Boolean%28val_1%29%29%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20Boolean%28val_1%29%3B%0Aconst%20step_2%20%3D%20Number%28val_2%29%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20Number%28val_2%29%3B%0Aconst%20step_3%20%3D%20val_3%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = ;

  const expected = Number(Boolean(String(a)));

  const val_1 = String(a);
  const step_1 = Number(Boolean(val_1));
  console.assert(step_1 === expected, "step_1");

  const val_2 = Boolean(val_1);
  const step_2 = Number(val_2);
  console.assert(step_2 === expected, "step_2");

  const val_3 = Number(val_2);
  const step_3 = val_3;
  console.assert(step_3 === expected, "step_3");
}
```

### 2

[parsonized](https://janke-learning.github.io/parsonizer/?snippet=%28a%20%2B%20b%29%20%3D%3D%20%28a%20%3C%20c%29%0A_%20%2B%20_%0A_%20%3C%20_%0A_%20%3D%3D%20_%0A%0A%0A%0A)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20%28a%20%2B%20b%29%20%3D%3D%20%28a%20%3C%20c%29%3B%0A%0Aconst%20val_1%20%3D%20a%20%2B%20b%3B%0Aconst%20step_1%20%3D%20val_1%20%3D%3D%20%28a%20%3C%20c%29%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20a%20%3C%20c%3B%0Aconst%20step_2%20%3D%20val_1%20%3D%3D%20val_2%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20val_1%20%3D%3D%20val_2%3B%0Aconst%20step_3%20%3D%20val_3%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  

```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = , b = , c = ;

  const expected = (a + b) == (a < c);

  const val_1 = a + b;
  const step_1 = val_1 == (a < c);
  console.assert(step_1 === expected, "step_1");

  const val_2 = a < c;
  const step_2 = val_1 == val_2;
  console.assert(step_2 === expected, "step_2");

  const val_3 = val_1 == val_2;
  const step_3 = val_3;
  console.assert(step_3 === expected, "step_3");
}
```

### 3


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=b%20%26%26%20typeof%20a%20%3D%3D%3D%20'string'%0Atypeof%20_%0A_%20%3D%3D%3D%20'string'%0A_%20%26%26%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20b%20%26%26%20typeof%20a%20%3D%3D%3D%20'string'%3B%0A%0Aconst%20val_1%20%3D%20typeof%20a%3B%0Aconst%20step_1%20%3D%20val_1%20%3D%3D%3D%20'string'%20%26%26%20b%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20val_1%20%3D%3D%3D%20'string'%3B%0Aconst%20step_2%20%3D%20b%20%26%26%20val_2%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20b%20%26%26%20val_2%3B%0Aconst%20step_3%20%3D%20val_3%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = , b = ;

  const expected = b && typeof a === 'string';

  const val_1 = typeof a;
  const step_1 = val_1 === 'string' && b;
  console.assert(step_1 === expected, "step_1");

  const val_2 = val_1 === 'string';
  const step_2 = b && val_2;
  console.assert(step_2 === expected, "step_2");

  const val_3 = b && val_2;
  const step_3 = val_3;
  console.assert(step_3 === expected, "step_3");
}
```
[short-circuiting - an advanced gotcha](https://codeburst.io/javascript-what-is-short-circuit-evaluation-ff22b2f5608c)

### 4


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=%28b%20%26%26%20typeof%20a%29%20%3D%3D%3D%20'string'%0Atypeof%20_%0A_%20%26%26%20_%0A_%20%3D%3D%3D%20'string')  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20%28b%20%26%26%20typeof%20a%29%20%3D%3D%3D%20'string'%3B%0A%0Aconst%20val_1%20%3D%20typeof%20a%3B%0Aconst%20step_1%20%3D%20val_1%20%3D%3D%3D%20'string'%20%26%26%20b%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20b%20%26%26%20val_1%3B%0Aconst%20step_2%20%3D%20val_2%20%3D%3D%3D%20'string'%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20val_2%20%3D%3D%3D%20'string'%3B%0Aconst%20step_3%20%3D%20val_3%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = , b = ;

  const expected = (b && typeof a) === 'string';

  const val_1 = typeof a;
  const step_1 = val_1 === 'string' && b;
  console.assert(step_1 === expected, "step_1");

  const val_2 = b && val_1;
  const step_2 = val_2 === 'string';
  console.assert(step_2 === expected, "step_2");

  const val_3 = val_2 === 'string';
  const step_3 = val_3;
  console.assert(step_3 === expected, "step_3");
}
```


### 5


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=%28%20a%20%3E%20Number%28b%29%20%29%20%7C%7C%20String%28c%29%0ANumber%28_%29%0A_%20%3E%20_%0AString%28_%29%0A_%20%7C%7C%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20%28%20a%20%3E%20Number%28b%29%20%29%20%7C%7C%20String%28c%29%3B%0A%0Aconst%20val_1%20%3D%20Number%28b%29%3B%0Aconst%20step_1%20%3D%20%28%20a%20%3E%20val_1%20%29%20%7C%7C%20String%28c%29%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20a%20%3E%20val_1%3B%0Aconst%20step_2%20%3D%20%28%20val_2%20%29%20%7C%7C%20String%28c%29%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20String%28c%29%3B%0Aconst%20step_3%20%3D%20val_2%20%7C%7C%20val_3%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B%0A%0Aconst%20val_4%20%3D%20val_2%20%7C%7C%20val_3%3B%0Aconst%20step_4%20%3D%20val_4%3B%0Aconsole.assert%28step_4%20%3D%3D%3D%20expected,%20%22step_4%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = , b = , c = ;

  const expected = ( a > Number(b) ) || String(c);

  const val_1 = Number(b);
  const step_1 = ( a > val_1 ) || String(c);
  console.assert(step_1 === expected, "step_1");

  const val_2 = a > val_1;
  const step_2 = ( val_2 ) || String(c);
  console.assert(step_2 === expected, "step_2");

  const val_3 = String(c);
  const step_3 = val_2 || val_3;
  console.assert(step_3 === expected, "step_3");

  const val_4 = val_2 || val_3;
  const step_4 = val_4;
  console.assert(step_4 === expected, "step_4");
}
```
[short-circuiting - an advanced gotcha](https://codeburst.io/javascript-what-is-short-circuit-evaluation-ff22b2f5608c)



[TOP](#operator-precedence)

---
---

# Exercises

---

## Types and Casting

### types & casting 1


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=typeof%20a%20%3D%3D%3D%20typeof%20b%0Atypeof%20a%0Atypeof%20b%0A_%20%3D%3D%3D%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20typeof%20a%20%3D%3D%3D%20typeof%20b%3B%0A%0Aconst%20val_1%20%3D%20%3B%0Aconst%20step_1%20%3D%20%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20%3B%0Aconst%20step_2%20%3D%20%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20%3B%0Aconst%20step_3%20%3D%20%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
*/
const a = 1, b = true;

const expected = typeof a === typeof b;

const val_1 = b < a;
const step_1 = val_1 < -1;
console.assert(step_1 === expected, "step_1");

const val_2 = Number(a);
const step_2 = val_2 > 1;
console.assert(step_2 === expected, "step_2");

const val_3 = Boolean(b);
const step_3 = val_2 > val_3;
console.assert(step_3 === expected, "step_3");
```

### types & casting 2


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=Boolean%28a%29%20!%3D%3D%20Boolean%28b%29%0ABoolean%28a%29%0ABoolean%28b%29%0A_%20!%3D%3D%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20Boolean%28a%29%20!%3D%3D%20Boolean%28b%29%3B%0A%0Aconst%20val_1%20%3D%20%3B%0Aconst%20step_1%20%3D%20%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20%3B%0Aconst%20step_2%20%3D%20%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20%3B%0Aconst%20step_3%20%3D%20%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B%20&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
 /* values to try
  "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
*/
const a = 1, b = 0;

const expected = Boolean(a) !== Boolean(b);

const val_1 = String(a) !== String(b);
const step_1 = val_1;
console.assert(step_1 === expected, "step_1");

const val_2 = a < b;
const step_2 = val_2 !== val_1;
console.assert(step_2 === expected, "step_2");

const val_3 = Number(a) === 1;
const step_3 = val_3;
console.assert(step_3 === expected, "step_3");
}
```

## types & casting 3


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=Boolean%28b%29%20%3D%3D%3D%20Boolean%28Number%28a%29%29%0ABoolean%28b%29%0ANumber%28a%29%0ABoolean%28_%29%0A_%20%3D%3D%3D%20_)   
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20Boolean%28b%29%20%3D%3D%3D%20Boolean%28Number%28a%29%29%3B%0A%0Aconst%20val_1%20%3D%20%3B%0Aconst%20step_1%20%3D%20%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20%3B%0Aconst%20step_2%20%3D%20%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20%3B%0Aconst%20step_3%20%3D%20%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B%0A%0Aconst%20val_4%20%3D%20%3B%0Aconst%20step_4%20%3D%20%3B%0Aconsole.assert%28step_4%20%3D%3D%3D%20expected,%20%22step_4%22%29%3B&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = 1, b = 0;

const expected = Boolean(b) === Boolean(Number(a));

const val_1 = Boolean(a) && Boolean(b);
const step_1 = val_1;
console.assert(step_1 === expected, "step_1");

const val_2 = a < Number(a);
const step_2 = val_2 > 1;
console.assert(step_2 === expected, "step_2");

const val_3 = b > a;
const step_3 = val_3 !== val_1;
console.assert(step_3 === expected, "step_3");

const val_4 = String(b);
const step_4 = val_4 > Boolean(a);
console.assert(step_4 === expected, "step_4");
}
```

[TOP](#operator-precedence)

---

## Logical Operators

### logical operators 1


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=!%28a%20%26%26%20!b%29%0A!_%0A_%20%26%26%20_%0A!%28_%29%0A%0A)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20!%28a%20%26%26%20!b%29%3B%0A%0Aconst%20val_1%20%3D%20%3B%0Aconst%20step_1%20%3D%20%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20%3B%0Aconst%20step_2%20%3D%20%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20%3B%0Aconst%20step_3%20%3D%20%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B%20&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
 /* values to try
  "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
*/
const a = true, b = false;

const expected = !(a && !b);

const val_1 = Boolean(a);
const step_1 = val_1 && b;
console.assert(step_1 === expected, "step_1");

const val_2 = a && b;
const step_2 = val_2;
console.assert(step_2 === expected, "step_2");

const val_3 = a || b;
const step_3 = val_3 === val_2;
console.assert(step_3 === expected, "step_3");
}
```

### logical operators 2


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=!!a%20%7C%7C%20!!b%0A!a%0A!_%0A!b%0A!_%0A_%20%7C%7C%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20!!a%20%7C%7C%20!!b%3B%0A%0Aconst%20val_1%20%3D%20%3B%0Aconst%20step_1%20%3D%20%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20%3B%0Aconst%20step_2%20%3D%20%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20%3B%0Aconst%20step_3%20%3D%20%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B%20%0A%0Aconst%20val_4%20%3D%20%3B%0Aconst%20step_4%20%3D%20%3B%0Aconsole.assert%28step_4%20%3D%3D%3D%20expected,%20%22step_4%22%29%3B%0A%0Aconst%20val_5%20%3D%20%3B%0Aconst%20step_5%20%3D%20%3B%0Aconsole.assert%28step_5%20%3D%3D%3D%20expected,%20%22step_5%22%29%3B%20&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
 /* values to try
  "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
*/
const a = 0, b = false;

const expected = !!a || !!b;

const val_1 = a || b;
const step_1 = val_1 === 0;
console.assert(step_1 === expected, "step_1");

const val_2 = a && b;
const step_2 = val_2 > val_1;
console.assert(step_2 === expected, "step_2");

const val_3 = Number(a) < 1;
const step_3 = !val_3;
console.assert(step_3 === expected, "step_3"); 

const val_4 = Boolean(b) === true;
const step_4 = val_4 !== step_3;
console.assert(step_4 === expected, "step_4");

const val_5 = String(b) === Boolean(b);
const step_5 = val_5;
console.assert(step_5 === expected, "step_5");
}
```

### logical operators 3


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=a%20%7C%7C%20b%20%26%26%20c%20%7C%7C%20a%0A_%20%26%26%20_%0Aa%20%7C%7C%20_%0A_%20%7C%7C%20a)   
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20a%20%7C%7C%20b%20%26%26%20c%20%7C%7C%20a%3B%0A%0A//%20break%20down%20this%20expression&cumulative=false&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = , b = , c = ;

  const expected = a || b && c || a;

  // break down this expression
  const val_1 = a || b;
const val_2 = a && c;
const step_1 = val_1 && val_2;
console.assert(step_1 === expected, "step_1");
}
```
[ast explorer](https://astexplorer.net/#/gist/bc0bac0e8559bf97071c9129a05a28f9/e5fcaa5df8317fb1a45ba1a7866733d96768c463)


[TOP](#operator-precedence)

---

## Arithmetic Operators

### arithmetic operators 1


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=-%28a%20%2B%20b%29%20*%20c%0A_%20%2B%20_%0A-%28_%29%0A_%20*%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%200,%201,%20-1,%20NaN,%20Infinity,%20.5,%20-0.0,%201e3,%201e-3,%20999e305,%20999e306%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20-%28a%20%2B%20b%29%20*%20c%3B%0A%0Aconst%20val_1%20%3D%20%3B%0Aconst%20step_1%20%3D%20%3B%0Aconsole.assert%28step_1%20%3D%3D%3D%20expected,%20%22step_1%22%29%3B%0A%0Aconst%20val_2%20%3D%20%3B%0Aconst%20step_2%20%3D%20%3B%0Aconsole.assert%28step_2%20%3D%3D%3D%20expected,%20%22step_2%22%29%3B%0A%0Aconst%20val_3%20%3D%20%3B%0Aconst%20step_3%20%3D%20%3B%0Aconsole.assert%28step_3%20%3D%3D%3D%20expected,%20%22step_3%22%29%3B%20&cumulative=false&curInstr=10&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
/* values to try
  0, 1, -1, NaN, Infinity, .5, -0.0, 1e3, 1e-3, 999e305, 999e306
*/
const a = 1e-3, b = .5, c = 0;

const expected = -(a + b) * c;

const val_1 = a * c;
const step_1 = val_1;
console.assert(step_1 === expected, "step_1");

const val_2 = c / (a + b);
const step_2 = val_2;
console.assert(step_2 === expected, "step_2");

const val_3 = c;
const step_3 = val_3;
console.assert(step_3 === expected, "step_3");
}
```
[scientific notation](http://www.java2s.com/Tutorials/Javascript/Javascript_Tutorial/Data_Type/How_to_write_Scientific_notation_literal_in_Javascript.htm)

### arithmetic operators 2


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=a%20**%20b%20%2F%20%2Bc%0A%2B_%0A_%20**%20_%0A_%20%2F%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%200,%201,%20-1,%20NaN,%20Infinity,%20.5,%20-0.0,%201e3,%201e-3,%20999e305,%20999e306%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20a%20**%20b%20/%20%2Bc%3B%0A%0A//%20break%20down%20this%20expression%20&cumulative=false&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
  /* values to try
    0, 1, -1, NaN, Infinity, .5, -0.0, 1e3, 1e-3, 999e305, 999e306
  */
  const a = , b = , c = ;

  const expected = a ** b / +c;

  // break down this expression 
  const val_1 = a * b;
const val_2 = val_1 / +c;
console.assert(val_2 === expected);
}
```

### arithmetic operators 3


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=b%20%25%20c%20-%20a%20**%20c%20%2F%20b%0A_%20**%20_%0A_%20%2F%20_%0A_%20%25%20_%0A_%20-%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%200,%201,%20-1,%20NaN,%20Infinity,%20.5,%20-0.0,%201e3,%201e-3,%20999e305,%20999e306%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20,%20c%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20b%20%25%20c%20-%20a%20**%20c%20/%20b%3B%0A%0A//%20break%20down%20this%20expression&cumulative=false&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
  /* values to try
    0, 1, -1, NaN, Infinity, .5, -0.0, 1e3, 1e-3, 999e305, 999e306
  */
  const a = , b = , c = ;

  const expected = b % c - a * c / b;

  // break down this expression
  const val_1 = a * c;
const val_2 = val_1 / b;
const val_3 = b % c;
const val_4 = val_3 - val_2;
console.assert(val_4 === expected);
}
```

[TOP](#operator-precedence)

---

## All Primitive Operators

### all primitive operators 1


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=a%20%25%20b%20%7C%7C%20!!a%0A_%20%25%20_%0A!a%0A!_%0A_%20%7C%7C%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%200,%201,%20-1,%20NaN,%20Infinity,%20.5,%20-0.0,%201e3,%201e-3,%20999e305,%20999e306%0A%20%200,%203%0A%20%201,%203%0A%20%202,%203%0A%20%203,%203%0A%20%204,%203%0A*/%0Aconst%20a%20%3D%20,%20b%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20a%20%25%20b%20%7C%7C%20!!a%3B%0A%0A//%20break%20down%20this%20expression&cumulative=false&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
  /* values to try
    0, 1, -1, NaN, Infinity, .5, -0.0, 1e3, 1e-3, 999e305, 999e306
    0, 3
    1, 3
    2, 3
    3, 3
    4, 3
  */
  const a = 1, b = .5;

const expected = a % b || !!a;

// break down this expression
const val_1 = Boolean(b) || Number (a);
const val_2 = Boolean(val_1 && a);
console.assert(val_2 === expected);n
}
```

### all primitive operators 2


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=typeof%20a%20%3D%3D%3D%20'number'%20%2B%20a%0Atypeof%20_%0A_%20%3D%3D%3D%20_%0A_%20%2B%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%200,%201,%20-1,%20NaN,%20Infinity,%20.5,%20-0.0,%201e3,%201e-3,%20999e305,%20999e306%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20typeof%20a%20%3D%3D%3D%20'number'%20%2B%20a%3B%0A%0A//%20break%20down%20this%20expression&cumulative=false&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
  /* values to try
    0, 1, -1, NaN, Infinity, .5, -0.0, 1e3, 1e-3, 999e305, 999e306
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = 0;

const expected = typeof a === 'number' + a;

// break down this expression
const step_1 = typeof a;
const step_2 = 'number' + a;
const step_3 = step_2 === step_1;
console.assert(step_3 === expected);
}
```

### all primitive operators 3


[parsonized](https://janke-learning.github.io/parsonizer/?snippet=!!%2Ba%20%3D%3D%3D%20Boolean%28a%29%0A%2B_%0A!_%0A!_%0ABoolean%28_%29%0A_%20%3D%3D%3D%20_)  
[on pytut](http://www.pythontutor.com/live.html#code=/*%20values%20to%20try%0A%20%20%22%22,%20%22%20%22,%20true,%20false,%20undefined,%20null,%200,%201,%20-1,%20NaN,%20Infinity%0A*/%0Aconst%20a%20%3D%20%3B%0A%0Aconst%20expected%20%3D%20!!%2Ba%20%3D%3D%3D%20Boolean%28a%29%3B%0A%0A//%20break%20down%20this%20expression&cumulative=false&heapPrimitives=nevernest&mode=display&origin=opt-live.js&py=js&rawInputLstJSON=%5B%5D&textReferences=false)  
```js
{
  /* values to try
    "", " ", true, false, undefined, null, 0, 1, -1, NaN, Infinity
  */
  const a = true;

  const expected = !!+a === Boolean(a);

  // break down this expression
  const step_1 = !!+a;
const step_2 = step_1 === Boolean(a);
console.assert(step_2 === expected);
}
```


[TOP](#operator-precedence)

---

## Resources

* [operator precedence: mdn](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)
* [operator precedence: scripting master](http://www.scriptingmaster.com/javascript/operator-precedence.asp)
* [operator precedence: dummies](https://www.dummies.com/web-design-development/javascript-operator-precedence/)
* [ast visualizer](https://astexplorer.net/) 
    * explore how JS parses your code and represents operator precedence
    * select to hide everything just above the collapsible tree, makes it readable
    * this tool will be very helpful figuring out order of operations when expanding expressions
        * the deepest operators are executed first, then their parents, ...
    * using this for anything but just expressions will likely be more confusing than helpful
    * this tool doesn't check for syntax errors and doesn't run code, so keep it simple and just copy in the expression. no need for variable declarations


___
___
### <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>
