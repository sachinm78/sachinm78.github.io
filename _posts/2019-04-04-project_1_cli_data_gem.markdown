---
layout: post
title:      "Project 1: CLI Data Gem"
date:       2019-04-04 21:47:56 +0000
permalink:  project_1_cli_data_gem
---


This week, my cohort (#team-ninja-vis-hid) and I began working on our first project: a CLI data gem.  When coding in Ruby, a gem is a library or data file that you can use to enhance, improve and add functionality to your code.  For more information on gems, check out this helpful guide from Stack Overflow: [](https://guides.rubygems.org/what-is-a-gem/)

CLI stands for command line interface.  In the early days of the tech revolution, CLIs were the primary way programmers interacted with their code.  These days, many users would be unfamiliar with CLI’s, but they’re still an essential tool in the belt of any software engineer.  I’m old enough to remember booting up a PC and using MS-DOS or when the first internet chat rooms were CLI applications where users could type and communicate with people from anywhere in the world.  It all sounds ordinary now in a world where we have internet access in the palm of our hands.  But back when I was just starting college, CLIs were all the rage. 

![](https://images.techhive.com/images/article/2014/05/freenas-menu-100300525-orig.jpg)
*Example CLI Display*

Here's a basic summary of our CLI project, in a nutshell: 
* **Build a CLI interface.**  It should greet the user and offer menu commands to navigate.  It should offer some menu options.  It should print out the desired data based on the user’s input.  
* **Scrape a website for data:** Choose any website of interest to try to scrape data from.  The data should come from two levels of the web page (i.e. we should scrape some data from a home page.  Then, click on a link to another section of that web page and scrape more data from there as well.  
* **Collect, store and display that data.** Use Object Oriented (OO) Ruby to code your CLI gem.

Let’s cover some of the key tools needed to complete this project:

**OO Ruby:** one of the reasons Ruby is a wonderful place to start with for anyone new to coding is that Ruby code reads like a language.  It’s straight and to the point.  But the coolest thing about Ruby is how we can use code to create objects that behave similar to how those same objects would interact in real life.  It’s definitely a fascinating language and one that every coder should explore.  

![](https://d2aw5xe2jldque.cloudfront.net/books/ruby/images/class_instance_diagram.jpg)
*Example of OO Ruby Class / Object Relationship*

There are tons of resources available online to learn more about OO Ruby, but I highly recommend starting with “Why’s Poignant Guide to Ruby.”  It’s not your typical book on coding.  It’s hilarious, quirky, and full of cartoons that will keep you laughing while you learn.  Frankly, it deserves its own blog post.  Trust me, it’s good, and it’s free!  Check it out here: 
[](https://poignant.guide/)

**Chrome Inspect Tool:** one of the coolest features included with Google Chrome is the “Inspect” tool.  Next time you’re browsing the web, right-click on any element on the page and select “Inspect.”  This will open up Chrome’s development tools menu.  It’s definitely easy to get lost in all the information being provided, but the key is to learn to parse all the HTML elements and find exactly the data you want to scrape.  

![](http://img.ezlocal.com/j/Step-3-Modify-Code.png)
*Example of Google Inspect*

**Ruby gems:** remember those gems I mentioned at the top of this post?  Here’s where they come in handy.  Two that you will definitely need to require in your code are Open-Uri and Nokogiri.  The first allows you to use a simple “open(URL)” command to open the URL between the parentheses.  Nokogiri then jumps in and helps you parse, or sift through, all the data until you find exactly the elements you need.  

Finding the right elements can be tricky, especially if you’re unfamiliar with HTML.  But don’t fret because there’s another amazing gem that will be your best friend on your journey through OO Ruby programming: Pry.  

Pry allows the programmer to jump right into their code to play around and see what it might output.  It was absolutely essential for me to help find the bugs in my code.  It was especially helpful when looking for the best HTML elements to try to scrape data from.  In Pry, I could copy and paste a particular HTML class element from a web page to see what data it contains.  Through this method, I was able to find exactly the data I needed.  If you’re planning to learn Ruby, make sure you have Pry as your go-to debugging tool. For more about Pry, check out this site: [](https://pryrepl.org/)

![](https://i0.wp.com/www.rubyguides.com/wp-content/uploads/2015/07/pry-binding.png)
*Example CLI display using Pry*

The final gem I used was called Colorize.  Before adding this gem to my project, my code looked dull and it was difficult to follow the content on the page.  With colorize, I could use commands to add color to my text, highlighting and other cool formatting to create a better user experience.  It was super simple to implement.  You can learn more about Colorize here: [](https://github.com/fazibear/colorize/blob/master/README.md)

That covers some of the basics needed to create this project.  One last piece of advice: choose a topic you care about.  I started the week with a topic that I wasn’t really into, but it seemed like it would be easy to try to scrape.  The problem was, I didn’t feel inspired or motivated by the topic I had chosen.  So instead, I scrapped what I had worked on that first day and decided to scrape data from the Chicago Blackhawks team roster.  

I’ve always been a sports fan, and growing up in Chicago, I’ve been treated to some amazing sports moments.  The 85 Bears super bowl team is the earliest one that jumps out at me.  Then there was the Jordan era where the Bulls dominated the NBA.  There’s also of course the Cubs and their century of futility.  Thankfully, they finally ended their curse!  But out of all the local teams, I’ve always been drawn most to the Blackhawks.  

I first started watching hockey in the early 90’s when the Blackhawks were aiming for their first Stanley Cup victory since the 1960’s.  But I didn’t start loving hockey until 1994.  That’s when the world was introduced to the first truly great sports simulation game: NHL ‘94.  That game on the Sega Genesis revolutionized sports video games and is still considered one of the best of its kind on the early gaming platforms. 

![](https://s.yimg.com/ny/api/res/1.2/xw_IOuIRxB9TIferCwg_jA--~A/YXBwaWQ9aGlnaGxhbmRlcjtzbT0xO3c9NjMwO2g9NDE2O2lsPXBsYW5l/http://media.zenfs.com/en/blogs/sptusnhlexperts/faFSAsaffssa.jpg)
*NHL ‘94 Screen Shot - So Epic!*

My love for hockey and Chicago sports in general is something I took with me as I travelled and taught in South Korea and beyond.  In fact, it wasn’t until I was living in Korea that I actually played a hockey game in real life.  There, I was lucky enough to be a part of a charity hockey team that played street hockey every weekend and raised money for local charities.  Jeju Islanders 4 Life!

![](http://www.erichevesyphotography.com/wp-content/uploads/2016/01/Blog6_15MeaningfulPhotos2015-1-of-22.jpg)
*Jeju Islanders Team Photo*

So with a topic I cared about in hand, it was a couple days of trial and error, of playing with and debugging with Pry, and of pulling and testing data to complete my first Ruby gem!  A few final thoughts on the process:
* **It’s hard, but rewarding.**  It will feel like an impossible task, but it’s not.  Just keep at it!
* **Make sure you have a great support group.**  It’s always more fun to have someone to show your code to and to bounce ideas of off.  I wouldn’t have completed this project without the support of my cohort lead and fellow ninjas!
* **Use Google!** Whether you're doing it on your own or with support,  just make sure that you explore all the resources out there at your fingertips.  I have barely scratched the surface here.  

Thanks for reading.  I’ll be back with some more thoughts on coding soon.  Until then, happy coding!  

