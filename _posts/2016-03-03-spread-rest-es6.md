---
layout: post
title: Spread / Rest in ES6
comments: true
---

- The new ES6 `...` operator is referred as `spread` or `rest` operator depending on where/how it's used
- Solid alternative to deprecated so called `arguments` array

### Syntax
1. Function call

```js
foo(...[1,2,3]);
```

2. Array Literal  

```js
var b = [ 1, ...a, 5 ];
```

3. Function parameters

```js
function foo(x, y, ...z) { /* .. */ }
```

### Spread
- Used infront of an array to spread/expand out into its individual values

#### Examples

```js
function foo(x, y, z) {
  console.log( x, y, z );
}

// 1. Spread out individual values
foo(...[1,2,3]); // 1 2 3

// 2. Pre-ES6 syntax
foo.apply( null, [1,2,3] ); // 1 2 3

// 3. Spread out individual values
var a = [2,3,4];
var b = [ 1, ...a, 5 ];
console.log( b ); // 1,2,3,4,5
```

### Rest
- Collecting the rest of the parameters into an array

#### Examples

```js
// Gather rest of the arguments to `z` variable as an array
function foo(x, y, ...z) {
  console.log( x, y, z );
}

foo( 1, 2, 3, 4, 5 ); // 1 2 [3,4,5]
```
