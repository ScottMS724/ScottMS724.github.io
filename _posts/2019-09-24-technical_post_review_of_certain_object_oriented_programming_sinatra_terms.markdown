---
layout: post
title:      "Technical Post. Review of Certain Object Oriented Programming/Sinatra Terms"
date:       2019-09-24 15:53:49 +0000
permalink:  technical_post_review_of_certain_object_oriented_programming_sinatra_terms
---


This blog post is meant to serve as a review of the three basic ways that the movement of information is handled in a Sinatra application. These three ways are params, sessions, and instance variables. I will explain the information contained by each type and when a developer should look to use each method.

**Params -** Params contain information that was just entered by a user into their browser. They come from a user's browser when a page is requested. Params should be used to capture inforation filled in by a user to an HTML form, often in the controllers of the application. An example of this would be if a user is signing up to a website with a username and password. Params should be used to obtain the custom username and password entered by the user.

**Sessions -** Sessions are a way for websites to track individual users on a website where each person creates their own user account. They are essentially cookie files, but on the website/server side as opposed to the user side. By giving each user a unique sessions' ID, the website knows who is who and will display the appropriate information to the correct user. Sessions are hashes that contain a unique ID for a certain user, and the ID will remain in sessions as long as the user is logged in. When a user logs out, the session hash for that session is deleted, until the user logs in again and is given a session ID again.

**Instance Variables -**  Instance variables are variables defined in a Ruby Class and can be referenced in any methods of that class. Each instance variable is a separate version, or instance, of the Class, and saves information about itself. Each instance variable is saved within its Ruby Class, and will presist unless specifically deleted. For example, @car would be a specific instance that was defined by the Car class. The Car class will give its instance variables certain characteristics that are shared by all instance variables of the same class (i.e. all cars have 4 wheels, two windshield wipers, etc...), but a specific instance variable i.e. @car would have some of its own characteristics that can be specific to only that instance variable (but not every instance of the class Car), such as the specifc model and color of @car. Instance variables are used to share information about the current state of an object, and should be used when you need information about an object to persist over time. In Rails, instance variables can be used to pass data between the controller and views.
