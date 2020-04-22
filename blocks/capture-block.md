## What You'll Learn 🧠

- What Capture blocks do
- How to use a Capture block
- How to capture a user's answer into a variable

## Video Tutorial

(updated video-tutorial coming soon)

## What the Capture Block Does

The Capture block allows you to capture the user's response into a variable. Once this response is stored in the variable, you can use this value throughout the rest of the skill. 

- i.e. You can ask the user what their name is using a Speak block, then follow that up with a capture block to capture the user's name into a name variable. You could then use the user's name throughout the rest of the project. this is a gchange to demonstrate github.

## How to Use the Capture block

**1. Create a Variable**

Create a variable by heading over to the variables menu on the far left of your canvas. You can name the variable anything you want, but most people will give it a name that corresponds with the data it stores. We're storing the user's name in this variable so we're going to our variable '**name'**.

![img](https://downloads.intercomcdn.com/i/o/109129824/2bcefb6c08de6ed21e34a046/Screen+Shot+2019-03-15+at+11.26.04+AM.png)

**2. Capturing Your Variable** Once we cue the user for a response, it's time to use our Capture block to store their response. Drag a Capture block onto your canvas and open it up.

![img](https://downloads.intercomcdn.com/i/o/109140069/c9c0d0a5502587c486ed702d/Screen+Shot+2019-03-15+at+12.04.44+PM.png)

Select an '**Input Type**' from the dropdown menu. These are Amazon and Google slot types. Choose one that corresponds with what the user is going to respond with. In this example, I'm going to select the **US_FIRST_NAME** slot type. 

- To see a list of Amazon's various slot types and example use case, click [here](https://developer.amazon.com/docs/custom-skills/slot-type-reference.html).

**Note**: Only the slots supported by your selected locale(s) on Voiceflow will be displayed in the dropdown.

![img](https://downloads.intercomcdn.com/i/o/109140223/26cd16a4473dd9484ad0ce16/Screen+Shot+2019-03-15+at+12.04.04+PM.png)

Now that we've selected an appropriate slot, we can select a variable to store the user's response. Under '**Capture Input To**,' a dropdown of all your existing variables should appear. We're going to select our '**name**' variable which we created earlier.

![img](https://downloads.intercomcdn.com/i/o/109149837/823bb68b8464b9978b19894f/Screen+Shot+2019-03-15+at+12.43.36+PM.png)

**3. Time to Test**

Here are our blocks.

![img](https://downloads.intercomcdn.com/i/o/109153034/1c4f18e415c9ca69b6b90a2f/Screen+Shot+2019-03-15+at+12.47.29+PM.png)

Here is the format of 'Speak: Name'

![img](https://downloads.intercomcdn.com/i/o/109153235/ca1af1d4a71b72fa8982f156/Screen+Shot+2019-03-15+at+12.48.09+PM.png)

Here is the output.

![img](https://downloads.intercomcdn.com/i/o/109153308/c1a7f9979490141dd44e69bb/Screen+Shot+2019-03-15+at+12.47.52+PM.png)

From here, we can use the {**name**} variable throughout our project. {**name**} currently stores "Valerie" but can be changed at any point in the project with other blocks. 
