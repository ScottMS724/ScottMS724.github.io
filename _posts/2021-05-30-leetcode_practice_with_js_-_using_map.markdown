---
layout: post
title:      "Leetcode Practice with JS - Using map."
date:       2021-05-30 12:38:29 -0400
permalink:  leetcode_practice_with_js_-_using_map
---


I came up with a simple solution for a problem on leetcode.com that makes use of the helper method `.map` helper method and ended up being a top 96% for runtime speed. Wanted to share my thought process:

__________

**Problem:** Given the array `candies`  and the integer `extraCandies`, where `candies[i]`  represents the number of candies that the **i'th** kid has.

For each kid check if there is a way to distribute `extraCandies` among the kids such that he or she can have the **greatest** number of candies among them. Notice that multiple kids can have the **greatest** number of candies.

**Example:** Input: candies = [2,3,5,1,3], extraCandies = 3
**Output:** [true,true,true,false,true] 
__________


It's clear that the main pieces of data to be concerned about is the value of the `candies` array that is highest (the kid with the "most candies"). We can reference this value as `mostCandies`. Once this value is determined, we simply have to add the `extraCandies` to each value in the array to see if any of these new values are now higher than the initial mostCandies value. Also we must make sure that the final array to be returned has 'true' and 'false' values and not the new integer values.

First, obtaining the highest value in the initial `candies` array. Thankfully, JavaScript provides a handy function for grabbing the highest value out of an array, `Math.max`. So, to reference the value as `mostCandies`:

`const mostCandies = Math.max(...candies);`

Now `mostCandies` refers to the highest value in the array, whatever it is. 

Next, we'll make a new array containing the sums of all the values of the original `candies` array with the `mostCandies` value added to each one. This requires using `.map` to iterate over the `candies` array to add to each value. Remember that `.map` iterates over an array, and returns a new array.

`const extrasAddedArray = candies.map(amount => amount + extraCandies);`

Almost there. All that's left to do is to iterate over this new array (using `.map` a second time) and see if any of the new values are equal to or greater than the `mostCandies` value. We need to return a new array that contains the values `true` if the value is greater than or equal to `mostCandies` and `false` if it's less than `mostCandies`. 

`const trueFalseArray = extrasAddedArray.map(totalCandy => totalCandy >= mostCandies ? true : false);`

Make sure to return that array as the final answer:

`return trueFalseArray;`

And that's it. The solutions' code altogether looks like this:

__

`const mostCandies = Math.max(...candies);

const extrasAddedArray = candies.map(amount => amount + extraCandies);

const trueFalseArray = extrasAddedArray.map(totalCandy => totalCandy >= mostCandies ? true : false);

return trueFalseArray;`
__

How would you solve this question? Can you think of further optimizations to my solution?
