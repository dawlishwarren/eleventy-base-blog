---
title: Pseudocode & Comments
description: A blog on how to effectively utilise comments when coding.
date: 2023-10-03
tags:
  - comments
  - pseudocode
---

### Problem

In programming as in life, it's all about solving problems. Regardless of the task you will always get to the result quicker when you can best identify the problem. Let's say we want to track which books we have and haven't read yet. Sounds simple, but what are the constituent parts of that problem?

### Solution

- Books. What information do we need to know?

  - We need to know the book's name, the author might be helpful, whether it's been read or not. This is starting to sound like something an object can store as key/value pairs.
  - We need to be able to store lots of these books, in a way in which we can access them easily. Given that we can assume they will be of a consistent shape we can confidently use an array to store this data.

- Now we have worked out how to build out and store our data. What do we need to do to it?

  - The problem requires us to be able to look at each book and see whether or not we've read it.
  - In short, we need to access the 'read' property of each book object and do something based on the result.
  - Iteration seems like the easiest way to do this. We can loop over our 'books' array and access the 'read' property of each iteration.

- Let's return something.
  - Cool, we have our books, we know we can easily pass judgement on them, what are we trying to achieve?
  - To accurately track what we've read we should return a statement based on the 'read' value.
  - Given 'read' can be a yes/no, a boolean value is the most appropriate for this variable.
  - With boolean values come a host of functions and methods we can use, such as switch statements or IF/ELSE blocks.
  - Let's say IF it hasn't been read, we return one string, and ELSE IF it has we return a different one.

```js
// --- Solution
// 1. Create array of objects
// booksArray = [{title, author, alreadyRead}, {...}, {...}]
// E.g [{'The Hobbit', 'J.R.R. Tolkien', alreadyRead: true}]
// 2. Iterate through the array of books. JavaScript array.map function would be useful with an array of objects
// 3. In the iteration function body we can test the book.alreadyRead value, and return a string depending on the value.
```

### Code

Finally, now we have broken the problem down into its smallest parts, the coding process becomes almost automatic.
Critically analysing the problem allows you to simply describe what each code chunk needs to achieve and helps keep it organised.

```js
// 1. Create array of objects
const booksArray = [
	{ title: "The Hobbit", author: "J.R.R. Tolkien", alreadyRead: true },
	{ title: "Frankenstein", author: "Mary Shelley", alreadyRead: false },
	{ title: "The Phoenix Project", author: "Gene Kim", alreadyRead: true },
];
// 2. Iterate through the array of books. JavaScript array.map function would be useful with an array of objects
booksArray.map((book) => {
	// 3. In the iteration function body we can test the book.alreadyRead value, and return a string depending on the value.
	if (book.alreadyRead) {
		console.log(`You have already read ${book.title} by ${book.author}.`);
	}
	if (!book.alreadyRead) {
		console.log(`You still need to read ${book.title} by ${book.author}.`);
	}
});
```
