# React-Design-Patterns
React: Design Patterns

## Introduction
- [Take your React skills to the next level](#take-your-react-skills-to-the-next-level)
- [What should know](#what-should-know)
- [What are design patterns?](#what-are-design-patterns)

## 1. Layout Components
- [What are layout components?](#what-are-layout-components)
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
- [Loading data from localStorage](#loading-data-from-localStorage)

## 3. Controlled adnd Uncontrolled Component
- [Controlled vs. uncontrolled components](#controlled-vs-uncontrolled-components)
- [Uncontrolled forms](#Uncontrolled-forms)
- [Controlled modals](#controlled-modals)
- [Uncontrolled onboarding flows](#uncontrolled-onboarding-flows)
- [Collecting onboarding data](#collecting-onboarding-data)
- [Controlled onboarding flows](#controlled-onboarding-flows)

## 4. Higher-Order Components
- [What are higher-order components?](#what-are-higher-order-components)
- [Printing props with HOCs](#printing-props-with-HOCs)
- [Loading data with HOCs](#loading-data-with-HOCs)
- [Modifying data data HOCs](#modifying-data-data-HOCs)
- [Creating forms with HOCs](#creating-forms-with-HOCs)
- [Higher-order component improvements](#higher-order-component-improvements)

## 5. Custom Hooks Patterns
- [What are custom Hooks?](#what-are-custom-hooks)
- [useCurrentUser Hook](#usecurrentUser-hook)
- [useUser Hook](#useuser-hook)
- [useResource Hook](#useResourcepHook)
- [useDataSource Hook](#usedataSource-hook)

## 6. Functional Programming and React
- [What is functional programming?](#what-is-functional-programming)
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
We're going to talk about are something called layout components. <br>

#### Layout Components
React components that deal primarily with arranging other components on the page. <br>

Let's start off with a definition here Layout components are components in React whose primary concern is helping us to arrange other components that we create on the page. <br>

Some examples of this that you're probable familiar with, and that we're going to be taking a look at throughout the rest of this chapter are splite screens, right?

#### Layout Component Examples

- Splite Screens

So arranging more than one component in different sections of the page. <br>

- Lists and Items

We also have lists and items, right? So display data in a list, this is a surprisingle hard thing to get completely right. <br>

- Modals

And Modals, which as most of you know, is just content that gets displayed over top the actual page. <br>

#### The Idea of Layout Component

```
<div styles={...}>
    <h1>Component Code...</h1>
</div>
```
So here's the basic idea of layout components and how we're going to go about creating them. <br>

Normally, when we create a component, let's say we're creating a side nagivation for out site, right? <br>

Just a bar on the left-hand side that contains some links. <br>

The normal way we would go about doing that, as you can see in this code on theleft, is by actually including the div and the styles that go with that side nav inside the component itself. <br>

```
<div styles={...}>
    {children}
</div>
```

However, with layout components, what we do is splite the actual layout styles into the their own component, and then simply display the component itself, in this case, the side nav, inside that layout component. <br>
```
<>
    <h1>Component Code...</h1>
</>
```
And what this does is it separates the component itself from where the component's being displayed on the page, and it gives use a lot more flexibility for how we use it in the feture. <br>

#### The Idea of Layout Components
Out components shouldn't know where they're beign displayed. <br>

So with all that said, the main idea of layout components is that out components that we create, right, the main content components of out pages, shouldn't know or care where it is that they're actually being displayed on the page. <br>

So just keep that in mind that is the main idea of layout components.

### Split-screen components
- All right. 
So now that we know what basic layout components are, let's take a look at some good examples of this pattern. 
The first example we're going to take a look at here is creating a split screen using layout components. 
So we're going to start off this example with just a basic Create React App application. You can find this in the exercise files. Just make sure to run NPM install before using this. And the first thing we're going to do is for styling purposes, we're going to install a package called styled components. Now, I've talked about styled components in other courses of mine. If you're curious about those, feel free to look around the library for them. Essentially, styled components are just a very easy way to add styles to React components. You'll see what I mean in just a minute. So we're going to start off here by adding a new file that's going to contain our split screen layout component. So we're going to call this split screen dot JS, and here's what this component's going to look like. We're going to start off by defining the component itself. So we'll say export const split screen. And it's going to take a few props that will make sense in a minute. The first prop is going to be called left, and this is going to be the component that will be displayed on the left side of the split screen. And what we're going to do, just to keep in with React's convention of giving components capital letter names, we're going to actually rename this left prop to Left with a capital L. So that's why I'm doing that. And then we're going to do the same thing with right here. Okay? So we have two props, Left and Right, and that's all we need for now. So the body of our component now is going to be fairly simple. What we're going to do is return a div. Inside that div, we're going to have two other divs, which are going to be basically each side of our split screen, right? The left-hand side and the right hand side. And inside each of those, we're going to display the left- and right-hand components respectively. So we're going to say Left. Then we're going to do the same thing for the right-hand side by saying div, and putting a component called Right inside of there. All right. So currently all this does is wraps our left and right components inside some divs, so what we're going to need to do next is actually add some styles to those divs. Now, as I mentioned before, we're going to be using styled components for this. So let's import the styled components package, which works a little bit like this. We're going to say import styled from styled components. And then to use our styled components package to add styling to these divs, what we're going to do is add a new styled component called container. So we'll say const container equals styled dot div. And then inside back ticks, this is just the syntax that styled components uses to define its components, inside here we're going to define the styles that we want to apply to container. And that's going to look like this. All we're going to do is add display flex to it. And then under that, we're going to define another styled component called pane. This is going to be the styles that we apply to these two divs that are wrapping our Left and Right components. So we're going to say const pain equals styled dot div. We're going to use back ticks there as well. And for this one, the only style we're going to give it is flex one. Basically, that will make the left and right panes take up equal amounts of space. We'll see shortly how to make it so that we can change the amount of space that each side takes up. Okay, so now that we have our container and pane styled components, the way we add those to our split screen component is simply by replacing div with container... and pane. And we got to go through and change all of these to pane and container as well. Okay. So that's what that's going to look like now. And now that we've created our split screen component, let's see what it looks like displayed inside our app. So what we're going to do, again, this is just the starter code that Create React App provides us with. What we're going to do is just delete all of this inside of here, and just display our split screen component. So first, of course, we have to import it, and you can remove this logo and app dot CSS thing as well. We're going to import split screen from split screen. I'm just going to adjust the indentation there to fit my IDE. And then inside of here, we're going to say split screen. And then just to get an idea of how this works, we're going to pass two components, one to the left prop of our split screen, I'll show you what that looks like in a second, and one to the right prop. So for these left and right components, all we're going to do is inside our app component, we're going to define two very, very simple components. The first component we'll call left hand component. And what that's going to do is just return, I don't know, something like a H one heading that says left, and we'll do the same thing. We'll have a right-hand component... which is basically just going to return. We'll have it return a paragraph tag that says right. Okay. So now that we have our left-hand component and right-hand components, let's insert those into the left and right props. So we're going to say left-hand component... and right-hand component. And that should be all we need to do. So let's run this app by doing NPM run start, and again, make sure to run NPM install before you do this. And we should see that this opens up local host 3000 in our browser. And we see that sure enough, we have our left component and our right components displayed in their respective places on the screen. Now, if you want to make it more obvious what this split screen component is doing, you can also add some styles to our left-hand component and right-hand component. And to do that, you can either use styled components, like we did before, but since this is going to be a fairly simple example, all I'm going to do is pass a style prop to the H one tag in our left-hand component. And we'll say background color, and we'll just make it something very obvious. We'll just say green, for example. And then for our paragraph tag inside our right-hand component, we'll say style, and for the background color there... we'll make that red, okay? So now, if we save this and go back, we're going to see that our left-hand component is displayed on the left-hand side, and our right-hand component is displayed on the right-hand side.

### Split-screen component improvements
- All right. So now that we've seen how to implement a basic split screen component, I'm going to show you a few modifications that we can make to that component in order to make it a little more developer friendly. So the first thing we're going to see is how to add weight to different components displayed by our split screen. What I mean by that is we might want our left component to take up less space and our right component to take up more space or vice versa. Now, the way that we can do that is simply by adding two more props to our split screen component. The first one is going to be left weight, and we're going to give that a default value of one. And we'll also have right weight, which will also give a default value of one. Oh, and the syntax for that is left weight equals one and right weight equals one. Okay, so basically all we have to do now is just pass this left weight and right weight through to their respective pane components and then modify this flex property accordingly. So what that's going to look like, and this is just how it works with styled components, we're going to say weight equals left weight. And for our right pane, we're going to say weight equals right weight. All right. And then we just have to go up to our pane component here, and we're going to insert the value of that weight prop into the flex property. And the way we're going to do that, again, this is just the way it works with style components, so don't worry about the syntax here, is we're going to say props and we're going to map that to props dot weight. Okay, so in other words, whatever we pass in for left weight and right weight, will replace this here. So if we pass in one, it'll be flex one. If we pass in five, it'll be flex five, et cetera. Okay, so let's see how to use this. We're going to open up our app dot JS component now and add these two other props that we just created. So we're going to say left weight, and let's say that we want the left-hand side to be one third as large as the right hand side. Well, since the weight props that we've defined pretty much reflect how Flexbox works. Our left weight is going to be one and our right weight will be three. All right, so our left weight is going to be one third as wide as our right weight here. Okay, so let's take a look at our app now. And we see that the left-hand side of our split screen is now a third as wide as the right-hand side. So this would be good if we wanted to display something like a side nav of some sort. So we've seen how to add weight to the different items in our split-screen component. And the next optimization that I'm going to show you is that instead of passing in our left-hand component and right-hand component as props, it's possible with layout components to make them accept their children as children in the sense of react. Let me show you what I mean by that. Instead of passing left and right as props, okay, we're going to keep our left weight and right weight here, instead of passing our left and right components as props, we're actually going to put them inside our split-screen component as children. What that's going to look like is this, we're going to say left-hand component and right-hand component like that. And then in order to make this work with our split screen, we're going to need to open that up. And we're going to remove the left and right props here and replace that with the children prop. And then what we're going to do is down here in the body of our split screen component, we're going to say const. And since children is going to be an array in this case, containing all of the elements that we passed as children to our split-screen component, what we can do is say const left and right. And notice we're not using capital letters in this case, since these are elements and not components, we're going to say equals children. And then instead of left as a component, we're going to display left, just using the curly braces. And then for right, we're going to do the same thing. Okay, so we have left and right inside curly braces. And as we can see now, if we go back over to our app, nothing has changed except that this is generally considered to be more developer friendly, right? Being able to pass in components as children to a layout component instead of having to pass them in as props. And what this also allows us to do is for our left-hand component, if our left-hand component needs to accept props, let's say that it needs a name prop of some kind and our right-hand component takes a prop. Let's say message. Okay. And let's display those inside of there. So we'll say message and name. Okay. If we want to pass those props into our left and right-hand components now, we can just do that directly. So we can say name equals Shaun, for example, and for our right-hand component, we can say message equals hello. Okay. And we can see that that works just like we want it to, whereas if we were rendering these components inside our split-screen component and passing them through as props like before, we would have to actually pass those name and message props through our split-screen component to our left and right components respectively. So we would have to add something like this and say, right props equals blah, blah, blah. That would be an object. And the same thing with left props. And we would have to pass those directly to here. So this is just a much easier way to do it right. Saying left and right. And that allows us to pass props directly to it. And it's just considered to be a little more readable that way.

### List and list items
- All right, so the next design pattern that we're going to take a look at here with layout components is lists and list items. Now, to start off here in the exercise files, you're going to find something a little bit different. Inside the app component, we have an array of people data and an array of products data, and what we want to do is display this data inside several different kinds of lists. So I'm going to show you how to create some list and list item components that can help us do this most effectively. So, first of all, let's create a few different kinds of list items for the people and the product. We've got different data to display here, such as name, age, hair color in the people than we do with our products where we have name, price, description, et cetera. So let's start off by creating some list item components and we're actually going to create two different variations of list items for each type of resource. So let's create a folder for our people, and inside there, we're going to create a SmallPersonListItem.js and a LargePersonListItem.js. Okay, and we're going to do the same thing for our products. So let's create a product folder, we'll say products, and inside there, we're going to say SmallProductListItem.js and LargeProductListItem.js. All right, so let's go through real quick and implement each of these. First of all, we're going to start off with our small person list item, and we're not really going to add any styling to these. It's really just going to be small or large depending on the quantity of information that it displays. So for our small person list item, I'm just going to type this out real quick, we're going to say export, const, small person list item. It's going to take a person as a prop. It's going to get only the name and age from that person props, so we'll say const, name and age equals person. And then, what we're going to do is return a paragraph that says name, name, comma, age, and then we'll put in the person's age and we'll put years after that. So that's our small person list item. Now notice that this small person list item doesn't really contain any styling that would indicate it knows where it's being displayed. In other words, we could display the small person list item in a numbered list, in a very narrow list, in a very wide list, and we could use the styling in its parent component to determine how it gets displayed. We'll see that in more detail a little later on. For now, first, let's implement our large person list item. For that, I'm just going to copy and paste our small person list item into large person list item. We're going to have to change the name here and this one's going to display a little more information than the small person list item. What we're going to do is get the name, age, hair color, and hobbies, properties from the person, and we're going to display them like this. Now, we're going to display all of this inside a react fragment for the same reason that I mentioned before. We don't really want this large person list item to be determining its own styling, we want its parent component to be able to do that. So we're going to have the name displayed like this. We're just going to say name, inside an h3 tag. Under that, we're going to have a paragraph tag with the person's age, we'll say age, age years. Under that, we're going to have their hair color. So we say hair color and insert the hair color into the JSX there. And then under that, we're going to have an h3 heading that says hobbies, and we're going to display all of their hobbies here. Remember that hobbies is an array if you go back and look at the original data. So we're going to say hobbies, under that, we're going to put an unordered list and we're going to map the hobbies. So we're going to say hobbies.map and for each hobby, we're going to add a list item which we'll need a key, of course, that key is just going to be the hobby itself, and we'll insert the hobby string into that list item. So that's our large person list item and our small person list item. Now, before we go on to implementing the small product and large product list items, I want to actually create the list components themselves. So, currently, we've only been creating the actual list item components. So let's take a look at what the lists that are going to display these components are going to look like. Now, contrary to what you might be expecting where we might have a large person list and a small person list, and a large product list and a small product list, we're actually just going to have a single list component that can display all of these different list items. Let me show you how that works. Inside the source folder, we're going to create a new file and we'll call this regular list. I'll show you how to make other types of lists in a minute here. And here's what regular list is going to look like. We're going to say export, const, regular list, and this list is going to take the items that it should display. So it's taking a prop called items and it's also going to take a prop called resource name. So this is going to be either products, or people, or whatever kind of resource that this list is going to be displaying. You'll see how we use that in a second. Now, the final prop, and I'm going to just indent all of these for readability. The final prop here is going to be called item component. Now, this is going to be the actual component that we use to display each of the items in this items array prop that we're getting here. So just like we did with the left and right-hand components when we saw how to do a split screen, we're going to rename item component so that it's got a capital letter. This just keeps in with React's convention of capital letters at the beginning of their component names. And then for the body of the component, here's what it's going to look like. It's actually going to be very simple. We're just going to say return and inside some react fragments. We're going to map over all of the items and display one item component for each of them, passing it to the prop called resource name. That might sound a little confusing but here's what it looks like. We're going to say item.map. We're going to get the item and its index here. And then, we're going to display the item component and pass through the current item that we're looking at to the prop with the name of a resource name. And what that's going to look like, this might look a little confusing for you. First of all, we need to add a key, which is just going to be the index. Normally, you're not supposed to use index as keys but we're just going to do that for now. We're going to use the spread operator, so dot, dot, dot, and then we're going to spread an object with a key that's going to be that resource name prop that we had up above, and we're going to pass through item for that. So what this is going to change to, let's say that we pass in person as resource name, this is going to change to person equals item. So that's what that's going to change to. It's kind of a confusing syntax at first but it's something you'll get used to. So that is how our regular list component works. Oh and this should be items.map, not item.map. All right, so let's see how our regular list works now. Let's open up our App.js component and display two lists, one which is going to display all small person list items and one which is going to display all large person list items. All right, so down here in our app, we're going to remove this h1 tag that I put there. We're going to display our regular list, which my IDE is going to import for me automatically. And then for the props, we're going to say items equals people. Under that, we're going to say resource name equals person. Remember that this resource name is the name of the prop that our small person list item and large person list item are expecting. And finally, we're going to pass through the component that we want each of these people to be displayed inside of. So we're going to say item component equals and we're going to include one with our small person list item, which again is going to be imported automatically for me. So make sure you go up and do that if your IDE doesn't do that. And that's how the regular list works. So we have one regular list with our small person list item. Under that, let's display one with the large person list item, just to show you what's possible with that. We're going to say item component equals large person list item. And now, if we run our app, which you can again do with NPM run start, we're going to see that up here at the top, we have a list of our people with the small person list item component. And down below, we have the same list component displaying a completely different list. For all of the people, it's using the large person list item. And I just want to point out before we move on that the regular way of doing this is not to have this reusable list component. It's, instead, to create a large person list item list and a small person list item list that then display those components. So, as you can see, the way that we've done it here makes the regular list a lot more reusable. We're able to simply pass in the component that we want to be displayed as children of this list.

### Creating different list types
- Okay. So now that we've seen how to use our regular list component to display people, using two different item components, we're going to implement the same kind of components for displaying products, right? So we have our small product list item and large product list item. Let's just create some very simple components for those. So for a small product list item, here's what that's going to look like. We're going to say export const, small product list item, and that's going to take a single prop, which is going to be product, right? That's the product that it's supposed to display. And for our small item, we're just going to get the name and price of that product. We're going to say equals product. And under that, we're going to say return and simply display in an H3 heading. You can use basically whatever element you want here, but I'm going to use an H3 heading. We're going to say name and price with a dash in between them, okay. And again, what this is going to allow us to do is have the parent component, essentially, whatever kind of list is displaying this item, determine the overall styling instead of us, you know, putting some kind of styled div as a wrapper. So that's a small product list item, for the large product list item, we're just going to add a little bit more data. So we'll say export const, large product list item, equals, and we have the product as the prop. And we're going to get the name, price, description, and rating from that product prop. So we're going to say name, price, description, rating equals product. And we're going to display all of those inside a fairly simple UI. We're just going to wrap all of this inside of react fragment, and we're going to have an H3 heading with the products name, like that, under that we're going to have the price of the product. So we're just going to display price inside a paragraph tag. Under that, we're going to have an H3 heading that says description. All right, so under here will be where we display the description now. We're going to say paragraph description. And finally under that, we're going to say average rating and display the products rating, okay. So that's the large product list item, before we display these however, I want to show you how to create a different type of list. So earlier we created this regular list, which simply takes some items, a resource name, and a given component that we want to display , maps over the items and passes the correct props to whatever component we give it. Now, if we wanted to simply display our large product, small product list item, et cetera. Inside this regular list, all we would have to do, is change this regular list, change items to products, change the resource name to product and change the item component to either small product list item, or large product list item. All right, and it would be as simple as that, we don't have to create any extra components or anything. Now, what if we wanted to display, as I've said before, a different type of list. What if we wanted to display a list that automatically numbered all of its items, for example? Well, the way we would do that is by creating a similar component to our regular list that we created before. All right, we're going to create a new file and we'll call it numberedlist.js, okay. And the numbered lists is going to be very similar to the regular list. The main difference is that it's going to automatically display numbers, along with its items. All right, so it's going to take items, resource name, and item component. And then instead of simply displaying the item component inside this map here, we're going to wrap it in react fragments and above this here, we're going to have H3 and we're going to display the number of each item that we're displaying. Now, since I is the index, we're actually going to display I plus one, so that it starts at one and goes one, two, three, four, five, et cetera, okay. So now all we need to do, if we want to display, let's say the large person list item with a numbered list, we literally just change this to numbered list. And it's not importing that for me because I forgot to change the name of it inside of here. So we'll change that to numbered list. Let's try typing that again. There we go, and it imported it for me now. Okay, so if we want to display our large person list item with the numbered list, all we have to do is say numbered list instead of regular list. And if we want to display our large product list item with the numbered list, all we have to do is take that change people to products, change resource name, to product, and change large person list item to large product list item, which will also be important automatically. So if we go back now, we see that the numbered list worked just like we wanted it to. Now, I didn't add much styling here. If you want to do that yourself, feel free to go ahead and do that. And we see that the numbered list also worked with each of our product list items. So what you can see here, the point of all of this is that by creating just six different components, right. Our large and small person and product list items and our regular list and numbered list components. We were able to create a lot of different combinations, right? We were able to create a total of eight different combinations. If you assume regular and numbered for each of these small person list item, large person list item, et cetera. And that might not seem like a huge savings at first, but as your apps get larger and larger, this can really end up saving you a lot of time.

### Modal components
- All right, so we've seen how to do split screen components. We've seen how to do list components and list items. The last layout component that we're going to take a look at here is modals. Now, modals are obviously an incredibly popular thing to see in web applications. So let's see how to create them as another layout design pattern. The first thing we're going to do is create a new file here, which we'll call modal.js. And this is going to contain all of the code for our modal, obviously. Now, before I show you how to implement this component, I just want to say that when most people go to add modals to the react application, almost always the first thing they do is install, react modal, or a similar package like that, but that's really not necessary. And I'll show you why it's actually quite simple to implement your own. What we're going to do is we're going to say import use state from react. And we're also going to import styled from styled components. We're going to be using this to add the actual modal styling. And then our basic modal component is going to look something like this. We'll say export, const, modal, and we're going to basically get the children. This is going to be very similar to what we did with our split screen component. We're not going to pass in the modal contents as a prop. In other words, we're just going to display them, sort of like this. We're going to say modal, and then inside there some component. Inside, say the app component, okay. So this children prop allows us to do that. Now for the body of our component, we're going to have a state variable here called should show and set should show. And we're going to set that to false initially. So initially the modal is going to be hidden, okay. And then for the actual structure of the model, we're going to go up and create two different styled components. The first one is going to be called modal background, and that's going to be a styled div. So we'll say styled.div, and with back ticks, and we'll come back to the styles for that in just a minute. And then we're going to have another style component called modal body. So we'll say const modal body equals styled.div, and we'll come back and do both of those in just a second. First, I just want to show you what the JSX here is going to look like, with those styled components. We're going to basically just have the modal background here. Inside that is going to be the modal body and inside the modal body is going to be the actual children that we passed to this modal component. Now we're going to add a few more things. The first thing is that we only want the modal background, modal body, et cetera, to show when should show is true. So what that's going to look like, we're just going to use short circuit evaluation here to do that. We're going to say, should show and, and then with parentheses, we'll say modal background, modal body, et cetera. So in other words, all of these things are only going to show, if should show is true. And in order to actually get the modal to show up in the first place, we're going to put a button who's on click property, basically sets this should show state to true. So we're going to have a function here that says set should show to true. And the button is going to say something like show modal, okay. And in order to make react happy, we're going to have to wrap all of this in react fragments. This isn't so much for styling, mostly this button here that shows the modal is just to get the modal to show up in the first place. Later on in the course, we're going to see a better approach on how to do this, okay. Now, a few more things before our model will work like we want it to. The first thing is that when a user clicks on our modal background, we'll want it to hide the modal, right? This is pretty typical functionality in most modals. So we're going to say on click for that equals, and this is just going to say, set should show to false. And then inside the body of the modal itself, we're going to have another button that will actually allow the user to hide it. Normally this would just be an X button or something up in the top right-hand corner. We're just going to use a regular button for now that says hide modal. And for the on click method of that, we're going to set should show to false. So on click, set should show false, okay. And lastly, for our modal body here, we need to add an onclick event. And basically what this is going to do is call event.stop propagation. And basically the reason that we have to do this is whenever the user clicks on one of the children inside our component, we don't want that click event bubbling up and closing the modal, right? If we left this off, that's exactly what would happen whenever the user clicked on anything inside the modal, it would close the modal. So that's what our model needs to look like. Let's now add some of our styles. And in fact, the styles are not super complicated, but if you just want to copy and paste those from the end state of the exercise files, I would highly recommend that. In fact, that's what I'm going to do here, just to save us a little bit of time. So that's what the modal background is going to look like. It's just going to be a semi-transparent, dark gray background that covers the rest of the page. And for our modal body here, I'm just going to copy and paste those as well. It's basically just going to have a white background. It's going to take up 50% of the screen, have a little bit of margin, padding, et cetera. So that's our modal component, in order to demonstrate what this will actually look like, let's open up our app.JS. And just to show you, remember earlier, when we created our small person list item, large person list item, et cetera. I said that making those in such a way that they didn't contain their own styles would make them much more flexible in the future. Now I'm going to demonstrate how that's true by inserting one of those list items. Let's pick the large product list item, for example, and displaying that inside our new modal component, okay. So let's display our model here and inside that modal, we're going to display our large product list item. So we'll say large product list item. And for the prop here, that's just going to be product and we'll pass the first element of our product array up at the top, okay. So if we make sure that our app is running and head over here, we're going to click on show model, and sure enough, we'll see that the details of that product are now inside our modal, right? And you can click either on the background or on this hide modal button and it will hide the modal for us. All right, and obviously if we were going to use this large product list item for other things, besides list items, we might want to rename it to something like large product details, right? And that would make more sense. And that would allow us to basically display that now either in a list or in a modal, which is kind of the strong suit of layout components.


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
