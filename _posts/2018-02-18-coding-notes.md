---
layout: post
title: "coding notes"
date: 2018-02-18 18:16:00
categories: coding
---

I thought I might as well blog this. These are notes for a Udemy course titled [Coding Interview Prep](https://www.udemy.com/javascript-interview-prep/learn/v4/content). The answers below are coded out on the Repl.it and Codepen websites. I have added hyperlinks to each of the code examples.

Also check out the following resources for practice algorithms: [JS: Interview Algorithm](https://thatjsdude.com/interview/js1.html); [Learning Algorithms in Javascript From Scratch](https://www.udemy.com/learning-algorithms-in-javascript-from-scratch/learn/v4/overview); [Coderbyte challenges](https://coderbyte.com/challenges); [Khan Academy JS interview questions](http://khan4019.github.io/front-end-Interview-Questions/sort.html); etc. Also check out [freeCodeCamp.org](https://www.freecodecamp.org) for a whole bunch of algorithm challenges.

1. [Triple Add Function](https://repl.it/@jgCarroll/tripleAddFunction): tripleAdd(10)(20)(30) // returns total of all 3 numbers added together
2. [What is and IIFE, and why are they used?](https://repl.it/@jgCarroll/exampleIIFE): Immediately invoked function expression. It declares a function and then calls it immediately. Used to take advantage of the local scope of variables inside the function. Example in Repl.it
3. [Source code guessing](https://codepen.io/pulamusic/pen/YeYvVp?editors=1010): Given some source code, guess what will happen when the various buttons are pushed.
4. [Closures](https://repl.it/@jgCarroll/closures): What is a closure? Code out an example of a closure. *My Answer*: a closure defines a function in a specific scope so that it explicitly has access to that scope. *Instructor's Answer*: A closure is an inner function that has access to the scope of an enclosed function.
5. ['This' keyword](https://repl.it/@jgCarroll/thisKeyword): What is the 'this' keyword in JavaScript, and how is it used? *My Answer*: The 'this' keyword relates to functions that are properties of objects.
6. [Hoisting](https://repl.it/@jgCarroll/hoisting): Describe what variable and function hoisting is and how it works. *Answer*: Variables and functions are hoisted to the top of the scope in which they are declared. Essentially, you can't call or log out a variable or function before it is defined. Also, bear in mind that `let` and `const` are block scoped, not function or global scoped.
7. [Scope and 'self' question](https://repl.it/@jgCarroll/scopeAndSelf): Look at the given code and guess at what is logged out to the console. *NOTE*: The code explains it all.
8. [== vs ===](https://repl.it/@jgCarroll/vs): What is the difference between `==` and `===`? *Answer*: `==` stands for 'equals' and tests for abstract equality (doesn't test for data type), whereas `===` stands for 'strict equals' and tests for strict equality (tests for data type).
9. [Log number function](https://repl.it/@jgCarroll/logNumberFunction): Look at the given source code and determine what will be logged to the console. *Answer*: It logs as undefined, probably because of the keyword `var` being used twice. The second `var` is function scoped, so `var num` is hoisted to the top of the function, but not defined until after the `console.log`.
10. [Use strict](https://repl.it/@jgCarroll/useStrict): What does `use strict` do to code, and what are the benefits of using it? *Answer*: Enforces stricter parsing and error handling in the code. It prevents the use of global variables; enforces that all function parameters must be unique; prevents deleting Object properties that are important. Essentially, `use strict` throws errors when we do bad stuff with our code, informing us early of errors that could throw off our code later.
11. [Curry function](https://repl.it/@jgCarroll/curryFunction): Given some starter code, curry the function. *Answer*: Function with multiple parameters should be re-written as multiple, embedded functions with one parameter each.
12. [Counter function](): Write a function that keeps track of how many times it was called and returns the number. *Answer in the code*.
13. [Logging X and Y](https://repl.it/@jgCarroll/loggingXAndY): Looking at the example code, what are the values of `X` and `Y` when they are logged out? *Answer is in the code example*.
14. [Call &amp; apply methods](https://repl.it/@jgCarroll/callAndApplyMethods): Describe the JavaScript `call()` and `apply()` methods. How do they function? What arguments do they take? How are they different? *Answers*: Both are predefined JavaScript methods. The `call()` method can be used to call a function with an object as an argument. The `apply()` method is similar, but it takes an array as an argument.
