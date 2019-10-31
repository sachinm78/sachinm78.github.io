---
layout: post
title:      "Hello Ruby, My Old Friend: Part 4 - The Splat Operator"
date:       2019-10-31 15:59:27 -0400
permalink:  hello_ruby_my_old_friend_part_4_-_the_splat_operator
---


This month, I’m revisiting an old friend, Ruby, and covering topics related to Ruby and Rails. In the [1st post in this series](http://crackingthecode.net/hello_ruby_my_old_friend_part_1_-_separation_of_concerns_and_mvc), I covered the **Separation of Concerns (SoC)** Principle and **MVC Architecture**. In [part 2](http://crackingthecode.net/hello_ruby_my_old_friend_part_2_-_using_ternary_operators), I discussed how to use a **ternary operator** in place of simple if/else conditional statements.  In [part 3](http://crackingthecode.net/hello_ruby_my_old_friend_part_3_-_array_set_operators), I covered using **Set Operators**.  This week, in my final post in this series, I’ll cover one more trick I’m starting to use: **the Splat Operator**

## The Splat Operator

In Ruby, the **Splat Operator** is represented by the `*` symbol.  There are many different ways it can be used, but I will focus on some of the common use cases.  Some of these uses may be quite familiar to seasoned devs, but I definitely learned something new while researching to write this post.  Let’s start with a basic example and work our way up from there.

## Single Splat

One of the common use cases for the single splat operator is when you don’t want to specify or are unsure of the number of arguments a method will take.  For example, let’s say we want to write code that greets members in a chat group, but we don’t know how many members will join.  We can use the splat operator to help us!

```
def greeting(*people)
     people.each{|person| puts "Hello, #{person}!"}
end
 
greeting("Amy", "Bob", "Chris")

=> Hello, Amy!
=> Hello, Bob!
=> Hello, Chris!
```

In the example above, `*people` will capture all the arguments you pass into the greeting method.  This is definitely handy when defining a method with an unknown number of possible arguments, but did you know you can use a similar trick when calling a method as well?  

In this example, we have a list of people and we want to call our greeting method on all of them.  

```
people = ["Dan", "Ellen", "Frank"]
 
greeting(*people)

=> Hello, Dan!
=> Hello, Ellen!
=> Hello, Frank!
```

Works like a charm!  And believe it or not, there's actually a lot more you can do with splats.  One fun example I found is for assigning variables in an array.  Say that you want to assign the first element in an array to one variable and the rest to another:

```
arr = [1, 2, 3, 4, 5]
first, *rest = arr

first
=> 1 

rest
=> [2, 3, 4, 5]
```

That’s a cool little trick that was new to me.  So as you can see, the splat operator is pretty handy.  But it gets better.  Let’s double up the fun!

## Double Splat

The double splat is represented by two `**` symbols.  It works very similarly to the single splat operator with one main difference: it can be used on hashes!  Let’s say we wanted to save a hash with the names and ages of the people in our chat group from above.  We could do something like this:

```
def name_and_age(**hash)
     hash
end
 
name_and_age(Alice: 24, Bob: 31, Carl: 26)
=> {:Alice=>24, :Bob=>31, :Carl=>26}

OR
 
hash = {Dan: 37, Ellen: 32, Frank: 21}

name_and_age(hash)
=> {:Dan=>37, :Ellen=>32, :Frank=>21}
```

Here, the “key: value” arguments we pass into the method will save them in a hash.  This might not seem very useful since you could just write out the hash normally, but if you don’t know the number of arguments, then try the double splat method.

This concludes my brief introduction to the splat operator.  If you’d like to go deeper into this topic, you can try reading the blog posts [here](https://alexcastano.com/everything-about-ruby-splats/) and [here](https://www.honeybadger.io/blog/ruby-splat-array-manipulation-destructuring/).  I hope you found this post useful and that you enjoyed this month’s return to Ruby.  I’ll be back next week with some new content.  Until then, Happy Coding!

