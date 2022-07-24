# React-Design-Patterns
React: Design Patterns

## Introduction
- [Take your React skills to the next level](#take-your-react-skills-to-the-next-level)
- [What should know](#what-should-know)
- [What are design patterns?](#what-are-design-patterns?)

## 1. Layout Components
- [What are layout components?](#what-are-layout-components?)
- [Split-screen components](#split-screen-components)
- [Split-screen component improvements](#split-screen-component-improvements)
- [List and list items](#list-and-list-items)
- [Creating different list types](#creating-different-list-types)
- [Modal components](#modal-components)

## 2. Container Components
- [What are container compoent](#what-are-container-component)
- [Server Instructions](#server-instructions)
- [CurrentUserLoad component](#currentuserload-component)
- [UserLoader component](#userloader-component)
- [ResourceLoader component](#resourceLoader-component)
- [DataSource component](#dataSource-component)
- [Loading data from localStorage](#Loading-data-from-localStorage)

## 3. Controlled adnd Uncontrolled Component
- [Controlled vs. uncontrolled components](#controlled-vs-uncontrolled-components)
- [Uncontrolled forms](#Uncontrolled-forms)
- [Controlled modals](#controlled-modals)
- [Uncontrolled onboarding flows](#uncontrolled-onboarding-flows)
- [Collecting onboarding data](#collecting-onboarding-data)
- [Controlled onboarding flows](#controlled-onboarding-flows)

## 4. Higher-Order Components
- [What are higher-order components?](#what-are-higher-order-components?)
- [Printing props with HOCs](#printing-props-with-HOCs)
- [Loading data with HOCs](#loading-data-with-HOCs)
- [Modifying data data HOCs](#modifying-data-data-HOCs)
- [Creating forms with HOCs](#creating-forms-with-HOCs)
- [Higher-order component improvements](#higher-order-component-improvements)

## 5. Custom Hooks Patterns
- [What are custom Hooks?](#what-are-custom-hooks?)
- [useCurrentUser Hook](#usecurrentUser-hook)
- [useUser Hook](#useuser-hook)
- [useResource Hook](#useResourcepHook)
- [useDataSource Hook](#usedataSource-hook)

## 6. Functional Programming and React
- [What is functional programming?](#what-is-functional-programming?)
- [Recursive components](#recursive-components)
- [Component composition](#Component-composition)
- [Partially applied components](#partially-applied-components)

## Conculation
- [Next steps](#next-steps)


### Take your React skills to the next level
Maybe you're learned the basics of React and are wondering where to go next.<br>

Or maybe you're looking to make Reactt development more intuitive for your self so that you can build anything you can imagine.<br>

Well, whatever the case, learning and mastering React design patterns might just be the way to take your software development career to another level. <br>

I'am Uzzal Roy, and I'am a senior software developer and tech educator.<br>

The topics in this course represent many of the things that I look for when interviewing React developer candidates.<br>

Things that will take you from a begineer or intermediate level to an advanced level in React.<br>

Join me this course to learn React's most important design patterns, and see how to take your productivity and intuition in React to the next level.

### What should know
In order to get the most out of this course, there are a few things that it would be helpful for you to know beforehand.<br>

##### What You Should Already Know
- React basics
- React Hooks
- Making network requests in React
- Functinal programming(not required)

The first thing that it would be helpful for you to have is a basic experience with React, right? <br>

Just knowing the basics behind how to React works should be sufficent.<br>

You should also have some experience with React Hooks.<br>

Now, hooks being a more recent addition to the React Library.<br>

You might want to brush up on these before you start this course, since we'll be talking about those in detail.<br>

It would also be helpful for you to have some experience making network requests in React.<br>

And for this, if you haven't seen this already, I hight recommend my course on Full Stack Development with React.<br>

And finally, a little bit of experience with functional programming would be very helpful, but this is not something that's required for this course. <br>

So if you're missing one or more of these prerequisites, feel free to brush up on those beforehand. Otherwise let's get going.

### What are design patterns?
We're going to be learning quite a few different React design patterns, but before we get into that, I wat to talk a little bit about what design patterns are in the first place.<br>

#### Design Patterns:<hr>
Design patterns are effective solutions to common application development challenges.<br>

So the definition that I've come up with for design patterns is that design patterns are effective solutions to common application development challenges. <br>

And notice here that i have effective underlined, because there are a lot of solutions to different problems that are not effective and that lead to more brittle code down the line and make your apps less performant and less maintainable.<br>

Those are generally referred to as anti-patterns. <br>

So design patterns are the positive equivalent of thouse, right? <br>

So in other words, they're that most effective solutions to a given development challenge. <br>

We'll see what I mean later on in the course. <br>

#### A Caveat<hr>
The design patterns we talk about in this course are not the Gang of Four OOP design patterns.<br>

Now, one caveat before we move on is that many of you may have heard of design patterns used in a different context, such as object oriented programming. <br>

Well, the design patterns that we're going to be talking about in this course are not those. <br>

In other words, they're not the so-called Gang for Four object oriented programming design patterns, such as creational, behavioral patterns, et cetera. <br>

There's something a little bit different. <br>

- The patterns we cover here are effective solutons to some extremely common challenges in React.

Basically the patterns that we're going to be covering here are things that I've personally run into time and time again in basically every React application I;ve worked on. <br>

#### Common Challenges
- Creating reusable layouts

Some of these challenges include things like creating reusable layouts to put our components into, right? <br>

We'll see later on how to make things <br>

- Reusing complex logic between multiple components

Another challenge is how do we reuse complex logic between our component? <br>

In other words, if we have two or more components that need to do the same complex things such a load data from a server, <br>
how do we best represent that in our React apps so that <br>
we can share that code between those components<br>
instead of having to copy and paste it.<br>

- Working with forms

Another extremely common challenge is working with forms in React.<br>

This something that despite hundreds of articles out there on how to do this currectly, I still see done incorrectly quite frequently.<br>

So we'll be discussing how to do that in React.<br>

- Incorporating functional concepts into our code

And finally, we're going to see from functional programming into our React apps. <br>

This is something that I've been asked about quite frequently since my functional programming courses. <br>

And Im very excited to share it with you in this course. <br>

Well, those are some of the common challenges we're going to be taking a look at. <br>

So let's jump right into the first pattern.

### What are layout components?
### Split-screen components
### Split-screen component improvements
### List and list items
### Creating different list types
### Modal components

### What are container compoent
### Server Instructions
### CurrentUserLoad component
### UserLoader component
### ResourceLoader component
### DataSource component
### Loading data from localStorage

### Controlled vs. uncontrolled components
### Uncontrolled forms
### Controlled modals
### Uncontrolled onboarding flows
### Collecting onboarding data
### Controlled onboarding flows

### What are higher-order components?
### Printing props with HOCs
### Loading data with HOCs
### Modifying data data HOCs
### Creating forms with HOCs
### Higher-order component improvements

### What are custom Hooks?
### useCurrentUser Hook
### useUser Hook
### useResource Hook
### useDataSource Hook

### What is functional programming?
### Recursive components
### Component composition
### Partially applied components

### Next steps
