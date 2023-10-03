---
title: Functions and Control Flow
description: A blog about functions
date: 2023-10-03
tags:
  - javascript
---

### Create, and Invoke

In JavaScript, and many other languages, functions are a fantastic tool.
The basic concept is simple: create the function by declaring it, with either of the below syntax:

```js
function() {
    //
}
```

or

```js
const function = () => {
    //
}
```

Once a function is declared it must be invoked/called to be read, to do so simply write the full function name with a pair of brackets, either empty or with any required arguments:

```js
function writeASentence() {
	document.write("Task 1: Hello world. ");
}
writeASentence();
```

### Arguments

Now we know how to build and call functions, we can add arguments/parameters to our function. These are variables that we 'pass' into the function to be used within the function body, e.g:

```js
function fullName(firstName, lastName) {
	document.write(`Task 2: ${firstName} ${lastName}. `);
}
fullName("Alex", "Warren");
```

### Returning values

The body of a function can be used to do a lot of things, but more often than not you will want to 'return' a value. This means that when you call the function, its value is equal to whatever is 'returned' in the body of the function. E.g:

```js
function updateFullName(firstName, lastName) {
	return `Task 3: ${firstName} ${lastName}`;
}
const fullNameFromFunction = updateFullName("Joe", "Bloggs. ");
document.write(fullNameFromFunction);
```

### Function bodies

Within the body of a function we can, and often do, perform complicated tasks and computations based on the arguments passed into the function. For example we can use a switch statement to determine precisely what to return given the value of the argument, e.g:

```js
const t = 40;

function dressForTheWeatherTwo(temp) {
	if (temp < 0) {
		return "Task 4.3: Stay inside!";
	} else if (temp < 30 || temp === 30) {
		return "Task 4.3: Wear a coat and a hat!";
	} else if (temp < 50 || temp === 50) {
		return "Task 4.3: Wear a coat!";
	} else {
		return "Task 4.3: just pants and vest is fine.";
	}
}
document.write(dressForTheWeatherTwo(t));
```
