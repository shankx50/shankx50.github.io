---
layout: post
title:  "Test Driven Development"
date:   2015-04-19
categories: programming testing
---

<strong>TDD</strong> stands for <strong>test-driven-development</strong> and it is one of the words that a junior developer will hear very often. If you are like me, then you have no idea what TDD is. You're told that it is a good approach to creating and maintaining clean, extendable code. That's right, but you have now idea why. Why would you have to test code that is working? Wouldn’t you just see an error if the code was not working?

No! You don’t test whether the syntax of your code is correct - <strong>you test if the LOGIC of your code is correct</strong>.

This means that in a way, writing tests is a lot easier than writing functional code. You don't have to write code that solves a problem - all you do is check whether existing code actually solves a given problem or not. This requires a shift of perspectives and is the main reason why new coders have trouble understanding testing.<strong> We are taught programming by writing solutions, not by writing tests around existing solutions.</strong>

TDD reverses the situation. In real TDD the coder writes the **test first** - then they try to write a solution that makes the test pass. There is a very important advantage in doing so. While working through the problem solving process, the coder doesn't just focus on the programming langue. There is a more **creativity-friendly environment** in his mind that allows for good solutions to come forth. It is not so easy to explain what I mean by that, but I think watching this <a href="http://www.pluralsight.com/courses/play-by-play-jim-weirich" target="_blank">set of videos</a> will help you understand. Pay attention to how <a href="http://en.wikipedia.org/wiki/Jim_Weirich" target="_blank">Jim Weirich</a> approaches solving the problem given to him.

<h2>Unit tests</h2>

Why are unit tests called unit tests? Because you test a unit of code - very often (not always) that is a method that takes an input and gives a single output.

Say you have a function that sums up two given numbers. What you test is IF you pass 2 and 7 into your function, you are ASSERTING that the outcome is equal to 9. This is essential to understanding unit tests - <strong>you check if a given INPUT produces the expected OUTPUT</strong>.

![Unit test diagram](/assets/unit-test.png)
