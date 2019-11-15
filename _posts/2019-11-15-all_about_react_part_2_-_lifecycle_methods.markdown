---
layout: post
title:      "All About React: Part 2 - Lifecycle Methods"
date:       2019-11-15 12:23:54 -0500
permalink:  all_about_react_part_2_-_lifecycle_methods
---


This month, I’ll cover new topics related to React each week.  In the [first post](http://crackingthecode.net/all_about_react_part_1_-_the_virtual_dom) in this series, we took a look at one of the features that makes React so popular: the **Virtual DOM**.  In this week’s post, we’ll look at the **lifecycle methods** and how they’re used in React.  

## React Lifecycle Phases

As a former STEM teacher, I’ve created many lessons to teach students about plant or animal lifecycles.  Just as a frog goes from egg to tadpole to adult frog, so too our components in a React application go through different phases.  These phases are commonly referred to as **mounting**, **updating**, **unmounting** and **error handling**.  Each of these phases has methods available, some of which can prove quite useful, while others are rarely used.  If you’re new to React, I’d recommend reading through the [official docs](https://reactjs.org/docs/state-and-lifecycle.html) to make sure you understand **[state](https://www.w3schools.com/react/react_state.asp)** and **[lifecycles](https://www.w3schools.com/react/react_lifecycle.asp)**.  

One note before we get started: React’s lifecycle methods have gone through some changes recently with the React 16 update.  It has been determined that some of the older lifecycle methods are not safe to use.  Those methods will be deprecated in React 17.  In this blog post, we focus on the most commonly used methods and will not learn about the soon to be deprecated unsafe lifecycle methods.  With that out of the way, let’s take a look at each phase in a React component’s lifecycle.

![](https://i0.wp.com/storage.googleapis.com/blog-images-backup/1*rubjO6t-iBoNjS_K1rOkzQ.png?zoom=1.25&resize=730%2C468&ssl=1)
*Diagram of React lifecycle Phases*

### The Mounting Phase

The mounting phase is the first phase in a React component’s lifecycle.  Here, we’re bringing our component to life for the first time.  

### The Updating Phase

As a React component grows, or gets updated, there are lifecycle methods available to us here as well.  

### The Unmounting Phase

The final phase, or unmounting, is where the component “dies,” or is removed from the [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)

### The Error Handling Phase

The error handling phase runs throughout all three phases above.  It’s important to note that not all React components will go through all the above phases or use all the available lifecycle methods.  For example, you may have a React component that mounts, has no updates or errors, and then unmounts.  

Let’s look at the most commonly used lifecycle methods.

![](https://miro.medium.com/max/1200/1*552z6hbX_b648DjpTLHZNg.png)
*Diagram of React 16 Component Lifecycle Methods*

## Common React Lifecycle Methods

### constructor()

The **constructor()** method is a commonly used method and usually the first one called upon in the React component lifecycle.  The constructor method is called before the component is mounted to the DOM.  This method is commonly used to initialise state and bind event handlers methods.

Here’s a quick example:

```
const MyComponent extends React.Component {
  constructor(props) {
   super(props) 
    this.state = {
       points: 0
    }  
    this.handlePoints = this.handlePoints.bind(this) 
    }   
}
```

### render()

The most commonly used lifecycle method is the **render()** method.  You will see it in all React classes because it’s the only required method within a class component in React.  As the name suggests, it handles the rendering of your component to the UI.  It occurs during the mounting and updating of your component.

Let’s look at a simple example of render() in React:

```
class Hello extends Component{
   render(){
      return <div>Hello {this.props.name}</div>
   }
}
```
A render() method has to be a **[pure function](https://en.wikipedia.org/wiki/Pure_function)** with no side-effects.  Pure functions are those that will always return the same output when the same inputs are passed. This means that you can not setState() within a render() method.  There are other methods available to set or modify state, thus keeping the render() method pure.  

### componentDidMount()

Once your component has mounted and is ready, the next React lifecycle method  that comes into play is **componentDidMount()**.  This method is called as soon as the component is mounted and ready. This is a good place to initiate API calls if you need to load data from a remote endpoint.

Unlike the render() method, componentDidMount() allows the use of setState(). Calling the setState() here will update state and cause another rendering but it will happen before the browser updates the UI. This is to ensure that the user will not see any UI updates with the double rendering.  

But even though you can call setState() here, it is not recommended because it can lead to performance issues or other unexpected bugs.  Instead, it is considered best practice to use the setState() method as past of the constructor() method.  

### componentDidUpdate()

This lifecycle method is invoked as soon as the updating happens. The most common use case for the componentDidUpdate() method is updating the DOM in response to prop or state changes.

Here is a common use example:

```
componentDidUpdate(prevProps) {
 //Typical usage, don't forget to compare the props
 if (this.props.userName !== prevProps.userName) {
   this.fetchData(this.props.userName);
 }
}
```

Notice in the above example that we are comparing the current props to the previous props. This is to check if there has been a change in props from what it currently is. In this case, there won’t be a need to make the API call if the props did not change.

### componentWillUnmount()

As the name suggests this lifecycle method is called just before the component is unmounted and destroyed. If there are any cleanup actions that you would need to do before unmounting, they can be performed here.

You cannot modify the component state in componentWillUnmount() lifecycle method.  This component will never be re-rendered and because of that we cannot call setState() during this lifecycle method.

This concludes my brief overview of commonly used React lifecycle methods.  Keep in mind that there are other lifecycle methods available as well.  If you’d like to go deeper into this topic, you can try reading the blog posts [here](https://blog.bitsrc.io/react-16-lifecycle-methods-how-and-when-to-use-them-f4ad31fb2282) and [here](https://medium.com/@nancydo7/understanding-react-16-4-component-lifecycle-methods-e376710e5157).  I’ll be back next week with some new React related content.  Until then, Happy Coding!

