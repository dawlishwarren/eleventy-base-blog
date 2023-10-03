---
title: Programming Concepts
description: This is a post on my blog about programming concepts
date: 2023-10-03
tags:
  - javascript
---

Let's use common programming concepts in JavaScript to create a tip calculator.

### Variables

Using variables (a container for information), we can pass data into functions and return the result we want.
In this case the variables we need to know are the bill amount, and the percentage that we want to tip.

In this case we can get these values by prompting the user and using whatever they pass to us.

```js
// bill amount
const preTipTotal = parseFloat(document.getElementById("pre-tip").value);
// tip percentage
const tipPercentage = parseFloat(
	document.getElementById("tip-percentage").value.replace("%", "")
);
```

### Validation

We also want to check that the value of our variable is of the right type. Types are categories of data, such as 'string', 'number', 'boolean' or 'array'.

```js
  const errors = document.getElementById("errors");
  if (Number.isNaN(preTipTotal)) {
    errors.innerHTML = "Check meal amount is a valid number";
    setTimeout(() => {
      errors.innerHTML = "";
    }, 2000);
  } else if (Number.isNaN(tipPercentage)) {
    errors.innerHTML = "Check percentage is a valid number";
    setTimeout(() => {
      errors.innerHTML = "";
    }, 2000);
```

### Functions

Finally, if our data is what we are expecting, we can use javascript to compute the result we want:

```js
    // If good data, calculate tip
  } else {
    // 'tip' operates on the variables we established earlier
    const tip = (preTipTotal * tipPercentage) / 100;
    // 'total' adds the values together and returns a consistent value fixed to 2 decimal places
    const total = (preTipTotal + tip).toFixed(2);
    document.getElementById("total-bill").innerHTML = total;
    document.getElementById('tip-readout').innerHTML = `Meaning your tip is worth ${tip.toFixed(2)}`
  }
});
```
