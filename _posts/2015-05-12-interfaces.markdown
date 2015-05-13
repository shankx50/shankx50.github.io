---
layout: post
title:  "The Importance of Interfaces"
date:   2015-05-12
categories: programming
permalink: /interfaces
---
{% include stupid.html %}

An interesting and quite useful concept in programming is an *interface*. But what exactly are interfaces and why do we use them?

##In simple words, what is an interface?

Let's look at the definition that the dictionary gives us:

<blockquote>
A point where two systems, subjects, organizations, etc., meet and interact.
</blockquote>

The question we need to pose is, which two systems do we speak about in programming? I like to imagine two entities. On one side we have the programmer who may have certain expectations for a class he is working with. On the other side we have precisely that class. So system number one is the programmer, and system number two is the class.

##In simple words, why do we use interfaces?

An interface is sometimes **referred to as a contract** between the user of the class (the programmer) and said class. Let's see if we can use an everyday analogy to understand what an interface is. Say you have an employer (the programmer) and an employee (the class). The employer tells the employee that he expects him to always report the total number of sales at the end of a workday. The employee agrees and both parties (systems) agree to sign a contract (interface) that clearly states that the employer can expect the employee to always report the total number of sales at the end of each day. The contract could look somewhat like this:

    public interface Reporting
    {
      int getTotalNumberOfSales;
    }

If we were to describe the employee as a class, it could look like this:

    public class Employee implements Reporting
    {
      ...
      some strengths and weaknesses
      ...

      public int getTotalNumberOfSales()
      {
        return balance;
      }
    }

Both parties work with each other for many years until suddenly the employee gets very sick and has to quit the job. The employer is desperate because he was used to getting a great and accurate report at the end of each workday. He would like to find a new employee that provides the **exact same** report - or, that implements the exact same interface. In a job posting he may say that he needs a new employee that **implements the Reporting interface**. If he finds a new employee that commits to doing so, the employer is very happy because he knows that he will get the same report he's been used to for many years.

Guess what the new empolyee's class would look like...

    public class NewEmployee implements Reporting
    {
      ...
      other strengths and weaknesses
      ...

      public int getTotalNumberOfSales()
      {
        return balance;
      }
    }

In other words, the employer can predict what quality of work he will be delivered by **any employee who implements his contract/interface**.



{% include disqus.html %}
