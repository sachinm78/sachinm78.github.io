---
layout: post
title:      "Hello Ruby, My Old Friend: Part 3 - Array Set Operators"
date:       2019-10-24 17:15:26 +0000
permalink:  hello_ruby_my_old_friend_part_3_-_array_set_operators
---


This month, I’m revisiting an old friend, Ruby, and covering topics related to Ruby and Rails. In the [1st post in this series](http://crackingthecode.net/hello_ruby_my_old_friend_part_1_-_separation_of_concerns_and_mvc), I covered the **Separation of Concerns (SoC)** Principle and **MVC Architecture**. In [part 2](http://crackingthecode.net/hello_ruby_my_old_friend_part_2_-_using_ternary_operators), I discussed how to use a **ternary operator** in place of simple if/else conditional statements.  This week, I’ll cover something I recently learned about and found very useful when working with arrays: **Set Operators**.

## The Set Class

If you’ve been writing Ruby for a while, you’re probably very familiar with data collections such as [*arrays*](https://ruby-doc.org/core-2.4.1/Array.html) or [*hashes*](https://ruby-doc.org/core-2.5.1/Hash.html).  But there is another data collection that isn’t as well known: the **[Set Class](https://www.rubyguides.com/2018/08/ruby-set-class/)**.  In Ruby, sets are unordered collections of unique objects.  According to the official docs, sets are a “hybrid of Array's intuitive inter-operation facilities and Hash's fast lookup.”  

And sets come with some unique and helpful operators to manipulate the data inside.  And lucky for us, most of these methods can be used with arrays as well.  Let’s look at some of the most useful **Set Operators**.

## Set Operators

As you may have noticed from the documentation on the *[Set Class](https://ruby-doc.org/stdlib-2.6.5/libdoc/set/rdoc/Set.html)*, there are a lot of useful operators available to use.  Let’s look at three of the most common and useful **Set Operators**:

## Union   |

The **union operator** *combines* the unique values of two sets.  To perform a union on two arrays you use the* pipe “|”* as an operator. For example:

```
[1, 2, 3] | [4, 5, 6]
=> [1, 2, 3, 4, 5, 6]

[1, 2] | [2]
=> [1, 2]
```

## Intersection   &

The **intersection operator** returns the elements that are *common* in both sets.  It uses the *ampersand “&”* symbol.   Let’s look at an example:

```
[1, 2, 3] & [3, 4]
#=> [3]

[1, 2] & [3, 4]
#=> []
```

## Difference   -

The **difference operator** returns the difference *between* two sets, and uses the *minus “-”* symbol.  Here’s an example:

```
[1, 2, 3] - [2, 3]
#=> [1]

[1] - [1]
#=> []
```

What’s on the left side of the difference operator is important. It takes elements on the left (in our case the elements in the array) and compares them to the elements on the right; and the elements that are different are returned.

As you can see, the Set Operators above can be very useful when working with multiple arrays of data.  The three I’ve covered here are only a few of the handy Set Operators available.  I’ll leave you with one last example of an interesting method used on arrays.

## 42 Or “The Reddit Method”

If you’re a fan of the classic sci-fi series *“The Hitchhiker’s Guide to the Galaxy,”* then you’re probably familiar with the significance of [the number 42](https://en.wikipedia.org/wiki/42_(number)).  And as devs are known to be quirky, it shouldn’t be too surprising that the creators of Rails would add a method to find the 42nd element in an array.  This method is also known as “[the Reddit Method](https://www.quora.com/Why-is-Array-forty_two-called-the-reddit-in-Ruby-on-Rails).”   

```
arr[41] # is equivalent to... 

arr.forty_two
```

While it may not provide the answers to the universe, it’s still quite amusing to know that this method exists and how it came to be!  

That’s all for this week.  I hope you’ve found this brief introduction to **Set Operators** useful.  I’ll be back soon with more useful Ruby tips and tricks.  Until then, Happy Coding!

