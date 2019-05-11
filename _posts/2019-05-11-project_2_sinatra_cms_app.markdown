---
layout: post
title:      "Project 2: Sinatra CMS App"
date:       2019-05-11 13:23:08 -0400
permalink:  project_2_sinatra_cms_app
---



For the second project in the full-time Web Development program, we were tasked with building a simple **Content Management System (CMS)** to keep track of something we’re interested in.  I chose to create a reading list application where users can track what they are currently reading.  

Here are some of the requirements for our Sinatra app:
* Must use **Sinatra ActiveRecord**
* Must use the **Model-Views-Controller (MVC)** file structure
* Must use one **has_many** and one **belongs_to** relationship
* Must allow users to perform **Create, Read, Update, Delete (CRUD)** actions

Let’s look at each of these requirements in more detail:

**Sinatra ActiveRecord:** To understand ActiveRecord, first we must understand the importance of **Object Relational Mapping (ORM)**.  In Object Oriented languages like Ruby, ORMs allow us to wrap our data in Ruby objects so we can easily manipulate them.  Instead of writing out Ruby methods by hand like we did for our CLI Gem project, here we can use the ORM ActiveRecord to inherit all the methods we will need to manipulate our object data.  

![](http://wiki.expertiza.ncsu.edu/images/2/2c/ORM_Flowchart.jpg)
*(Image source: http://wiki.expertiza.ncsu.edu/images/2/2c/ORM_Flowchart.jpg)*

For a basic overview of ActiveRecord and ORMs, check out the Rails guide [here:](https://guides.rubyonrails.org/active_record_basics.html)


**MVC File Structure:** When creating a computer program, it’s important to remember the Separation of Concerns (SoC) principle.  By separating our code into distinct sections that are each responsible for performing specific tasks, it will be far easier to debug and maintain our program over time.  

In the MVC format, Models serve as “the brains” of the application.  This is where we can implement ActiveRecord to manipulate our data.  This is also the place you will likely spend the least amount of time writing code since ActiveRecord has already done the heavy lifting for you.  

The Views section of you app is the user interface.  Here, we write all our CSS and HTML code that creates the user experience.  Everything your user can see or interact with in your application will be coded here.  

![](https://cdn-images-1.medium.com/max/1000/1*JY9MYH-w_aBOZHfCJCx52Q.png)
*(Sample Sinatra MVC File Structure: Image source: https://cdn-images-1.medium.com/max/1000/1JY9MYH-waBOZHfCJCx52Q.png)*

Last but definitely not least, the Controls section of your application is where you will spend the majority of your time working and debugging.  Controllers are the link between the Models and the Views.  They allow the Models and Views to communicate.  The Controllers section is also generally further broken down so that routes for actions by the user are separate from routes for the object in question and general routes for the application.  

**Relationships (has_many and belongs_to):** In ActiveRecord, we can use **Associations** to help connect our data.  For example, if you are creating an app that will track your favorite shows, you could say that your users have many shows and that your shows belong to a user.  For my project, my users have many books and books on a reading list belong to a user.  

For more about ActiveRecord Associations, check out the Rails guide [here:](https://guides.rubyonrails.org/association_basics.html)

**CRUD:** In computer science, the four basic functions of persistent storage are create, read, update, and delete.  These are the functions our user will expect from our app.  In my Reading List application, users should be able to create a unique account, log in and out of the application, add books to their reading list, and then edit, update or delete those books.  

That covers some of the basics needed to create this project.  Just like with your first project, you are likely to encounter numerous bugs and errors along the way.  There may even be moments where you feel like giving up or that it’s just too difficult to do.  When you feel those negative thoughts creeping in, take a deep breath and reach out for help.  My cohort lead and fellow members definitely helped me troubleshoot issues along the way.  Also, don’t forget to return the favor and help others along once you’ve completed your project.  

If you'd like to see a video demonstration of my app, you can do so here: (coming soon)

Thanks for reading.  I’ll be back with some more thoughts on the process of learning web development soon.  Until then, happy coding!  







