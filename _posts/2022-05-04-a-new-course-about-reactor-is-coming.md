---
layout: post
title: A New Course About Project Reactor Is Coming
description: Where I explain my plan for realeasing a free course about Project Reactor.
categories:
  - project reactor
  - news
  - course
---

For the last five years, I've been producing courses for Pluralsight.

It's a great company to work with, but when you work with (or for) someone else, you don't get a lot of flexibility (for example, to release any course you want and when you want it).

That's why I'm going to make an experiment. I'm going to release a course about Project Reactor on GitHub and YouTube for free, something like my [study guide for the Java 8 certification exam](https://ocpj8.javastudyguide.com) but with video. I'll see how to monetize it later (probably by selling the printed book version or with ads).

The idea is to create a course that teaches the fundamentals of reactive programming with Project Reactor. Here's a high-level outline of the course (subject to change):
- Introduction to reactive programming
- Creating a sequence with Flux and Mono
- Transforming a sequence with the map and flatmap operators
- Using other reactive operators
- Handling errors
- Schedulers and threading
- Using a context
- Working with blocking calls
- Testing with StepVerifier

In general, I create my courses following these steps:
1. First, I write all the content and create all the examples.
2. Next, I create the slides.
3. Then I record the audio and the video separately.
4. Finally, I synchronize the audio and video, add call-outs, etc.

So first, I'll write the text of course as if it were a book. At the same time, I'll create the slides and other visual elements from where I'll get the images and GIF animations that will accompany the text. 

For this, I've created a [GitHub Pages site](https://eherrera.net/project-reactor-course/) that I'll be updating with the content of the course in the following weeks. Right now, it only has the main modules of the course (according to the outline above) with sample subsections as placeholders.

Once I have all the text, I'll use it as the script to record the video for each lesson. I'll upload the videos to YouTube and embed them on the corresponding pages.

After this course, if there's demand for it, I can create more courses to teach how to develop reactive microservices with Spring and Kubernetes.

On the other hand, I'll keep working with Pluralsight. I've sent a proposal for a JMeter course oriented to Java developers, about how JMeter (and other tools) can be used to test the performance of Java applications. However, it may take weeks to get approved. Also, I'll keep updating my existing [courses](/courses/), as long as they don't decide to retire them or freeze them in a particular version.

If you have questions or comments, don't hesitate to contact me via [email](mailto:&#101;&#115;&#116;&#101;&#98;&#97;&#110;&#104;&#98;&#50;&#64;&#121;&#97;&#104;&#111;&#111;&#46;&#99;&#111;&#109;&#46;&#109;&#120;) or [Twitter](https://twitter.com/eh3rrera).



