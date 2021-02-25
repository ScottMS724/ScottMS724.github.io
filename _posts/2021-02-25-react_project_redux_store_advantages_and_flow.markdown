---
layout: post
title:      "React Project: Redux Store Advantages and Flow     "
date:       2021-02-25 18:03:07 +0000
permalink:  react_project_redux_store_advantages_and_flow
---

For the final project of the Flatiron curriculum, a Single Page Application (SPA) app was to be created using the JavaScript framework React:Redux for the frontend. React:Redux made managing all the moving parts and changing pieces of an app much easier to manage. In this blog post, I'd like to outline what building my app in Redux taught me about this powerful framework, and why it is useful.

The main advantage of Redux is having all the state of the application in one place. With Redux, this is known as the 'store.' Data that is modified upon certain user actions is 'stateful' information, and the Redux store keeps track of all of the stateful data. This means it is a lot easier to keep track of all that data, and allows it to be easily referenced at any moment. It also means easier transfer to different parts of the app of this stateful information, rather than the developer having to keep track of what the state is at all the different places of an app (without a Redux store). This is a huge boon, especially as apps get more complex.

In order for Redux to be able to keep all the stateful data in one place, a certain flow of information has to be set up. It begins with the Redux component importing the functions (known as actions) it will need to handle the data. The component uses the connect function to give the action full Redux functionality within that component. When the action is called by the component, it begins the dispatch (essentially the command to change a part of the Redux store's state) which activates the action creator that actually changes the state (known as the reducer), and finally, the component then grabs this modified state through the mapStateToProps function, a function that is obtained from the React framework itself. Once this flow and setup is understood, you have the full power of a Redux store at your disposal. All of your state neatly in one place, able to be easily passed around to different parts of your app as needed.

I look forward to utilizing the Redux store in future projects. It is a powerful tool especially as apps grow in size and complexity.
