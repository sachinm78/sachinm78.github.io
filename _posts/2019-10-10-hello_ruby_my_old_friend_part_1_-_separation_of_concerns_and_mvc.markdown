---
layout: post
title:      "Hello Ruby, My Old Friend: Part 1 - Separation of Concerns and MVC"
date:       2019-10-10 14:00:02 -0400
permalink:  hello_ruby_my_old_friend_part_1_-_separation_of_concerns_and_mvc
---


For the past month or so since graduating from Flatiron, I’ve been focused on the job hunt and how best to prepare for the next steps after graduation.  I decided I would work to strengthen areas I felt less confident in or that needed improvement.  So I spent this past month working through JS lessons to increase my comfort level with the syntax, CSS tutorials to improve my styling abilities, and interview prep to boost my confidence in interviews, especially ones that are technical in nature.

Along the way, it seems that what I once saw as a strength - my knowledge and familiarity with Ruby - has gotten rusty from lack of practice.  I realised this in a technical interview where I chose to write my answers in Ruby, only to find that I was often using JS syntax and had forgotten some of the common Ruby methods for manipulating data in an array.  Thankfully, my interviewer was patient and helped me through the exercises.  Still, I wasn’t happy with my performance and I know I have room for improvement.  So, for my next series of posts, I will cover some of the Ruby topics I’ve been told may come up in technical interviews.  Let’s start with something basic but important to know to keep your code manageable: **[Separation of Concerns(SoC)](https://en.wikipedia.org/wiki/Separation_of_concerns)**

## SoC

In computer programming, **SoC** is a key design principle stating that software should be built in distinct features that overlap as little as possible.  There are many advantages to building software following the **SoC** principle including:

* Each part of your program will have a specific function, making it easier to trace and debug.
* You can understand one part of the program by knowing its concern without having to worry about the others.
* You can work on sections of code independently and check for functionality in each section before building out more complexity.
* It helps to keep your code well organized and *[DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself).*

Whether you’re just beginning to learn code or you’re a seasoned veteran, **SoC** is a principle you should adhere to.  In Ruby, that’s made easy using Rails and **[MVC Architecture]( https://www.sitepoint.com/model-view-controller-mvc-architecture-rails/)**.

![](https://www.guru99.com/images/1/122118_0445_MVCTutorial1.png)
*Diagram of MVC Architecture*

## MVC Architecture

If you’ve built a Rails application, you’re probably familiar with using the **SoC** design principle.  That’s because it’s considered best practice to follow the **MVC Architecture** when building out a Rails app.  So what does MVC stand for?  At a very basic level, it can be outlined as follows:

* **M - Models:** This is where the data from your database is handled.  Models also handle *[validations](https://guides.rubyonrails.org/active_record_validations.html)* and *[associations](https://guides.rubyonrails.org/association_basics.html)* between different models.

* **V - Views:** This is the user interface or what the user sees in the browser.  Views often consist of HTML code styled with CSS and JavaScript.

* **C - Controllers:** This is the brains of the operation that handles how the Models and the Views interact with each other.

Just like we discussed with **SoC**, using **MVC Architecture** has many advantages including:

* **Reusable code:** You can use the data from a model in multiple views.  
* **Easier to maintain and debug:** Because you’ve separated concerns, making changes to one component to fix errors or enhance functionality should not break the others.
* **Easier to Scale:** As your application grows, it will be easier to manage.  For example, if you decide to upgrade your database, your views and controllers can remain unchanged.

If you’d like to take your understanding a bit deeper, here’s a great [blog post](https://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/) that goes into much more detail.  

That’s it for this week’s return to Ruby.  Check back soon for more Ruby tips and tricks.  Until then, happy coding!

