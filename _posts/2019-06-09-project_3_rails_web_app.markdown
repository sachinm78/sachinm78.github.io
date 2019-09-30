---
layout: post
title:      "Project 3: Rails Web App"
date:       2019-06-09 16:08:49 -0400
permalink:  project_3_rails_web_app
---

For the third project in the full-time Web Development program, we were tasked with building our first Rails web app.  Like the Sinatra app we built for our second project, our Rails app will be a simple **Content Management System (CMS)** to keep track of some content of our choice.  For my project, I chose to create a TV show review application where users can rate and review their favorite shows.  

There is quite a lot that goes into building out your own Rails app.  Luckily, Rails comes packed with tools to help you build out exactly what you'll need for a functioning web application.  There are far more helpful Rails console commands available than I can list, but here is a great run down of some of the [most commonly used commands:](https://www.agiratech.com/rails-commands/).

There are quite a few requirements for this project.  Some of them proved to be quite challenging to achieve.  Here are some of the core requirements you will need to implement into your Rails app:

**Relationships in Your Models:**

For this project, your models must include:
* at least one **has_many** relationship
* at least one **belongs_to** relationship
* at least two **has_many :through** relationships
* a many-to-many relationship implemented with **has_many :through** associations 
 
The relationships start simple.  For example, in my project, **a user has many reviews**.  But things can quickly become confusing once you add a **has_many :through** relationship.  To meet this requirement, your models will need to include a **join_table** with foreign keys for your other models.  The image below is a great example from the Rails Guide for [Active Record Associations](https://guides.rubyonrails.org/association_basics.html)

![](https://guides.rubyonrails.org/images/association_basics/has_many_through.png)
*(Image source: https://guides.rubyonrails.org/association_basics.html)*

**User Authentication** 

One of the most challenging features to implement in my Sinatra project was user authentication.  In Rails, this becomes much easier to achieve thanks to a brilliant gem called **Devise**.  Devise comes jam-packed with some amazing features that will handle all of your user authentication requirements for this project.  You can even create basic views that you can use for your sign up and login pages.  It's also fairly easy to implement Devise if you have the right instructions to follow.  You can find that and much more about the [Devise Gem](https://github.com/plataformatec/devise) on their Github repository.

Devise almost sounds too good to be true, but it really is as amazing as it sounds.  One thing to note: your configuration in your controllers and your user model will be handled through Devise.  It's important to have a good understanding of how this will be different from how you may be used to handling user authentication in Sinatra and in most of the Rails labs.  I definitely feel it was worth the effort to learn how to use Devise.  I had my user authentication requirements completed in less than an hour.  That definitely called for celebration!

![](https://media.tenor.com/images/4a3ed62b7a158d34a37d8c53595b445f/tenor.gif)
*(Image source: https://tenor.com/search/snoopy-happy-dance-gifs)*

**Nested Resources**

A nested resource has a parent-child relationship that can match the relationships in your models.  You can read all about  nested resources and [routing in Rails](https://guides.rubyonrails.org/routing.html#nested-resources) here.  

For my project, I nested resources for my Show model under my User model (i.e. /users/:user_id/shows/:id).  While simple enough to implement in your routes, nested resources can be very tricky to code in your views and controllers.  The key thing to remember is that your forms will need two values passed in (i.e the :user_id and the :id for the show instance).  

This is a challenging requirement because there were only a few labs in the curriculum where we got to practice using nested resources.  It was made even more challenging because of the relationship requirements for this project.  Also, this is one aspect where using Devise made things a little tricky since Devise handles the user side of things.  

![Example Nested Resources](https://i.ytimg.com/vi/ZHJB9ddQlSs/maxresdefault.jpg)
*(Image source: https://www.lynda.com/Ruby-Rails-tutorials/Nested-resources/139989/159168-4.html*

Our Rails project had many specifications, which can seem daunting at first.  But as with anything in life, if you take it one step at a time, you'll be pleasantly surprised at how much you can achieve if you really put your mind to it.  I found this project to be challenging and at times, quite frustrating.  But in the end, it was a very rewarding experience to learn how to troubleshoot and problem solve my errors mostly on my own.  There's no better feeling of accomplishment than completing a difficult challenge.  You can do it, future coder!

If you'd like to see a video demonstration of my app, you can do so [here](https://www.youtube.com/watch?v=l3wu2nolwaA&t=3s).

Thanks for reading.  I’ll be back with some more thoughts on web development soon.  Until then, happy coding!  







