---
layout: post
title: "coding update"
date: 2017-12-08 21:54:00
categories: coding
---
I finally figured out the code I pasted into my previous post "new coding platform." When I posted it earlier it still wasn't working. I've got it going now, and here it is.

```javascript
const menu = {
_courses: {
_appetizers: [],
_mains: [],
_desserts: [],

get appetizers() {
 	return this._appetizers;
  },
set appetizers(appetizer) {
  this._appetizers.push(appetizer);
	},
get mains() {
	return this._mains;
	},
set mains(main) {
  this._mains.push(main);
	},
get desserts() {
	return this._desserts;
	},
set desserts(dessert) {
  this._desserts.push(dessert);
	},

},

get courses() {
return {
appetizers: this._courses.appetizer,
mains: this._courses.main,
desserts: this._courses.dessert
};
},

addDishToCourse(courseName, dishName, dishPrice) {
const dish = {
	name: dishName,
  price: dishPrice
};

this._courses[courseName].push(dish);

},

getRandomDishFromCourse(courseName) {
	const dishes = this._courses[courseName];
	const randomIndex = Math.floor(Math.random() * dishes.length);
  return dishes [randomIndex];
},

generateRandomMeal: function() {
  const appetizer = this.getRandomDishFromCourse('appetizers');
  const main = this.getRandomDishFromCourse('mains');
  const dessert = this.getRandomDishFromCourse('desserts');
  const totalPrice = appetizer.price + main.price + dessert.price;
return `Your meal is ${appetizer.name}, ${main.name}, and ${dessert.name}. The total price is $${totalPrice.toFixed(2)}.`;
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
