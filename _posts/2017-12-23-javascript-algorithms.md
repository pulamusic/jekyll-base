---
layout: post
title: "JavaScript algorithms"
date: 2017-12-23 13:25:00
categories: coding
---

I have been re-working my way through the [FreeCodeCamp](https://www.freecodecamp.org) JavaScript algorithms, testing things out in [Repl.it](https://repl.it/repls) as I go. This is a much more satisfying time around since I am doing a lot more of the coding by myself. That being said, I have been looking at the answers on the FreeCodeCamp forum as well as StackOverload, but one thing I have learned about coding is that Google is my best friend - if I have a question, chances are someone else has had the same question. In fact, even if my question is extremely basic, I can search out the answer, and, more than likely, someone has answered it on StackOverload.

Anyway, let me share some of the code I have been writing, along with some basic explanation.

---

**Capitalize a String**: The following code takes a string and capitalizes every word. It seems like it should be simpler than it is, but the trick is to split the string into an array, loop through and capitalize each member of the array, and then re-join the array into a single string.

```JavaScript
function titleCase(str) {
  str = str.toLowerCase().split(" ");
  for (var i = 0; i < str.length; i++) {
    str[i] = str[i].charAt(0).toUpperCase() + str[i].slice(1);
  }
  return str.join(" ");
}

titleCase("go fuck a duck"); // outputs "Go Fuck A Duck"
```

---

**Reverse a Paragraph**: This code reverses a paragraph, leaving the words intact. This isn't really a FreeCodeCamp algorithm, but it is related. If I remove the spaces from the `.split(' ')` and the `.join(' ')` methods, the code will then reverse all letters of each word as well. Essentially, just by making two small changes I could turn a string into a palindrome.

```JavaScript
let words = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum porta diam tellus, accumsan euismod orci lobortis non. Quisque eget nisl gravida, sodales lectus eu, pretium neque. Phasellus suscipit suscipit est varius rutrum. Sed placerat, risus nec tempor vestibulum, dui libero efficitur purus, in dignissim turpis felis eu elit. In vel dictum libero. Vivamus ullamcorper condimentum risus in fermentum. Fusce massa quam, lacinia nec ipsum non, tempus luctus risus. Nullam aliquam justo leo, quis placerat eros porta sit amet.";

let wordsArray = words.split(' ');

let reverseWords = wordsArray.reverse();

let reversePara = reverseWords.join(' ');

console.log('ORIGINAL PARAGRAPH: ' + words);
console.log(' ');
console.log('PARAGRAPH IN REVERSE: ' + reversePara);
```

---

**Truncate a String**: This code takes in a string and a number, and then truncates the string to the specified number of characters. In the example below, it takes in a string and truncates it to 11 characters, including the `'...'` at the end of the truncation. If the string plus the ellipsis was less than 11 characters, the code would leave it unmolested.

```JavaScript
function truncateString(str, num) {
  if (str.length > num && num > 3) {
    return str.slice(0, (num - 3)) + '...';
  } else if (str.length > num && num <= 3) {
    return str.slice(0, num) + '...';
  } else {
    return str;
  }
}

truncateString("A-tisket a-tasket A green and yellow basket", 11); //outputs 'A-tisket...'
```

---

**Falsy Bouncer**: This is a very simple bit of code that removes any false values from an array. Nothing more complicated than that.

```JavaScript
function bouncer(arr) {
  var filteredArray = arr.filter(Boolean);
  return filteredArray;
}

bouncer([7, "ate", "", false, 9]); //outputs [7, "ate", 9]
//bouncer(["a", "b", "c"]);
//bouncer([false, null, 0, NaN, undefined, ""]);
//bouncer([1, null, NaN, 2, undefined]);
```
