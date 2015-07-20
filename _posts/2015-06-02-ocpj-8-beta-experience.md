---
layout: post
title: My OCPJ 8 Beta exam experience
description: My experience taking the Java SE 8 Programmer II (1Z1-809) beta exam.
categories:
  - java
  - certification
---

Today I took the OCPJ 8 beta exam. I didn't get a free voucher (I sent too late my application and there was a limited number of vouchers) so I had to pay $50 USD. Still, a great value for the money.

Three hours and 106 questions. It's a tough exam.

I think with some luck, I'll barely pass this time. I forgot about the rules of default methods in interfaces and inheritance rules about the throws clause. Anyway, I got a lot of questions related to lambda expressions. I would say about 30% of the exam, in one way or another, is about lambda expressions.

Based on my experience, here's a breakdown of the topics I got, so you can make sure to study them:

**Java Class Design**

* 2-3 questions about the concept of encapsulation
* Questions about inheritance regarding visibility modifiers and declaring throwing exceptions
* How to override equals and how it behaves if you don't override it
* How to create a singleton class
* Rules about static classes
 
**Advanced Java Class Design**

* Rules about abstract classes
* Final keyword on classes and methods
* 2-3 questions about how to create inner classes
* How to use methods and constructor inside an enum
* Extend and implement an interface (study the rules of defaults methods)
 
**Generics and Collections**

* Create a class with generic parameters
* Use ArrayDeque
* Use java.util.Comparator and java.lang.Comparable interfaces and Collections.sort
* Filter a collection by using lambda expressions
 
**Lambda Built-in Functional Interfaces**

* Use of Predicate, Consumer, Function, Supplier and UnaryOperator
* Just one or two questions about the primitive and binary versions, not hard
 
**Java Stream API**

* Focus on peek(), map(), flatMap(), max(), grouping, sorting, and Optional class
 
**Exceptions and Assertions**

* Focus on the rules of multicatch
* Create auto-closeable resources
* Enable asserts and the syntax *assert condition : expression*
 
**Use Java SE 8 Date/Time API**

* Work with ZonedDateTime, for example, what happens when you add hours to the time when the daylight savings starts
* Basic use of LocalDateTime, Instant, Period, and Duration
 
**Java I/O Fundamentals**

* Use of System static members and Console object
* Use of FileInputStream, BufferedReader, and BufferedWriter
* Rules about serialization
 
**Java File I/O (NIO.2)**

* Path operations (create paths, relative paths, normalize)
* Stream methods, for example, how to read a file with streams
 
**Java Concurrency**

* Identify a deadlock in code
* Use of CyclicBarrier
* The concept of the Fork/Join Framework
* Parallel Streams using reduction operations
 
**Building Database Applications with JDBC**

* Know the core interfaces and classes of the JDBC API and which of them have to implement the datasource provider
* How to load a driver and use the DriverManager class
 
**Localization**

* Know all the constructors of the Locale class
* Know which resource bundle is loaded depending on the locale set.
 
I created my own material to study. I put it online at [http://eherrera.net/ocpj8-notes/](http://eherrera.net/ocpj8-notes/) for all planning to take this exam.

Based on this notes, I'll create a study guide. It's going to be huge book, so even tough the exam won't be available until around September-October 2015, I'll start right now.

Feel free to ask me something in particular or any doubt you have about a topic covered by the exam. 