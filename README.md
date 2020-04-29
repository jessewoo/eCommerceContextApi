# Removing Redux, Using Context API
We are going to replace our local state management from redux to the new context API. This repository is our application before we introduced sagas to handle our asynchronous code, which is a good starting point to make the appropriate changes!

# Pros and Cons of Context API

## Pros
- Context API will be around as it's a CORE FEATURE of React. 
- Both Context API and Redux, the purpose is to handle handling local state, a single source of truth and a single direction of data flow.
- Context API is way less VERBOSE, easier to write
- It's LIGHT WEIGHT STORAGE for state management as Redux, is very opinionated in how it needs to be setup
- Context API offers efficiency and ease of use.

## Cons
- We lose the FLEXIBILITY of the redux ecosystem. We lose redux-sagas, lose redux-thunk, lose ability to handle asynchronous actions inside redux middleware. 
- With Redux, we were using HOC connect to connect our components to respective selectors, mapStateToProps, mapDispatchToProps to trigger different things in our components which made things REUSABLE, but now a component is TIGHTLY COUPLED to different properties inside the component itself. 
- As our application grows, we will have to wrap more and more providers in order for our application to access all thing whereas Redux, it’s just ONE Provider and then it separates out all the stores into individual reducers. With Redux, there is better SEPARATION and an easier index.js file to work with.

# Recommendations
For a large / complex application - use Redux because it gives you more power, more flexibility including asynchronous event handling and ability to reuse your components in a much better way. 

For a portfolio project, a landing page or a small project - use Context API without having to install Redux ecosystem.

In the end, all tools to solve specific problems