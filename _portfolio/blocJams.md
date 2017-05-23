---
layout: post
title: BlocJams
thumbnail-path: "img/blocjams.png"
short-description: BlocJams is a basic music player app.  My first front end app.

---

{:.center}
![]({{ site.baseurl }}/img/blocjams.png)


## Explanation

**The meat of this case study is to be found in my Conclusion (statement of learning) found at the bottom of the page.**

This was the first project at Bloc.io and it formed the majority of the frontend foundations section.  I built it three times; once using vanilla JS, once using jQuery, and a final time with AngularJS.  The final product is quite shallow with no database interaction as the focus of the project was on DOM manipulation.

## Problem

Create a web app with music play back capability.  The focus of the project was to learn about DOM manipulation using vanilla JS, jQuery, and AngularJS.

## Solution

I decided on a complete refactor to use AngularJS to create a single page app.  By using a single page app I could insure a more friction-less user experience by minimising load times between views.  As well, AngularJS allowed for a separation of concerns allowing for the future integration of more features.

## Results

A ready to go web app for playing music!  In its current state the app is quite bare bones but because it has been built (in its final incarnation at least) with AngularJS it could be easily wired into a more robust back end.

## Conclusion (Statement of Learning)

While I was able to consolidate my understanding of HTML, CSS, and Javascript the most valuble concept that I was able to get from doing this project was more programmatic.  By learning to use AngularJS I was able to see the basic structure of a much larger app.  I was able to see how all the parts interact and yet remain separate from each other.  

By learning the basics of AngularJS I was introduced to some very sound and broadly applicable programming theory.  I was able to gain an understanding of separation of concerns and functional programming.  Before this project much of the code I wrote was all built around the global scope - and my functions were ridiculously huge!

I have also developed a more thoughtful approach when solving programming problems.  To use an automotive analogy: Before learning AngularJS someone would tell me to build a car and I would say "Okay" and just start building making it up as I went along.  Now, when someone asks me to build a car I think about what I need (engine, wheels, cooling system, etc...) and how those parts might be connected.  Then I start building.

**As a Final Note:**

I have yet to find anywhere online a great high-level, beginner friendly, overview of AngularJS and what it does.  I found this incredibly frustrating when I was trying to get my head around what AngularJS was and why I should be using it.  This is something that I hope to change!
