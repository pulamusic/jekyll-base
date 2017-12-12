---
layout: post
title: "learning React"
date: 2017-12-12 14:50:00
categories: coding
---

I have been working since yesterday on the [first of the two React tutorials on Codecademy](https://www.codecademy.com/learn/react-101). So far it makes sense to me, although I don't yet know how to compile React code to create readable JavaScript. Here is an instance of uncompiled React code.

---
```JavaScript
import React from 'react';
import ReactDOM from 'react-dom';

class Button extends React.Component {
  scream() {
    alert('AAAAAAAAHHH!!!!!');
  }

  render() {
    return <button onClick={this.scream}>Scream</button>;
  }
}

ReactDOM.render(<Button />, document.getElementById('app'));
```
---

React is a JavaScript library, though as I stated before it needs to be compiled using the command line before it can be read by a browser. Essentially, it looks like JavaScript with elements of HTML code added to it. This is interesting to me since I have become frustrated with the tutorials' insistence on using only the console to output code from JavaScript. The React tutorial, so far, outputs to a browser, so I can see immediately how useful it is in working with HTML documents. With the long-ish [JavaScript tutorial](https://www.codecademy.com/learn/introduction-to-javascript) I was left wondering how I can practically use this code in creating web pages and apps. The React tutorial almost immediately addresses this concern of mine.

I'm beginning to get the sense, though, of how limited these tutorials can be in terms of making me a self-sufficient developer. This React tutorial is pretty skimpy, leaving me to wonder just how proficient I will be in writing React code when I am done with it. I suppose a next step will be to do the tutorials on the [React.org](https://reactjs.org/) website, which I can tell deals with compiling code almost immediately.

After having done the full Codecademy tutorials on JavaScript and React it may also be useful to go back to [FreeCodeCamp](https://www.freecodecamp.org/) in order to complete their curriculum. If I do that, I would like to re-do the algorithms and fix up the projects that I have supposedly already completed. I know the weather app I allegedly wrote (long story) is broken. Certainly, I didn't fully learn how to create JSON code. I now have a little more experience with it, so maybe I can be more actively involved in creating the apps.

I have been thinking lately about finally creating a web page for the New Africa House Ensemble, though we are basically disbanded at this point. I did purchase the url last year, so I may as well make use of it at some point. I would like to do a parallax scrolling single-page site with some slide toggle windows for some of the information, leaving a clean page full of images and sound files. I would like the large background images to show off some of the musicians whose music we play and/or admire, maybe creating a few collages of images. I would like there to be a photo gallery and a gallery for sound files. At the top of the page there should be a scrollspy menu so that people can jump to different portions of the page. There should be a list of all the musicians who performed with the band with perhaps modals that pop out and give some sort of biographical information.

Ah, who knows. This group is essentially defunct at the moment. It would be nice to resurrect it, though.
