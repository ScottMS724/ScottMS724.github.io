---
layout: post
title:      "Filling in the Gaps - React Hooks"
date:       2021-05-08 18:32:46 +0000
permalink:  filling_in_the_gaps_-_react_hooks
---


There is one final area of React knowledge to grok after finishing the Flatiron curriculum: React hooks. Hooks give functional components access to the same functionality as class components, allowing for some removal of complexity. They give a way to write reusable code with just functional components besides more usual techniques such as Inheritance. In this post, I want to outline the three most commonly used types of hooks that come with React ("primitive hooks") conceptually and qualitatively. For specific syntax, check out https://reactjs.org/docs/hooks-overview.html. Besides these three hooks that I will go over, there are also other primitive hooks less commonly used, as well as the ability to build custom hooks. 

1. **useState**. As you may be able to infer from the name, useState is a hook that gives functional components the ability to access and modify the application's state. The equivalent in class components would be the use of setState as well as constructors that set the initial state of a class component. A functional component can alter state in the same way by using the hook, useState.

2. **useEffect**. This hook gives functional components the same functionality that lifecycle methods give to class components. By leveraging useEffect, a functional component can tell code to execute *at a certain time*, which is what lifecycle methods do in class components. useEffect can be configured in three different ways: 1. tell code to execute when a component is rendered for the first time only (equivalent to the constructor lifecycle method), 2. tell code to execute when a component is rendered for the first time and on each re-render (equivalent to the componentDidMount lifecycle method), 3. tell code to execute when a component is rendered for the first time, and on each re-render, and when some piece of specific data is changed, (equivalent to the componentDidUpdate lifecycle method).

3. **useRef**. This hook allows a functional component to create a 'ref', often used to access the DOM. This means a functional component can track some attribute of a specific DOM element. It is equivalent to the class component method React.createRef. 

With hooks, functional components can access the utility that would normally only be available to class components. Happy coding all.
