---
layout: post
title:      "Preparing For Your JavaScript Tech Interview: Part 2"
date:       2019-09-21 13:06:02 -0400
permalink:  preparing_for_your_javascript_tech_interview_part_2
---


In [part 1](http://crackingthecode.net/preparing_for_your_javascript_tech_interview) of this post, I listed out some resources to practice your JS skills to help prepare you for technical interview.  Here in part 2, I’ll list some key concepts you should know before your JS tech interview with resources to help you strengthen your knowledge and confidence so you don’t end up like this guy!

![](https://pics.me.me/thumb_programming-pro-tip-code-javascript-underwater-so-nobody-could-see-62401907.png)

## 5 Key JS Concepts

There are many key concepts that may come up in your technical interview.  Here are 5 every JS programmer should be familiar with, in no particular order.  For each concept, I’ve provided a brief overview and some additional resources to help you study up on them:

**This:** For new devs, one of the most difficult concepts to fully wrap your head around is the ‘this’ keyword. In most languages, ‘this’ is a reference to the current object instantiated by the class.  But of course, JS isn’t most languages.  In JS, ‘this’ normally refers to the object which ‘owns’ the method, but it depends on how a function is called.  One of the best rundowns on the “this” keywords I’ve found was on the [w3school’s JS documentation](https://www.w3schools.com/js/js_this.asp) website.  It's a good place to start if you need help understanding "this."

Additional resources:
* [JS MDN docs on "this"](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)
* [A Quick reference guide on “this”](https://alligator.io/js/this-keyword/) from alligator.io
* [Understanding “this”](https://medium.com/quick-code/understanding-the-this-keyword-in-javascript-cb76d4c7c5e8) from the Medium series Quick Code

**Closures:** Another JS concept that might come up in tech interviews is the closure.  The best explanation I’ve found on this topic comes from the Medium series *Master The JavaScript Interview*, which I have relied on heavily for this blog post.  Here is their definition of a closure:

“A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function’s scope from an inner function.”

I recommend reading their entire series.  You can start [here](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-closure-b2f0d2152b36).

Additional resources:
* [JS MDN docs on closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)
* [W3schools docs on closures](https://www.w3schools.com/js/js_function_closures.asp)

![](https://i.imgflip.com/h0dj1.jpg)

**Pure Functions:** This one is a bit simpler to grasp.  A pure function will always return the same output when given the same input as an argument.  In other words, pure functions have predictable outcomes.  That makes them a key concept in functional programming since pure functions are less likely to have bugs.  Medium’s Mastering The JavaScript Interview series has an excellent rundown on[ this topic](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-pure-function-d1c076bec976).  You should also review the different kinds of functions in JS.  Here are the [official docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions).  

**== vs ===:** Leave it to JS to make even comparisons complicated.  An important concept to grasp is the difference between the double and triple equals sign.  Because the == in JS does type conversions, it can result in false equivalencies, so it’s considered best practice to use === for comparisons.  Before your tech interview, it can’t hurt to review all the [comparison operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators) in JS.

Additional resources:
* A good rundown on [this topic](https://codeburst.io/javascript-double-equals-vs-triple-equals-61d4ce5a121a) from Medium

**Hoisting:** In JS, variables are moved to the top of their scope before they are executed.  If the variables haven’t been properly defined, their values can be “hoisted,” leading to errors.  One way to avoid this issue is to use the *let* and *const* keywords when defining variables.  W3schools has a pretty simple explanation on [this topic](https://www.w3schools.com/js/js_hoisting.asp).

Additional Resources:
* [MDN docs on hoisting](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting)

![](https://karolgalanciak.com/images/js_results_not_so_wut.jpg/)

These are just a few key concepts that may come up during a technical interview.  Be sure to review them, but don’t stop there.  There are loads of resources available to help you prepare for your technical interview.  I’ll close this post with a few additional resources that go beyond what I’ve covered here:

* [10 concepts](https://www.infoworld.com/article/3196070/10-javascript-concepts-every-nodejs-developer-must-master.html) every JS programmer should know
* [A Perfect Guide](https://medium.com/dev-bits/a-perfect-guide-for-cracking-a-javascript-interview-a-developers-perspective-23a5c0fa4d0d) for cracking the JS Tech Interview
* The [Medium blog post](https://medium.com/@marcellamaki/my-javascript-tech-interview-prep-notes-part-1-concepts-d78637058599) that inspired me to write this series

I’ll be back soon with more tips and resources for you.  Until then, happy coding!

