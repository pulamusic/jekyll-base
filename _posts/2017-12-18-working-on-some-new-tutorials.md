---
layout: post
title: "working on some new tutorials"
date: 2017-12-18 14:29:00
categories: coding
---
I finally signed up for the [Pluralsight](https://app.pluralsight.com/library/) website so I can take some more coding tutorials. So far I have taken a few tutorials for JavaScript - some excellent and some not. I've also started a tutorial on HTML5, trying to learn a lot more of the functionality of this updated version.

As for JavaScript, I created a very basic zombie apocalypse game from the project for one of the tutorials. It's a lot of code, but I have included it at the bottom of this post. Let me write a bit more before I wind up this post. The code below is so long anything I write below it will be lost to me.

One thing I realize is that I need to stop every once in a while and create something with the code I am learning. This has been difficult with JavaScript, and much easier with HTML and CSS. Creating the game below really helped me to solidify a few JavaScript concepts. Next I need to write something that includes functions, objects, and classes.

Oh, wait, I did do something with classes that turned out pretty nice. Let me also paste that code into the bottom of this post. This code outputs bibliographic information to an HTML table (I won't include the HTML in this post, though). There is probably a simpler or more efficient way to accomplish what this code accomplishes, but this is where I am at the moment with my JavaScript skills.

This is a long post because of the code, so let me wrap it up for now. I'll probably want to write something more later.

---
**Zombie Apocalypse**
```JavaScript

const beginningScenarios = [
  'You wake up in a hospital after having been unconscious for several days. It is too quiet and there is nobody around. You look out the window and... holy shit, it\'s the zombie apocalypse!',

  'After days of hiding out in your basement, you finally go upstairs to see what is going on. When you peek out the window...the street is teeming with zombies!',

  'The radio announced two days ago that the zombie apocalypse has arrived. You have been traveling by night, hiding out in people\'s homes during the day, avoiding zombies as best you could.',

  'You are inside a church with the doors barricaded, trying desperately to keep the zombies out. Every now and then the zombies push a bit harder against the door and parts of the barricade need to be re-done.',

  'The zombie apocalypse arrived while you were on a sailboat at sea. You have enough provisions for a few more days, but eventually you will need to go ashore to get more food. You sail up and down the coast, looking for a safe place to land.'
]

// random number generator, used in several places throughout the game.
function randomNumber (range) {
  return Math.round(Math.random() * range)
}

window.alert(beginningScenarios[randomNumber(beginningScenarios.length - 1)])

const name = window.prompt('First of all, what do I call you?')

const weapon = window.prompt('Ok, ' + name + '. Being that it is the zombie apocalypse, you decide you need a weapon to defend yourself. You look around and see the following items: a shovel, a baseball bat, a crossbow, a rubber chicken, a can of hairspray, a gun, a machete, a nail file, a hammer, and a boomerang. Which do you choose, or did you find something else?')

window.alert('So, ' + name + ' you have grabbed a ' + weapon + ' to defend yourself. You attack.')

const survival1 = randomNumber(2)
const survival2 = randomNumber(2)
const survival3 = randomNumber(2)
const survival4 = randomNumber(2)
const survival5 = randomNumber(2)

// if/else if statements that lead the player through several paths.
if (survival1 === 0) {
  window.alert('The zombie bites you. You lose! And...')
  window.alert('...you have been turned into a zombie! You try to bite someone')
  if (survival2 === 0) {
    window.alert('Damn it, someone has killed you with a ' + weapon + '. End of the line for you.')
  } else if (survival2 > 0) {
    window.alert('Successful bite! Another zombie in this world.')
    window.alert('You have another human in your sights. You go in for the attack.')
    if (survival4 === 0) {
      window.alert('Someone has successfully killed you. No more zombie.')
    } else if (survival4 > 0) {
      window.alert('You are a successful zombie! Happy biting.')
    }
  }
} else if (survival1 > 0) {
  window.alert('You kill the zombie with your ' + weapon + '. You win! But...')
  window.alert('...a second wave of zombies is attacking! You look around again and grab your ' + weapon + ' and try to defend yourself.')
  if (survival3 === 0) {
    window.alert('This zombie has bitten you. You lose!')
  } else if (survival3 > 0) {
    window.alert('You lucky bastard, you killed another zombie!')
    window.alert('Here comes yet another zombie! Now you pick up your ' + weapon + ' and you try to kill it.')
    if (survival5 === 0) {
      window.alert('Finally, you have been bitten. You are a zombie! Time to bite.')
    } else if (survival5 > 0) {
      window.alert('You kill another one! You are getting good at this.')
    }
  }
}

```

---
**Bibliography**
```JavaScript

'use strict'

class Book {
  constructor (author, title, yearPublished) {
    this.author = author
    this.title = title
    this.yearPublished = yearPublished
  }
}

// instances of class Book
const book1 = new Book('Michel Foucault', 'The Order of Things', 1967)
const book2 = new Book('Jacques Derrida', 'Of Grammatology', 1971)
const book3 = new Book('Michel de Certeau', 'The Practice of Everyday Life', 1978)
const book4 = new Book('Paul Gilroy', 'The Black Atlantic', 1993)
const book5 = new Book('Henry Louis Gates', 'The Signifying Monkey', 1988)
const book6 = new Book('Frantz Fanon', 'The Wretched of the Earth', 1967)
const book7 = new Book('Mikhail Bakhtin', 'The Dialogic Imagination', 1975)
const book8 = new Book('Michel Foucault', 'The Archaeology of Knowledge', 1972)

// printed in HTML
document.getElementById('author1').innerHTML = book1.author
document.getElementById('title1').innerHTML = book1.title
document.getElementById('year1').innerHTML = book1.yearPublished

document.getElementById('author2').innerHTML = book2.author
document.getElementById('title2').innerHTML = book2.title
document.getElementById('year2').innerHTML = book2.yearPublished

document.getElementById('author3').innerHTML = book3.author
document.getElementById('title3').innerHTML = book3.title
document.getElementById('year3').innerHTML = book3.yearPublished

document.getElementById('author4').innerHTML = book4.author
document.getElementById('title4').innerHTML = book4.title
document.getElementById('year4').innerHTML = book4.yearPublished

document.getElementById('author5').innerHTML = book5.author
document.getElementById('title5').innerHTML = book5.title
document.getElementById('year5').innerHTML = book5.yearPublished

document.getElementById('author6').innerHTML = book6.author
document.getElementById('title6').innerHTML = book6.title
document.getElementById('year6').innerHTML = book6.yearPublished

document.getElementById('author7').innerHTML = book7.author
document.getElementById('title7').innerHTML = book7.title
document.getElementById('year7').innerHTML = book7.yearPublished

document.getElementById('author8').innerHTML = book8.author
document.getElementById('title8').innerHTML = book8.title
document.getElementById('year8').innerHTML = book8.yearPublished

```

---
