---
layout: post
title:      "Moving from ideas to code. Methods and tips."
date:       2020-03-02 17:50:46 +0000
permalink:  moving_from_ideas_to_code_methods_and_tips
---


While working through the Learn curriculum, whether it be a lesson, lab, project, or videos from the Flatiron staff, there are some key tactics of moving from the position of having just general ideas of what you want your project to be, to actually coding with a clear path of how to get to that idea. I want to use this blog post to outline some of these fundamental tactics that I have found useful throughout the course, and especially while working on the recent final Rails project.

**Feature Story**

One of the most essential methods of getting your program from just an idea to actual code, is to create a "feature story" of your application. The feature story should include what you want the program to do, often describing the experience of using your app from the user's point of view. For example, "a user will be able to log in with their e-mail and password, and then be able to edit their own profile while being able to look at other users' profiles'" would be an example of a feature story. Having this allows you as the developer to be able to easily visualize what it is you actually want the experience of someone using your app to be like, and from there you can begin to outline the steps needed to obtain that goal.

**Simple Steps**

Once you have the feature story giving a clear conception of what the program will look like when it is finished, a good next method to implement is to put your workflow into the concise steps to reach the feature storys' functionality. These steps should be broken down into their most specific form and should be very simple. For example, "step 1, generate a user model and controller," "step 2, stub out a #new method in the User controller," and so on. With the feature story and your simple steps in place, a clearer picture is beginning to form of how to get your ideas into code.

**Hard-code / Stub Out Data**

Before getting into the nitty-gritty of your programs' code, it helps to stub out the information the program will actually be dealing it. As you implement the simple steps, instead of dealing with abstract information and code, begin by hard-coding variables just so you can test the basics of the program. Once you have a working program with your hard-coded data, you can begin the process of abstracting that data.

**Efficiency / Organization**

Finally, make sure your methods and files generally only deal with one job in your application. Avoid messy files with lots of steps. Utilize helpers and partials to deal with repetition or messy code.

I've found a reportoire of tactics to help going from ideas to actual code to be very helpful in my projects. Good luck and happy coding!


