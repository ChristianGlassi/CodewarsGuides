# Friend or Foe #
### Christian Glassiognon | Javascript ###

## **Introduction** ##

The [Friend or Foe](https://www.codewars.com/kata/55b42574ff091733d900002f) kata is where you filter through a list of strings in order to determine whether that string is a friend or foe. If a string contains exactly 4 letters, they are a friend.

Because our function takes in and returns array as an input we will be using the [Array.filter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) method to filter out any strings that are not our friends. Additionally, the filter method works well because we need to keep original names of the order in the output.

>The filter method works by accepting a callback function as its parameters. This callback function determines what goes into the new array when you call the filter. The callback must return a true false bool to coerce the value into the array. 

### *Friend or Foe Example* ###
##### [Friend or Foe Kata Instructions](https://www.codewars.com/kata/55b42574ff091733d900002f) #####

     Input = ["Ryan", "Kieran", "Jason", "Yous"]
     Output = ["Ryan", "Yous"]


### *Function Signature* ###

     function friend(friends)

     /*friends: array*/

## Code ##

     function friend(friends) {
       return friends.filter( person => person.length == 4 );
     }

>Our callback function argument accepts a single value from the array. Our callback function body returns true if the value is exactly 4 letters long by using [.length](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length) and false if the value is shorter or longer.

##### Hope this guide helps, if you have any suggestions, create a pr request! #####