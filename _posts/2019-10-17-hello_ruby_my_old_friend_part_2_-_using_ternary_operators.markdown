---
layout: post
title:      "Hello Ruby, My Old Friend: Part 2 - Using Ternary Operators"
date:       2019-10-17 14:36:16 -0400
permalink:  hello_ruby_my_old_friend_part_2_-_using_ternary_operators
---


This month, I’m revisiting an old friend, Ruby, and covering topics related to Ruby and Rails.  In the [1st post in this series](http://crackingthecode.net/hello_ruby_my_old_friend_part_1_-_separation_of_concerns_and_mvc), I covered the **Separation of Concerns (SoC) Principle** and **MVC Architecture**.  This week, I’ll focus on a neat tool to help write cleaner, concise simple conditional statements in Ruby: the **ternary operator**.  

When you’re first starting out learning Ruby, it’s okay to focus on writing code that works first and foremost.  After all, the goal at the end of the day is to have code that’s functional.  And once you have that code working, it’s good practice to revisit it to see if it can be simplified or improved.  This is where things can get confusing for new developers.  One of the beauties of Ruby (or maybe one of the pitfalls if you’re new to coding) is that there are many ways to accomplish the same task.  So as a new developer, how do you know what’s best?  The answer to that will vary case by case, but it’s always good to know the tools at your disposal that can help take a large block of code and make it more concise and easier on the eyes.  One such tool that every Ruby developer should get comfortable using is the [ternary operator](https://www.rubyguides.com/2019/10/ruby-ternary-operator/).  

## What is a ternary operator?

Ternary operators are a great shorthand approach to writing out *if/else conditional statements.*  Let’s start by defining the name.  “Ternary” means composed of three items.  These parts include a conditional statement and two possible outcomes, one *truthy* and one *falsey*.  In simpler terms, the three items are your object that you’re performing a conditional statement on, what happens if that statement is true and what happens if that statement is false.  Before diving into ternary operators, let’s cover some basics about conditional statements.  

![](https://camo.githubusercontent.com/c8dcd2c8adeafdd3be5bec086d5d996c2454dc6d/687474703a2f2f746563682d6361726565722d626f6f737465722d636f75727365732e73332e616d617a6f6e6177732e636f6d2f30312d66756c6c2d737461636b2d7765622d646576656c6f7065722f73656374696f6e732f31312d70726f6772616d6d696e672d776974682d727562792f63686170746572732f30372d636f6e646974696f6e616c2d616e642d6c6f676963616c2d6f70657261746f72732d616e642d70726f6772616d2d666c6f772d636f6e74726f6c2f6173736574732f696d616765732f69662d656c73652d656e642d626c6f636b2e6a7067)
*Simple Diagram of a Ruby Conditional Statement*

## Conditional Statements

A [conditional statement](https://www.rubyguides.com/ruby-tutorial/ruby-if-else/) in the simplest of terms is a line of code that will evaluate a value to see whether it is true or false and in each case, will run the given code based on the outcome of that evaluation.  First, let’s define the following in Ruby: 

* **Booleans:** a logic statement or value that evaluates to either true or false
* **Truthy:** anything that evaluates to true
* **Falsey:** *false* and *nil* are the only flasey values in Ruby

If you’re still having trouble understanding these concepts, you can [read more here](https://www.rubyguides.com/2019/02/ruby-booleans/).

Let’s take a look at a basic Ruby if/else statement.  In this example, we’ve written a Ruby method that lets us know whether to buy more apples or to eat an apple based on the number of apples we currently have.

```
def apple_shopper(apples)
  if apples < 1 
    "buy more apples" 
  else 
    "eat an apple"
end

apples = 3
apple_shopper(apples)
# =>eat an apple

apples = 0
apple_shopper(apples)
# => buy more apples
```

With the magic of the ternary operator, this conditional statement can be written in one line of code as follows:

```
def apple_shopper(apples)
  apples < 1 ? "buy more apples" : "eat an apple"
end

apples = 3
apple_shopper(apples)
# =>eat an apple

apples = 0
apple_shopper(apples)
# => buy more apples
```

Simple, neat, concise!  The basic format to follow when using ternary operators is as follows:

                              (condition) ? (true_return_value) : (false_return_value)

We have a conditional statement (the statement that is either going to be true or false), followed by a question mark *‘?’*. We then enter the return value if the conditional is true, which is followed by a colon *‘:’*. Lastly, we enter our return value if the condition is false.

Ternary operators are great to get familiar with, but do keep in mind that there are instances where it may be better to write out the conditional statement the long way.  This is especially true if your conditional statement is more complex and has many conditions to evaluate.  In those cases, ternary operators will not work or may even make your code more difficult to understand.  But when you have a simple if/else conditional, using the ternary operator is considered best practice.

That’s all for this week.  I’ll be back soon with more Ruby tips and tricks.  Until then, happy coding!

