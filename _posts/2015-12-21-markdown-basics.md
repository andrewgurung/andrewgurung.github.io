---
layout: post
title: Markdown basics
comments: true
---

Note: ***Markdown allows you to write using an easy-to-read, easy-to-write plain text format, then convert it to structurally valid XHTML***

### 1. Multiple lines [Code Snippet]###

Enclose codes within triple backticks \` \` \`

Snippet:

```
` ` `
console.log("Markdown Basics");
` ` `
```

Result:

```
console.log("Markdown Basics");
```

##Language specific markdown code blocks: Javascript <br/>##
Syntax: Enclose codes within triple backticks \` \` \`js

Snippet:

```
` ` `js
var bar = 'Bar';
var foo = {b: bar};
` ` `
```

Result:

```js
var bar = 'Bar';
var foo = {b: bar};
```

### 2. Headings###

Snippet:

```
# Main Heading#
## SubHeading First##
### SubHeading Second###
```

Result:

# Main Heading#
## SubHeading First##
### SubHeading Second###

### 3. Quote###

Use > to start a quote

Snippet:

```
>Random Quote: Any application that can be written in JavaScript, will eventually be written in JavaScript - Jeff Atwood
```

Result:
>Random Quote: Any application that can be written in JavaScript, will eventually be written in JavaScript - Jeff Atwood


### 4. Nested Lists###

Unordered List: * or a -
Ordered List: Numbers

Snippet:

```
1. Item 1
	1. A corollary to the above item.
	2. Yet another point to consider.
2. Item 2
	* A corollary that does not need to be ordered.
  * This is indented four spaces, because it's two spaces further than the item above.
  * You might want to consider making a new list.
3. Item 3
```

Result:

1. Item 1
	1. A corollary to the above item.
	2. Yet another point to consider.
2. Item 2
	* A corollary that does not need to be ordered.
  * This is indented four spaces, because it's two spaces further than the item above.
  * You might want to consider making a new list.
3. Item 3

### 5. Links###
Syntax: \[Title](URL)

Snippet:

```
[Visit My GitHub!](https://www.github.com/andrewgurung)
```

Result:

[Visit My GitHub!](https://www.github.com/andrewgurung)
