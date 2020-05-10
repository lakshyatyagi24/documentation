# Code Block
## What You'll Learn 

➤   What the code block is and how it works

➤   Example applications of the code block

## Code Block Overview**

The code block accepts a popular programming language known as **JavaScript**. If you don't know how to code, that's alright! Thankfully, there's lots of resources we can use to integrate this block into our skill's logic. 

![img](https://downloads.intercomcdn.com/i/o/109208313/0c2cfde1732a1a448196de06/Screen+Shot+2019-03-15+at+5.09.20+PM.png)

## JavaScript Resources

- [W3Schools](https://www.w3schools.com/js/) - good for learning JS syntax and supported functions
- [Stack Overflow](https://stackoverflow.com/) - good for finding answers to specific questions (must specify that you're using JS in your search).

## Beginner's Example**

To store a random number from 0 - 100 in the {random_num} variable put this in your Code block:



```
random_num = Math.floor(Math.random() * 101); 
```

Declare 'random_num' as a variable on Voiceflow. Connect the Code block to a Speak block that states "The random number is {random_num}" and run your project on the Voiceflow test tool. 

![img](https://downloads.intercomcdn.com/i/o/109211439/1b1cf3d2e6f352c8efb1885f/Screen+Shot+2019-03-15+at+5.31.05+PM.png)

I copied this code from [here](https://www.w3schools.com/js/js_random.asp). Easy stuff, right? 

## **Advanced Example**

To get the current date in (yyyy/mm/dd) format put this in your code block:



```
var today = new Date();
var dd = today.getDate();
var mm = today.getMonth()+1; //January is 0!
var yyyy = today.getFullYear();

if(dd<10) {
    dd = '0'+ dd
} 

if(mm < 10) {
    mm = '0'+ mm
} 

var todaysDate = yyyy + '-' + mm + '-' + dd;
```

Declare 'todaysDate' as a variable on Voiceflow. Connect the Code block to a Speak block that states "The current date is {todaysDate}" and run your project on the Voiceflow test tool. 

![img](https://downloads.intercomcdn.com/i/o/109212317/df18448ad436350ac3687076/Screen+Shot+2019-03-15+at+5.38.39+PM.png)
