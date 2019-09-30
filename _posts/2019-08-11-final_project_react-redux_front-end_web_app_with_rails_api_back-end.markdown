---
layout: post
title:      "Final Project: React-Redux Front-end Web App With Rails API Back-end"
date:       2019-08-11 16:42:38 -0400
permalink:  final_project_react-redux_front-end_web_app_with_rails_api_back-end
---


The final project in the full-time web development program required us to use all that we’ve learned over the past few months to create a full-stack web application of our choice.  In this blog post, I’ll go over some of the key concepts required to build out your application and provide some resources and tips to help you meet the project requirements.

Let’s break down this project into 3 main categories:

1. REACT
* Getting started
* Container Components vs. Presentational Components

2. REDUX
* What is Redux?
* Redux Thunk

3. Rails API
* Creating seed data
* Connecting your API to your React


### **1. REACT**

**Getting Started:** For this project, I found myself struggling to get started at first because I wasn’t quite sure what I wanted to build.  I also didn’t feel completely comfortable with some of the new course material, and I wasn’t quite sure if I should start with the front-end or back-end.  So I decided to take some time early in project week to practice connecting React apps to Rails APIs and get more comfortable with all the new course materials in this final section of our program.  If you too are struggling to get started, I highly recommend watching and coding along to the following video tutorials from the Learn Library:

* [Mock-bnb](https://www.youtube.com/watch?v=cRuJCeXZadM) application
* Kais surf shop [Part 1](https://www.youtube.com/watch?v=nnqmLFop8Cg) and [Part 2](https://www.youtube.com/watch?v=9KrrlWy1E_A)

Even if you know exactly what you want to build, these videos will definitely still help you get started, troubleshoot, and follow good habits as you code.  

After completing the tutorials and feeling much more comfortable with the ins and outs of a React-Redux app, I was ready to get started.  After playing around with a few ideas for a day, I eventually settled on making a random generator app.  Before starting at Flatiron, I was working as a STEM educator teaching coding, robotics and digital design to elementary students.  One of the fun apps we built using block coding language was a random funny name generator.  That inspired me to try something similar on a larger scale.  I ended up with 4 themed random generators:
* Random Superhero Name
* Random Star Wars Adventure
* Random Hipster Ipsum Sentence
* Random Smart Dev Sentence

I decided to build out my front-end application first because in order for me to create database tables for my project, I needed to know what it would look like first.  Also, in practice, I found the Rails API to be quite simple to create.  If you have a solid idea of what your models will look like, it may be better for you to start with the easier back-end application.  But if you aren’t quite certain about your tables, definitely start on the front-end, otherwise you will probably need multiple changes to your database and might even need to start over from scratch.  

When you’re ready to get started, simply use the command *create-react-app your-app-name*.  

*Sample File Structure Using create-react-app*
![](https://hackernoon.com/hn-images/1*eXN1LlNnuZmosJ7n7EsJ-Q.png)
*(Image source: https://hackernoon.com/hn-images/1eXN1LlNnuZmosJ7n7EsJ-Q.png)*

**Container Components vs Presentational Components:** One of the most important concepts to make sure you understand before working on your project is the difference between Container - *or functional* - components and Presentational - *or stateless* - components.  The primary difference between the two is that  Container components care about *how things work* and Presentational components care about *how things look*.  

To fully understand the difference between the two, we need to talk about **state**.  State is an object that helps determine how a component will handle changes to data.  In fact, React’s ability to quickly and easily manage changes to state is what truly makes it special.  A Container component will be more complex and handle changes to state, while a Presentational component will generally be simpler and not concerned with state.  

Here are some helpful resources to help you fully grasp these concepts:
* [React Component](https://reactjs.org/docs/react-component.html) Documentation
* An [explanation](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0#.ezqa6w143) from React creator, Dan Abramov

### **2. REDUX**

**What is Redux?**  React is very powerful, but it does have some limitations.  Redux is a state container for React applications that simplifies how we manage state.  By placing state in one simple JS object and allowing all parts of our application to access that object, Redux helps make our React more efficient and our code easier to manage.  

To do this, Redux uses a pattern of [actions](https://redux.js.org/basics/actions) and [reducers](https://redux.js.org/basics/reducers) working together to manage the [store](https://redux.js.org/basics/store) - a single object that holds the application’s state.  Actions are payloads of data that send changes to state based on what occurs (e.g. a user clicks a button.  Reducers specify how state will change based on those actions.  These actions can then be imported into your Container components to be called as needed.

*Redux Data Flow*
![](https://image.slidesharecdn.com/theevolutionofreduxactioncreators-160825141450/95/the-evolution-of-redux-action-creators-5-638.jpg?cb=1472134833)
*(Image source: https://image.slidesharecdn.com/theevolutionofreduxactioncreators-160825141450/95/the-evolution-of-redux-action-creators-5-638.jpg?cb=1472134833)*

**Redux Thunk:** The final piece to our front-end puzzle is a middleware called **Thunk**.  Thunk allows us to use our Redux action creators to return a function instead of a plain old JavaScript object.  I found it easy to implement this middleware, but if you’re struggling to understand it, try this [blog](https://daveceddia.com/what-is-a-thunk/).

For more information on Redux, read the [official documentation](https://redux.js.org/introduction/getting-started)

### **3. RAILS API**

**Creating Seed Data:** As I mentioned above, setting up your Rails application should be fairly simple and painless.  If you know what your database should look like, you can have your back-end up and running in less than 30 minutes!  Take a moment to think about that.  Remember how hard Rails seemed when you first started it a few months ago?  Well, good news!  It gets easier and more familiar with each day.  

Since my application required a lot of unique data to optimize randomization, I used a very helpful gem called [faker](https://github.com/faker-ruby/faker) to seed my database.  Faker is great.  It has lots of different categories you can try and plenty of unique data available.  Even if you don’t need a lot of seed data, faker is a great way to create a small data set to test out your API.  My project wouldn’t have been possible without it.  And if you choose to connect to an external API instead, here are a few helpful resources:
* Saving External API Data to Your Rails API: [Blog](https://itnext.io/saving-external-api-data-to-your-own-rails-api-fad0fa75066) 
* A Searchable [API Directory](https://www.programmableweb.com/apis/directory)

**Connecting Your API to React:** Once you have your API set-up with data seeded and properly rendering in json, connecting to your React app is easy.  For this project, we were required to use the **fetch() method** within our actions to GET and POST data from our API.  

A couple tools you will definitely want installed are the **React and Redux DevTools** extensions.  These tools are key in testing your data as you build your app.  And when you’re ready to connect to your API, the Redux Dev Tools will be your best friend to test your data and debug any issues.  They are available for most modern browsers, but I recommend using Chrome as your go-to browser for web development.  
* [React Dev Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en) for Chrome
* [Redux Dev Tools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd?hl=en) for Chrome

![Redux DevTools](https://i.stack.imgur.com/1rHes.png)
*(Image source: https://i.stack.imgur.com/1rHes.png)*

**Final Thoughts:** Like every project in our curriculum, this project seemed overwhelming at times.  But once again, I feel I learned the most and really honed my knowledge as I built, broke, troubleshot, and fixed my application.  In the end, I made an application that is fun, unique and really resonates the playful side of my personality.  It’s hard to believe that this is the last project in this program.  The curriculum may be over, but my coding journey is just beginning!

If you'd like to explore the code for this project, here is a link to my repos:
* [Randomness API](https://github.com/sachinm78/Randomness-api) Rails Application
* [Randomness Client](https://github.com/sachinm78/Randomness-client) React-Redux Application

And if you'd like to see a video demonstration of my app, you can do so [here](https://www.youtube.com/watch?v=ClmMETSF2no&t=8s).

Thanks for reading.  I’ll be back with some more thoughts on web development soon.  Until then, happy coding!  

