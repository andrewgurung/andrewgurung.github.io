---
layout: post
title: Equality in Javascript == Vs ===
comments: true
---

There are two ways of comparing equality in Javascript.

1. Lenient equality operator: "==" checks for value equality
2. Strict equality operator:  "===" checks for both value and type equality

```js
var a = "42";
var b = Number( a ); // Explicit coercion
console.log(a == b);  // true
console.log(a === b); // false
```

## Best Practice: Whether to use == or ===

1. If either value (aka side) in a comparison could be true, false, 0, "", []
    use ===
2. Else it is safe to use ==
