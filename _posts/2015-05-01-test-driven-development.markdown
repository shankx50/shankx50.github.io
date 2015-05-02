---
layout: post
title:  "Test Driven Development"
date:   2015-05-01
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

<h3 id="mocking">Please, mock me!</h3>

As so often in programming, it helps understanding concepts by first looking at their literal meaning. ***Mocking and unit testing go hand in hand.*** Simple unit testing may rely on a function alone, but you will see that you will quickly have to mock dependencies. ***So what is mocking?*** The dictionary says : <q>...arranged for training or practice, or performed as a demonstration...</q> We arrange, orchestrate, or mimic situations in which we want our code to behave in a certain way. We are fooling the code to believe that it lives in a certain environment.

Let's look at a very practical example. You may have a block of code that takes a list and sorts it in alphabetical order. Sorting the list correctly is the logic you want to test. Now you need to get that list from somewhere. You could just hard-code it in your test - and that's fine depending on what your test needs to achieve. However, it is very likely that your function gets the list from an external resource. Say you want a list of 10 names, then you could call this <a href="http://www.filltext.com/?rows=10&fname={firstName}&lname={lastName}&pretty=true" target="_blank">external resource</a>. If you just clicked on the link, you saw that the friendly people of <a href="http://www.filltext.com" target="_blank">www.FillText.com</a> provide this free service for development needs.

Can we use this service to arrange our test then? We could, but it is ***good practice*** to have ***tests that do not depend on external resources***. What if *FillText* were to discontinue their services? What if you have the power to unintentionally break that external resource? That's why you want to ***make your tests independent*** by mocking/faking that resource within the test. Basically you have to create your own *FillText* that returns the list to the code you want to test. How this is done is a more advance topic that goes beyond the scope of this post. But I do want you to understand what mocking is, and why it is important and even necessary to write good unit tests.

I have only worked with mocks within Angular and I have seen that <a href="https://docs.angularjs.org/api/ngMock/service/$httpBackend" target="_blank">$httpBackend</a> is one option to mock such a resource. Again, that's only one option!


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

{% include disqus.html %}
