## Exercise 1

```js
function sentence(param_1) {
  var word_1 = param_1("t","e","a");
  var word_2 = param_1("e","a","t");
  var word_3 = param_1("a","t","e");
 return word_1 + ' ' +  word_2 + ' ' +  word_3;
}

function first(_1, _2, _3) {
  return _2 + _3 + _1;
}

const result = sentence(first);

console.assert(result === 'eat ate tea', 'result === ' + result);
```
---

## Exercise 2

```js
function sentence(param_1, param_2, param_3) {
  var word_1 = param_1("t","e","a");
  var word_2 = param_2("t","e","a");
  var word_3 = param_3("t","a","e");
  return word_1 + "" + word_2 + "" + word_3;
}

function first(_1, _2, _3) {
  return _2 + _3 + _1 + ' ';
}
function second(_1, _2, _3) {
  return _3 + _1 + _2 + ' ';
}
function third(_1, _2, _3) {
  return _1 + _3 + _2;
}

const result = sentence(first, second, third);

console.assert(result === 'eat ate tea', 'result === ' + result);
```
---

## Exercise 3

```js
function sentence(param_1, param_2, param_3) {
  var word_1 = param_1('t', 'a', 'e');
  var word_2 = param_2('e', 't', 'a');
  var word_3 = param_3('a', 't', 'e');
  return word_1 +" "+ word_2 +" "+ word_3;
}

function first(_1, _2, _3) {
  return _3+_2+_1;
}
function second(_1, _2, _3) {
  return _3+_2+_1;
}
function third(_1, _2, _3) {
  return _2+_3+_1;
}

const result = sentence(first, second, third);

console.assert(result === 'eat ate tea', 'result === ' + result);
```
---
## Exercise 4

```js
function sentence(param_1, param_2, param_3) {
  var word_1 = param_1('t', 'a', 'e');
  var word_2 = param_2('e', 't', 'a');
  var word_3 = param_3('a', 't', 'e');
  return word_1 +" "+ word_2 + " "+word_3;
}

function first(_1, _2, _3) {
  return _2 + _3 + _1;
}
function second(_1, _2, _3) {
  return _3 + _2 + _1;
}
function third(_1, _2, _3) {
  return _3 + _2 + _1;
}

const result = sentence(third, second, first);

console.assert(result === 'eat ate tea', 'result === ' + result);
```
---
