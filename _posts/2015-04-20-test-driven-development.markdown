---
layout: post
title:  "Test Driven Development"
date:   2015-04-20
categories: programming testing
permalink: /test-driven-development
---

<strong>TDD</strong> stands for <strong>test-driven-development</strong> and it is one of the words that a junior developer will hear very often. If you are like me, then you have no idea what TDD is. You're told that it is a good approach to creating and maintaining clean, extendable code. That's right, but you have now idea why. Why would you have to test code that is working? Wouldn’t you just see an error if the code was not working?

No! You don’t test whether the syntax of your code is correct - <strong>you test if the LOGIC of your code is correct</strong>.

This means that in a way, writing tests is a lot easier than writing functional code. You don't have to write code that solves a problem - all you do is check whether existing code actually solves a given problem or not. This requires a shift of perspectives and is the main reason why new coders have trouble understanding testing.<strong> We are taught programming by writing solutions, not by writing tests around existing solutions.</strong>

TDD reverses the situation. In real TDD the coder writes the **test first** - then they try to write a solution that makes the test pass. There is a very important advantage in doing so. While working through the problem solving process, the coder doesn't just focus on the programming langue. There is a more **creativity-friendly environment** in his mind that allows for good solutions to come forth. It is not so easy to explain what I mean by that, but I think watching this <a href="http://www.pluralsight.com/courses/play-by-play-jim-weirich" target="_blank">set of videos</a> will help you understand. Pay attention to how <a href="http://en.wikipedia.org/wiki/Jim_Weirich" target="_blank">Jim Weirich</a> approaches solving the problem given to him.

##Unit tests

Why are unit tests called unit tests? Because you test a unit of code - very often (not always) that is a method that takes an input and gives a single output.

Say you have a function that sums up two given numbers. What you test is IF you pass 2 and 7 into your function, you are ASSERTING that the outcome is equal to 9. This is essential to understanding unit tests - <strong>you check if a given INPUT produces the expected OUTPUT</strong>.

![Unit test diagram](/assets/unit-test.png)

Unit tests are the first line of defense for catching bugs, but sometimes issues come up with integration between components which can't be captured in a unit test. End-to-end tests are made to find these problems.

##End-to-end tests (E2E) according to <a href="http://www.techopedia.com/definition/7035/end-to-end-test" target="_blank">techopedia</a>

End-to-end testing involves ensuring that **integrated components of an application function as expected**. The entire application is tested in a real-world scenario such as communicating with the database, network, hardware and other applications.

For example, a simplified end-to-end testing of an email application might involve:

- Logging in to the application
- Accessing the inbox
- Opening and closing the mailbox
- Composing, forwarding or replying to email
- Logging out of the application

The simplest way of conducting E2E tests is by just opening a browser and trying the things that need testing. Hence E2E can be done **without writing code.** I imagine that beginner programmers unknowingly conduct a lot of E2E testing just because, as opposed to unit testing, is feels very natural and straightforward. Note that E2E testing is only possible when functioning units of codes exist (tested or not).

<script type="text/javascript"
  src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

So in a way one can say that unit tests $$\subset$$ E2E.

---

<span id="math">Did you see that? :) I was able to print out mathematical symbols. How cool is that?! Let's try something fancier.</span>

When $$a \ne 0$$, there are two solutions to $$(ax^2 + bx + c = 0)$$ and they are
$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$

In case you are interested, here is the markup.

    <script type="text/javascript"
      src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
    </script>

    When $$a \ne 0$$, there are two solutions to $$(ax^2 + bx + c = 0)$$ and they are
    $$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$

Learn more about MathJax <a href="http://docs.mathjax.org/en/latest/index.html" target="_blank">here</a>.

##More testing types found on <a href="http://en.wikipedia.org/wiki/Software_testing" target="_blank">wikipedia</a>

- Installation testing
- Compatibility testing
- Smoke and sanity testing
- Regression testing
- Acceptance testing
- Alpha testing
- Beta testing
- Functional vs non-functional testing
- Destructive testing
- Software performance testing
- Usability testing
- Accessibility testing
- Security testing
- Internationalization and localization
- Development testing
- A/B testing
- Concurrent testing
- Conformance testing or type testing
