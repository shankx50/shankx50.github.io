---
layout: post
title:  "Too Much Abstraction"
date:   2015-05-10
categories: programming
permalink: /too-much-abstraction
---
{% include stupid.html %}

**_Abstraction_** is another word programmers like to use often, whereas I don't know if they always understand what it even means. **The definitions of abstraction**:

1. the quality of **dealing with ideas rather than events**: topics will vary in degrees of abstraction.
- something that exists **only as an idea**: the question can no longer be treated as an academic abstraction.
2. freedom from representational qualities in art: geometric abstraction has been a mainstay in her work.
- an abstract work of art.
3. a state of preoccupation: she sensed his momentary abstraction.
4. the process of considering something **independently of its associations**, attributes, or concrete accompaniments: duty is no longer determined in abstraction from the consequences.
5. the process of **removing something**, especially water **from** a river or other **source**: the abstraction of water from springs and wells.

I think when programmers talk about abstraction, they mean something along the lines of the first and fourth definition. I really like number four a lot. **The process of considering something independently of its associations**. In the case of high-level programming languages, we mean that we write code that itself generates low-level code. The lower the level of code, the closer it is to just 1 and 0's.

I know far to little to give you a good example, but what I can tell you is that when I write

    a = "e"
    print a

then those two lines of Ruby code generate a far bigger amount of assembly code that makes the screen print out my string "e" again.

However, I see a danger in the heavy use of high-level languages and application frameworks that help contemporary programmers get started. Yes, abstraction helps us to be productive, but at the same time it gives us the wrong belief that we know how to program, when in reality we don't. When I learned working with the Ruby on Rails framework, I was surprised about all the magic that happens behind the scenes. What connects my controller to my view and model? Mystery. Yes, it's good to get started, but we have to understand, that at some point, **we need to make the effort to try to understand what is going on under the hood**.

Where is the limit? What is a healthy balance between understanding low-level language and just being able to use a tool, and apply it successfully against solving problems. The answer is probably a different one depending on who poses the question.

Before you run off and learn assembly code, I do ask you to first explore and understand a contemporary programming language. This is something that I still have to do. It won't take very long till you'll read posts about language exploration on this blog. So far, I have dabbled a bit in JavaScript, Ruby, PHP, Python, SQL and C Sharp. I feel that it is time for me to focus on one language and really learn it along with solid programming principles. This brings up the ubiquitous question of new programmers: **Which language should I learn first?** Having read many good opinions, I think it boils down to **starting with a programming language you like, that you feel good with and that makes sense to you**. It doesn't seem to matter which language since you're not savvy enough yet to identity strengths and weaknesses of a specific language.


{% include disqus.html %}
