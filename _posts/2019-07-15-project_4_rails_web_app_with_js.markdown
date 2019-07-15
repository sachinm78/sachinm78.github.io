---
layout: post
title:      "Project 4: Rails Web App With JS"
date:       2019-07-15 18:55:54 +0000
permalink:  project_4_rails_web_app_with_js
---


Project 4 in the full-time Web Development program builds right on top of our Rails project from last time.  For this project, our task was to add Javascript front-end features to our existing Rails app.  For my Rails project, I chose to create a TV show review application where users can rate and review their favorite shows.  

The requirements for this project weren’t as daunting because unlike Ruby, where we had almost three months to prepare us for our first Rails project, we've only had a few weeks to get familiar with Javascript (JS).  Writing functions in JS is definitely a change from the style and structure of **Object-Oriented Ruby** (OO Ruby).  OO Ruby is easy on the eyes and the code reads logically.  That feels far from the case with JS.  The syntax took a little getting used to.

Thankfully, JS got some much needed improvements in the ES6 version released in 2015.  Among the many new features included in this version update were [arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) to simplify writing functions and improved variable declarations using [let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) and [const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const) keywords.  Using ES6 syntax to write your JS code will help you meet a majority of the project requirements with ease.

![](https://miro.medium.com/max/875/1*uKSqphvj9r712aKOujuZtQ.png)
*(Image Source: https://twitter.com/raganwald/status/564792624934961152)*

One element that proved somewhat challenging for me was to display form data dynamically using JS.  The simplest form from my Rails project for me to use was built using [nested resources](https://guides.rubyonrails.org/routing.html#nested-resources), which was a major requirement of our Rails project.  The challenge here was how best to get the user_id data for the current user and declare it in my JS code.  The solution that worked for me was using the **location.href** property and **Regular Expressions** to select the current user_id from the URL of the current page itself.  This was a great tip from a fellow member of my cohort.  

This project may feel daunting at first since JS syntax takes some getting used to.  But I was able to follow a wonderful example lesson from the Learn.co video library to help me pass all the requirements.  I highly recommend starting your project by watching and coding along with [this example](https://www.youtube.com/watch?v=oHPM0ekV7zQ).  

If you'd like to see a video demonstration of my app, you can do so here (coming soon).

Thanks for reading.  I’ll be back with some more thoughts on web development soon.  Until then, happy coding!  








