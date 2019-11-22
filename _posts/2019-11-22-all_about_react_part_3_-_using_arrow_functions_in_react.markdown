---
layout: post
title:      "All About React: Part 3 - Using Arrow Functions in React"
date:       2019-11-22 17:03:46 -0500
permalink:  all_about_react_part_3_-_using_arrow_functions_in_react
---


This month, I’ll cover new topics related to React each week.  In the [first post](http://crackingthecode.net/all_about_react_part_1_-_the_virtual_dom) in this series, we took a look at one of the features that makes React so popular: the **Virtual DOM**.  In the [second post](http://crackingthecode.net/all_about_react_part_2_-_lifecycle_methods), we covered **lifecycle methods** and how they’re used in React.  In this week’s post, I’ll talk about how to use arrow functions in your React code.

## Scrimba.com

I recently started a new online course on [Scrimba](https://scrimba.com/) that covers some advanced React features.  I was excited to take this course because a lot of the features covered are new enough that they weren’t covered in depth during my Flatiron curriculum.  

If you haven’t tried out Scrimba, I highly recommend it as supplementary learning material to your bootcamp curriculum.  They have lots of free courses in React, JS, CSS, HTM and more.  And their learning platform is one of the best I’ve used online.  You can pause their video lessons and edit in sandbox mode at any time.  It’s an amazing feature and a great way to practice.  I like their courses so much that this is the second paid one I've purchased.  In this week's post, I want to cover a couple neat things I learned from my new course about using arrow functions in your React code.

## Using Arrow Functions

One thing that can get confusing for new devs is keeping up with all the updates and new features with the languages and frameworks we’re learning.  It’s taken me some time and practice to help get used to all the [new features](http://es6-features.org/#Constants) introduced with JS ES6.  One new feature is the [arrow function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions), and while I have used it while writing JS, I didn’t use it when I worked on my final project in React.  I used to find the arrow function a bit confusing, but as you get used to it, you can see some of the benefits to using it.  Let’s take a look at a few examples.

![](https://scotch-res.cloudinary.com/image/upload/w_auto,q_auto:good,f_auto/v1561344201/tbepoamnyxtlx8soszhd.png)

Before these updates, if we wanted to write out a simple function that renders “Hello World!,” it might look something like this:

```
function App() {
    return (
        <p>Hello World!</p>
    )
}
```
Now, we can simplify this function slightly using arrow functions as follows:

```
const App = () => (
    <p>Hello World!</p>
)
```

The new method is slightly simpler and it gets rid of those annoying curly brackets.  You can also use arrow functions when writing class methods in React.  For example, if I wanted to write a method that increments a counter, it might look something like this:

```
increment() {
        this.setState(prevState => {
            return {
                count: prevState.count + 1
            }
        })
}
```

This becomes much simpler when using the arrow function:

```
increment = () => {
        this.setState(prevState => ({count: prevState.count + 1}))
}
```

That’s much better, isn’t it?  Three key things to notice here:
1. Arrow functions have a lexical ```this```, meaning that you won’t need to write a binding statement as part of the constructor method.  
2. Arrow functions have an implicit return, so we can remove the return key word all together if we write our return value on the same line as the arrow.  
3. Because the return statement here is an object within curly brackets, we need to wrap the object in parentheses as well.

## BONUS: Simplify Your Class Constructor Method

One bonus feature of using arrow functions as detailed above is that you can also now simplify your class constructor method.  Because the arrow functions replace the need to bind your ```this``` value, there's no need for the constructor at all.  

Here is an example of a constructor method for our increment button.  In our constructor, we will set our state with a counter value of 0.  I have also included a statement that will bind the value of ```this```.

```
constructor() {
        super()
        this.state = {
            count: 0
        }
        this.increment = this.increment.bind(this)
 }
```

When using arrow functions, you don't need that binding statement at all.  In fact, you can get rid of the constructor all together and declare your state as follows:

```
state = {
        count: 0
}
```

See?  Much better!  And all thanks to that arrow function!  

This concludes my brief overview of using arrow functions in React.  They can take some getting used to, but as you can see, there are definitely benefits to using them.  Thanks for reading.  I’ll be back next week with some new React related content.  Until then, Happy Coding!



