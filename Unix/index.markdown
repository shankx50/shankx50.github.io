---
layout: page
title: SWIFT
date:   2015-09-18
permalink: /swift/
---
<p>Last update: {{ page.date | date: "%b %-d, %Y" }}</p>
SWIFT is the language to learn if you are interested in iOS development. Here are my notes:
<br/>

- strongly typed, but compiler infers the type. Hover over to have IDE show actual type
- no semi-colons at the end of expressions
- use key word ***let*** for constants and ***var*** for all other variables
- variables can't be ***nil*** unless you explicitly type them as ***optional*** like shown below

      var str: String?

- control structures


      for counter in 0..<10{
        if counter != 5{
          print(counter)
        }
      }

- switch cases in SWIFT do not fall through

- simple arrays

      var cars = ["Buick","Chevy","Ford"]
      cars[1] = "Dodge"

      for car in cars{

      }

- 2D arrays

      var beautifulImage =[
        [3,15,2],
        [2,33,4],
        [23,32,32]
      ]

      for i in 0..<beautifulImage.count{
        for j in 0..<beautifulImage[i].count{
          if beautifulImage[i][j] < 5{
            beautifulImage[i][j] = 5
          }
        }
      }



- hashes, maps, key-value pairs, in iOS Dictionaries

      var speed = [
        "Buick":"slow",
        "Dodge":"medium",
        "Ford":"fast"
      ]
      speed["Dodge"]

- basic functions

      func funcName(type: String) -> String {
        return "car"
      }

      func funcName(type: String = "default String", price: Int) -> String {
        return "car"
      }

      // subsequent parameters must be named when calling functions
      funcName("Buick", price: 1000)



- curly braces define a closure(function)
- use keyword ***inout*** in function signature when passing variables into functions and we want that the original variable passed in is modified by the function, not a copy. In this case we need to prepend an & to the variable passed in, when calling the function
