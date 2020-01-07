---
layout: post
title:      "All About React: Part 4 - Get Hooked on Hooks!"
date:       2020-01-07 21:13:07 +0000
permalink:  all_about_react_part_4_-_get_hooked_on_hooks
---


*Author’s note: Sorry for the delay between posts!  It was a busy holiday season of balancing quality time with family and learning new tricks in React.  I’m finally ready to share some of what I’ve learned.  To finish off this section on React, let’s get hooked on hooks!*

This month, I’ll cover new topics related to React each week.  In the [first post](http://crackingthecode.net/all_about_react_part_1_-_the_virtual_dom) in this series, we took a look at one of the features that makes React so popular: the **Virtual DOM**.  In the [second post](http://crackingthecode.net/all_about_react_part_2_-_lifecycle_methods), we covered **lifecycle methods** and how they’re used in React.  In the [third post](http://crackingthecode.net/all_about_react_part_3_-_using_arrow_functions_in_react), we discussed the advantages of using **arrow functions** in your React code.  In the final post for this section, I’ll talk about how to manage state in React using **hooks**.

## An Intro to State in React

One of the challenges all React devs will face is how best to manage state in their React apps.  This challenge is something you will also struggle with whether you are a seasoned dev or just starting your learning journey.  For those of you who are new and maybe struggling to understand this issue, here are a few helpful links you should read before continuing this post:

*What is state?* Here is the [official React documentation on state](https://reactjs.org/docs/faq-state.html).  You can also see a simple explanation by W3Schools [here](https://www.w3schools.com/react/react_state.asp).

Here is a helpful blog post that covers this topic in simple terms: A [beginner’s guide to state management](https://dev.to/dylanmesty/reactjs-state-management-a-beginner-s-perspective-35f3) in React

## State Management in React

There are many options for managing the state of your data in React.  It would take multiple blog posts to cover them all in detail, but two common options are [Redux](https://react-redux.js.org/introduction/why-use-react-redux) and the new [Context API](https://reactjs.org/docs/context.html) included with the latest React updates.

Both of these options have their pros and cons, which are covered quite well in [this post](https://medium.com/dailyjs/comparison-of-state-management-solutions-for-react-2161a0b4af7b).  But where they helped to solve some of the problems with state management, they have their limitations and can also introduce new challenges of their own.  I can speak from example.  For my final project as part of my coding bootcamp, I was tasked with using Redux to manage state in my React project.  I found it to be often confusing and repetitive, making what could have been simple code far more complex than necessary, all to pass data from one component to another without breaking your app.  

Additionally, Redux actually requires a middleware called [Thunk](https://github.com/reduxjs/redux-thunk) for it to be of any use to manage state properly with a complex app.  In the end, while I finished my project, I thought to myself that there must be a better way to pass data from one component to the next.  Thankfully, the devs at React had a solution that would vastly simplify this issue: enter **React Hooks**!

## Hooks to the Rescue!

With the introduction of [Hooks](https://reactjs.org/docs/hooks-intro.html) with React 16.8, state management in your apps got a lot simpler.  From the React docs on Hooks, “Hooks are functions that let you “hook into” React state and lifecycle features from function components. Hooks don’t work inside classes — they let you use React without classes.”  That means you can write *functional components*, which are simpler than *class components*, and still manage the state of your data!  Also, functional components don’t need a render method, so they tend to be more concise to write.  If these topics are new or confusing to you, here is the React doc for [components and props](https://reactjs.org/docs/components-and-props.html). 

## Common Hooks in React

There are a lot of hooks that were added by the React team.  You can even create your own custom hooks if needed.  To keep this post manageable, let’s look at two that will be commonly used and how they work, *useState* and *useEffect*.

### useState

The *useState* hook is going to be the most commonly used because it allows you to easily set state and pass state from one component to another.  The React docs on hooks linked above do a far better job than I could of describing how hooks work.  But what I found helpful is seeing the difference between a class component set up to manage state and how it would look as a functional component using the useState hook.  

So, here is a simple class component that will render a question and the answer, which will be derived from state.  

```
import React from "react"

class App extends React.Component {
    constructor() {
        super()
        this.state = {
            answer: "Yes"
        }
    }
    
    render() {
        return (
            <div>
                <h1>Are you hooked on Hooks? {this.state.answer}</h1>
            </div>
        )
    }
}

export default App
```

Here, we have a simple constructor method that initializes our state to have the answer to our question `“Are you hooked on Hooks?”` set to `“Yes”`.  Let’s look at what this same code would look like using the useState hook:

```
import React, {useState} from "react"

function App() {
    const [answer] = useState("Yes")
    return (
        <div>
            <h1>Is state important to know? {answer}</h1>
        </div>
    )
}
```

Here, we have imported the `useState` hook from the React library.  We then can create a variable `[answer]` and apply the useState hook to set the value we desire, in this case `“Yes”`.  Remember, functional components don’t require a render method like class components, so all we need to do is return our `<div>` and use the variable we created `{answer}` to handle our state.  Note that `const [answer]` is using [array destructuring](http://www.react.express/destructuring) so that we don’t have to write `{answer[0]}` in our `h1`.  As you can see, our code becomes much more concise and simpler to follow using hooks!  Keep in mind that this is a very simple example with our answer hardcoded to `“Yes”`.  But it’s also very simple to implement dynamic code so that you can assign the answer based on user input or whatever your code requires.  

### useEffect

One more hook you’re likely to encounter often is the *useEffect* hook.  This hook was created to simplify how we use [lifecycle methods](https://reactjs.org/docs/state-and-lifecycle.html) in React.  A simpler way to look at useEffect is to think of it as something that allows us to produce side effects in our component.  For example, when you have event listeners or an `onClick` function, we can use useEffect to simplify our code.  

Let’s look at a simple example of a counter.  In the following code, we have a counter that was built using the useState hook.  It has a simple increment and decrement method to increase or decrease the counter value with the click of a button.  

```
import React, {useState} from "react"

function App() {
    const [count, setCount] = useState(0)
    const [answer, setAnswer] = useState("Yes")
    
    function increment() {
        setCount(prevCount => prevCount + 1)
    }
    
    function decrement() {
        setCount(prevCount => prevCount - 1)
    }
    
    return (
        <div>
            <h1>{count}</h1>
            <button onClick={increment}>Increment</button>
            <button onClick={decrement}>Decrement</button>
        </div>
    )
}

export default App
```

Let’s say we wanted the counter color to change to a random color every time the user clicks one of the buttons.  With useEffect, this is simple enough to implement.  In the following code, we had installed the `randomcolor` dependency from the npm library (type `npm install randomcolor` into your console).  We can use this in our code with useEffect to have our counter display a new random color every time our state changes.  Let’s look at the code:

```
import React, {useState, useEffect} from "react"
import randomcolor from "randomcolor"

function App() {
    const [count, setCount] = useState(0)
    const [color, setColor] = useState("")
    
    function increment() {
        setCount(prevCount => prevCount + 1)
    }
    
    function decrement() {
        setCount(prevCount => prevCount - 1)
    }
    
    useEffect(() => {
        setColor(randomcolor())
    }, [count])
    
    return (
        <div>
            <h1 style={{color: color}}>{count}</h1>
            <button onClick={increment}>Increment</button>
            <button onClick={decrement}>Decrement</button>
        </div>
    )
}

export default App
```

Here, we have imported the `useEffect` hook from the React library along with our `useState` hook.  We have also imported `randomcolor` to use in our app.  Next, in our state, we have created new variables, `color` and `setColor`, to manage the state of our counter.  We have initialized the color to be an empty string `“”`.  Next, we created a very simple function using the useEffect hook, which takes a function as an argument.  Here, we have used our setColor variable and randomcolor to change our counter value’s color.  We are also passing our `[count]` variable to this function.  Finally, we have added a `style` tag to our `<h1>` to set the color of our count value.  

This may be a bit confusing to follow if you’re new to hooks. Just know that before hooks, this simple addition of a random color effect could have created a real headache to implement by using multiple lifecycle methods.  Thankfully, hooks makes adding effects to your code far simpler! 

That concludes this brief intro into the world of React hooks.  I hope you’re as hooked to hooks as I am.  They really are a game-changer as far as state management goes in React.  There are tons of amazing resources to learn more about hooks.  As always, the best place to start is the official React docs I’ve included above.  If you’re interested in learning more about hooks and state management in React,here are a few blog posts I have found useful:

Blog: [State of React State Management For 2019](https://blog.bitsrc.io/state-of-react-state-management-in-2019-779647206bbc)

Blog: [State Management With React Hooks](https://medium.com/javascript-in-plain-english/state-management-with-react-hooks-no-redux-or-context-api-8b3035ceecf8)

Blog: [State Management Using Only React Hooks](https://blog.logrocket.com/state-management-using-only-react-hooks/)

Blog: [Global State Management Using React Hooks And Context](https://dev.to/vanderleisilva/global-state-management-with-react-hooks-and-context-5f6h)

Thanks for reading.  Check back soon for more new content.  Until then, happy coding!

