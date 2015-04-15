---
layout: post
title:  "Test Driven Development"
date:   2015-04-15
categories: programming testing
---

<strong>TDD</strong> stands for <strong>test-driven-development</strong> and it is one of the words that a junior developer will hear very often. If you are like me, then you have no idea what TDD is. You're told that it is a good approach to creating and maintaining clean, extendable code. That's right, but you have now idea why. Why would you have to test code that is working? Wouldn’t you just see an error if the code was not working?

No! You don’t test whether the syntax of your code is correct - <strong>you test if the LOGIC of your code is correct</strong>. 

<h2>Unit tests</h2>

Why are unit tests called unit tests? Because you test a unit of code - very often (not always) that is a method that takes an input and gives a single output.

Say you have a function that sums up two given numbers. What you test is IF you pass 2 and 7 into your function, you are ASSERTING that the outcome is equal to 9. This is essential to understanding unit tests - <strong>you check if a given INPUT produces the expected OUTPUT</strong>.

![Unit test diagram](/assets/unit-test.png)

