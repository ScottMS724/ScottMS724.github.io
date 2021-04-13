---
layout: post
title:      "Review of React/JS Principles (setState & Arrow Functions)"
date:       2021-04-13 13:23:18 -0400
permalink:  review_of_react_js_principles_setstate_and_arrow_functions
---


This blog post is an assignment associated with my final project assessment. I will be reviewing the concepts of setState & arrow functions. Specifically, what setState (and dispatch) does that simply declaring state (i.e. "state = ") would not, and the difference between 'this' in an arrow function and a regular function, and when you would use one over the other.

**setState vs. state =**

State is data that is modified in the component itself. Unlike a component's props, a component's state can change during the component's life. Why should the react method 'setState()' be used to update state instead of a simple declaration, i.e. 'state = '? The answer is that setState() updates the state asynchronusly, that is, it does not block the React code from continuing to execute while the state is being updated. It allows the component to finish its current task before updating the state.

The other main reason to use 'setState' over a simple declaration is that 'setState' activates React's lifecycle methods. The lifecycle methods 'shouldComponentUpdate()', 'componentWillUpdate()', 'componentDidUpdate()', all depend on state being modified using 'setState()'. Changing state directly via 'state = ' does not signal to the lifecycle methods that the state has changed and that the component should re-render accordingly. React docs explicitly note that state should not be modified directly because of this reason.

**'this' - Arrow Functions vs. Regular Functions'**

JavaScript functions can be defined in many different ways. Two common ways to define functions in JS are 1. regular function declaration/expression (i.e. "function greet(who) {" and "const greet = function(who) {") and 2. arrow functions (i.e. "const greet = (who) => {"). There are key differences between these two ways to define functions that determine when they should best be used. 

One of the biggest differences between regular functions and arrow functions is the value of the 'this' variable. With regular functions, the value of 'this' is dynamic and depends on how the function is invoked. With arrow functions, the value of 'this' always captures the 'this' value of the enclosing/most outer context instead of creating its own context, regardless of how or where the function is being invoked. This means, with arrow functions, it is simpler to keep track of the value of 'this' as the function gets more complex. Additionally, inside classes, an arrow function's 'this' will always equal the class instance, which is particularly useful when methods are used in a callback fashion.

There is a situation where you must use regular functions over arrow functions, and that is when using contructors. Regular functions have no problem parsing code using the 'new' keyword like "const redCar = new Car('red');" when the class is declared using a regular function i.e. "function Car(color) {", but if a class were to be declared as an arrow function i.e. "const Car = (color) => {", then JS will throw a TypeError if "const redCar = new Car('red');" is attempted.

Happy coding everyone :)
