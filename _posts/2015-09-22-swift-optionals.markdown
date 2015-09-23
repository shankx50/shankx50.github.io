---
layout: post
title:  "Swift's optional type"
date:   2015-09-23
categories: programming
permalink: /swift-optionals
---
{% include stupid.html %}

## What are Swift optionals and why are they useful?

The Swift language introduces optional types, which handle the ***absence of value***. Optionals are an example of the fact that Swift is a ***type safe language***. Which would lead me to ask, what is a type safe programming language?

Wikipedia teaches that: <q>In computer science, type safety is the extent to which a programming language discourages or prevents type errors. A type error is erroneous or undesirable program behavior caused by a discrepancy between differing data types for the program's constants, variables, and methods (functions)...</q>

Ok, so how exactly does an optional prevent errors then? Swift is smart enough to prevent you from doing computations with variables of a specific type that may not be possible at all.

For example, can you calculate the square root of nothing? No, of course not. Hence:

      //WRONG
      var maybeNumber:Double? = nil

      maybeNumber = 56

      sqrt(maybeNumber)

In the case above, the compiler will complain. We set it to 56, but maybeNumber is still only an ***optional Double***. We need to add an if statement that checks whether maybeNumber is not nil. Then we can use the bang operator (!) to force unwrap the variable.

      //RIGHT
      var maybeNumber:Double? = nil

      maybeNumber = 56

      if(maybeNumber != nil){
      sqrt(maybeNumber!)
      }

One can use the optional type for many powerful features. One of them being conditional chaining.

      let degree = student.highSchool?.college?.degrees?[0]

The code above will only be non-nil if the student has passed highSchool, went to college and successfully graduated.

{% include disqus.html %}
