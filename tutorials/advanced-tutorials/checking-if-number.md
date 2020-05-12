# Check if the value is a numbers

Learn how to ensure you get only numbers from users when you ask.

**Blocks used:**

- [Capture block](/blocks/capture-block.md)
- [IF block](/blocks/if-block.md)
- [Speak block](/blocks/speak-block.md)

**When would I need to do this?** Let's say we want to ask the user for their age in our birthday candles voice app, and want to multiply their answer by 5 to calculate the total candle price. We ask the user for their age, and they say '10 years old'. Our app will crash because we can't multiply '10 years old' by 5 because it's a word, not a number.

We want the user to say '10' because it's a number - not '10 years old', which is a word. But of course, it would be bad user experience to ask them beforehand to say only the number - and even then some users may not 'get it' and would still say a word.

So, we want to do a check on their response after they give it to make sure. We can do this by using an IF block after we capture the user's response, and doing a check. If it's a number - everything is OK and the user doesn't even realize we did a check. If it's not a number, we can ask the user to do it again but only saying the number.

For developers wondering how this process works saying to themselves "isn't everything a user says a word?".... yes - but Voiceflow detects if the word said by the user corresponds to a number such as the word 'eight' - and then we convert it to the number '8'. 

Let's dive-in.

**Running a number check** If you're doing some calculations with user inputs and want only numbers, you need a handy way to check if you got a number. You can do this by using an IF block after a capture block. Inside the IF block, we're going to set a conditional for:

- IF {variable} - {variable} = 0

What we are doing above is using the IF Block to determine if the {variable} we captured in the capture block is a number. It doesn't matter what number it is, a number minus itself is always 0 - which is TRUE. If the user said anything that isn't a number, then the IF block will be FALSE because "{word} - {word} = 0 " is NOT TRUE because these are words, not numbers.

The logic looks like this in the IF block:

 [![img](https://downloads.intercomcdn.com/i/o/109539378/9da259e28e27b32f06e8111f/image.png)](https://downloads.intercomcdn.com/i/o/109539378/9da259e28e27b32f06e8111f/image.png)[![img](https://downloads.intercomcdn.com/i/o/109539867/2214d563fa3cd76dd4613083/Screen+Recording+2019-03-18+at+05.06+PM.gif)](https://downloads.intercomcdn.com/i/o/109539867/2214d563fa3cd76dd4613083/Screen+Recording+2019-03-18+at+05.06+PM.gif)

We ask the user for their age with a speak block, capture their response in a capture block, then immediately run their response through our IF block to check if their response is a number. If it is a number, the #1 condition is TRUE and follows the #1 path. If the IF block response is FALSE, that means they did not say a number and follow the IF block's ELSE path where they are asked again to say only the number of their response. The are then rerouted back to the original capture block to try again.

This method ensures that you always get a number from the user, without any skill-breaking user responses.