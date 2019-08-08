---
layout: post
title: "code testing"
date: 2019-08-08 09:12:00
categories: coding python
---

I've been working for a while now on the CS50w course, [Web Development with Python and JavaScript](https://courses.edx.org/courses/course-v1:HarvardX+CS50W+Web/course/). I am now working on the topic of testing and Continuous Integration (CI)/Continuous Delivery (CD). Let me just break this stuff down a bit before it flies out of my head.

* **Class Notes**: Before I forget, here is a link to the [class notes](https://cs50.harvard.edu/web/2019/spring/notes/8/). These notes are essential.
* **Testing**: For general testing with Python, best to use `unittest` or `pytest`. Write as many tests as one can think of in a single testing file or in numerous files and/or folders - apparently there cannot be too many tests.
* **CI**: For automated CI we are learning to use [TravisCI](https://travis-ci.org), a web service that works with GitHub to run testing every time a particular code-base is pushed to its repository. For a Wikipedia article on CI, check [here](https://en.wikipedia.org/wiki/Continuous_integration).
* **CD**: TravisCI can also be used to automatically deploy code if the tests pass. This is the real Continuous Delivery. For a Wikipedia article on CD, check [here](https://en.wikipedia.org/wiki/Continuous_delivery).
* **Headless Testing**: This is a type of browser testing that does not include the graphical interface of an ordinary browser - so, headless browser testing. For this I can use [Selenium](https://www.seleniumhq.org/) as a way to automate the testing. I'm not sure yet if Selenium tests can be automated using TravisCI, but I'll look into it.
* **Docker**: [Docker](https://www.docker.com/) is an alternative to creating an app in a virtual machine. I don't yet understand the way it is supposed to work, but it looks as if it may be interesting.

I have to say that I am a little lost in all of this. I understand the syntax of how to write tests, but I'm a little lost on the process of deciding what to test in the first place. I suppose it is a matter of experience. Probably I should start by making sure that my final project for this course has a full testing suite and a connection to TravisCI. In fact, that's what I should be working on right now.

Let me get back to working on my final project.

#### This post is just over 370 words.
