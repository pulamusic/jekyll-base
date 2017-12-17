---
layout: post
title: "new coding platform"
date: 2017-12-08 14:55:00
categories: coding
---
I'm trying out a new coding platform: [repl.it](https://repl.it/repls). This seems like it will be a simpler way to test out JavaScript and other languages as I write with them. I have embedded a short example below to see if it will work. Let me just post this as is and then write more later.

<iframe height="400px" width="100%" src="https://repl.it/@jgCarroll/reversePara?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals" width="100%" ></iframe>

And now it is later...well, ten minutes later. The embed worked really well, so now I feel like I can write a full post. **Repl.it** seems like it will be a useful resource. In addition to JavaScript, I can use it to test out Ruby, HTML, CSS, Python, and a number of other languages. This is a much more useful way to test code rather than using a browser console. It will be interesting to see how it works with HTML and CSS.

I struggled quite a bit today with one of the [Codecademy projects](https://gist.github.com/e9261fe8dc16210c32c10d46e136c5d1), and I found repl.it when I asked for some help and the helper used repl.it to show me part of an answer. Below is the code I have been working on so far. Bear in mind that it still doesn't work.

```javascript
const menu = {
_courses: {
  _appetizers: [],
  _mains: [],
  _desserts: [],

  set appetizers(appetizerIn) {

  },

  get appetizers() {

  },

  set mains(mainIn) {

  },

  get mains() {

  },

  set desserts(dessertIn) {

  },

  get desserts() {

  }
},

get courses() {
  return {
    appetizers: this._courses.appetizers,
    mains: this._courses.mains,
    desserts: this._courses.desserts
  }
},

addDishToCourse(courseName, dishName, dishPrice) {
const dish = {

};

this._courses[courseName].push(dish);

},

getRandomDishFromCourse(courseName) {
  const dishes = this._courses[courseName];
  const randomIndex = Math.floor(Math.random() * dishes.length);
},

generateRandomMeal: function() {
const appetizer = this.getRandomDishFromCourse('appetizers');
const mains = this.getRandomDishFromCourse('mains');
const desserts = this.getRandomDishFromCourse('desserts');
const totalPrice = appetizer.price + mains.price + desserts.price;

return `Your meal is ${appetizer.name}, ${main.name}, ${dessert.name}. The price is $${totalPrice}.`

}

};

menu.addDishToCourse('appetizers', 'Caesar Salad', 4.25);
menu.addDishToCourse('appetizers', 'Chicken Fingers', 5.49);
menu.addDishToCourse('appetizers', 'Nachos', 4.99);
menu.addDishToCourse('appetizers', 'Chicken Wings', 5.99);

menu.addDishToCourse('mains', 'Steak Tips', 12.25);
menu.addDishToCourse('mains', 'Roasted Chicken', 10.99);
menu.addDishToCourse('mains', 'Shrimp Scampi', 13.99);
menu.addDishToCourse('mains', 'Blue Cheese Burger', 9.99);

menu.addDishToCourse('desserts', 'Red Velvet Cake', 4.99);
menu.addDishToCourse('desserts', 'Tiramisu', 3.99);
menu.addDishToCourse('desserts', 'Gelatto', 3.99);
menu.addDishToCourse('desserts', 'Irish Coffee', 4.99);

let meal = menu.generateRandomMeal();
console.log(meal);
```

The error message notes that there is a problem with the way I am using `.push()`, though I can't yet figure out what the problem is. I'll work on it by myself for a while longer before I ask for further help. Maybe at this point I can review some of the questions and answers people have posted online. I'm not in danger of just lifting the entire answer from someone else's work.

I'm going to write a bit more because I want to reach my 500 word minimum, but I don't have anything else to say at the moment. I need to be strict with myself every time I post on this blog because I'm striving to improve my writing. My writing only improves by doing it.

Reached my minimum. Of course, this also includes the code I pasted into this post, but I did write the code anyway.
