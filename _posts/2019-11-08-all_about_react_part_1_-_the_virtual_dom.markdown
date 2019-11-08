---
layout: post
title:      "All About React: Part 1 - The Virtual DOM"
date:       2019-11-08 18:51:54 +0000
permalink:  all_about_react_part_1_-_the_virtual_dom
---


This month, I’ll cover new topics related to React each week.  For the first post in this series, let’s take a look at one of the features that makes React so popular: the **Virtual DOM**.

## The DOM

First, let’s talk about the **DOM**, or [Document Object Model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction).  We can think of any website as a document made up of an HTML or XML tree.  To make edits or updates to the website, we need a programming interface.  For most modern web browsers, that interface is the DOM, which represents the document as nodes and objects.  The DOM is an object-oriented representation of the web document that can be edited using scripting languages such as JavaScript.  

## Limitations With The DOM

Modern web browsing is dynamic and users have become accustomed to speedy usage.  There is also far  more interactivity and functionality to most web applications today than just a few years ago.  Every time there is a change to the current state of the web app, the DOM gets updated to represent that change.  There are a couple of problems that arise here:

1. DOM manipulation can slow down performance.  
2. Most JavaScript frameworks make more updates to the DOM than they have to, further slowing things down.  

To combat these issues, the people at [Facebook created the React framework](https://en.wikipedia.org/wiki/React_(web_framework)) featuring something new: the **Virtual DOM**.  

![](https://miro.medium.com/max/800/1*CqdIWZy0NMPQhYx2rKzo9g.png)
*DOM vs Virtual DOM Diagram (Source: https://miro.medium.com/max/800/1*CqdIWZy0NMPQhYx2rKzo9g.png)

## The Virtual DOM

The [Virtual DOM](https://reactjs.org/docs/faq-internals.html) is a representation of the actual DOM and its use was made popular by the React framework.  In React, for every DOM object, there is a Virtual DOM object that corresponds to it.  The virtual object has all of the same properties as the real DOM object.  Manipulating the virtual DOM object is faster than manipulating the DOM object because the changes don’t need to be made on the user interface.  Think of the virtual DOM as editing a blueprint as opposed to editing the structure of the object itself.  

So why is it faster?  Because unlike with the actual DOM, there is no need to do unnecessary updates to all the DOM objects.  Instead, React compares the virtual DOM to the actual DOM and then changes only those elements that need to be updated.  This makes for improved performance compared to manipulating the DOM directly. This improved performance is one of the factors that make React so popular.  

This concludes my brief overview of the Virtual DOM.  If you’d like to go deeper into this topic, you can try reading the blog posts [here](https://reactkungfu.com/2015/10/the-difference-between-virtual-dom-and-dom/) and [here](https://programmingwithmosh.com/react/react-virtual-dom-explained/).  I’ll be back next week with some new React related content.  Until then, Happy Coding!



