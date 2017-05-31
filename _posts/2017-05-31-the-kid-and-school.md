---
layout: post
title: "the kid and school"
date: 2017-05-31 12:17:00
categories: life coding
---

# why won't she go?

So the kid refused to go to school this morning. Essentially, the principal yelled at her yesterday for not wearing a proper uniform. Zanaya got angry, yelled back, and left the school. Now she thinks she can just not go to school. Valerie now wants to move Zanaya to another program so she can get her GED, and I put my foot down. We have moved this kid to different schools so often she has not been able to establish a community of friends other than the few she has picked up here and there. If Zanaya totally refuses to go to school then we are really fucked. I refuse to move her again. I'm putting my foot down, and this little girl is going to listen.

This has got me upset now. I need to force myself to write about something else.

I came across a strange blog post yesterday. This woman had done the entire Free Code Camp front end certification without understanding how to construct a simple HTML page separate from CodePen. She felt the need, in this post, to point out that Bootstrap is a CSS framework, and that jQuery is a subset of JavaScript. How the hell does somebody get so far along with a program without understanding what I consider to be some of the very basics of coding? Really, it was quite a weird post. Stranger still, there were a number of comments on the post thanking the author for her clarification.

Do people really not pay attention to the fundamentals? One of the things that holds me up is the fact that I focus on fundamentals, but at least I have a solid foundation. Having this foundation makes me confident that when JavaScript finally clicks for me it will really click. It's the algorithmic logic of JavaScript that trips me up, making it impossible for me to write anything other than very basic code. One thing I have learned along the way, though, is that almost any question I have about JavaScript has already been answered by someone on the internet. I have a feeling that, for me, this is the way to learn - learn by doing, and the understanding will come.

Speaking of coding, one thing I haven't tried with Markdown is its ability to present code in a post. Let me try it out below using an example from one of my CodePens.

```var input = document.querySelector('.numberInput');
    var para = document.querySelector('#output');

function squared(num) {
  return num * num;
}

function cubed(num) {
  return num * num * num;
}

function factorial(num) {
  var x = num;
  while (x > 1) {
    num *= x-1;
    x--;
  }
  return num;
}

input.onchange = function() {
  var num = input.value;
  if (isNaN(num)) {
    para.textContent = 'You need to enter a number!';
  } else {
    para.textContent = num + ' squared is ' + squared(num) + '. ' +
                       num + ' cubed is ' + cubed(num) + '. ' +
                       num + ' factorial is ' + factorial(num) + '.';
  }
}```
