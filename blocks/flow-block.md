## What you'll learn

- What flows are, and how they work
- How to create flows
- How to create flows within flows
- How to duplicate flows, and reuse existing flows
- How to transfer local variables between flows

**Video tutorial**

**What are flows?**

A flow is a set of blocks in Voiceflow organized within a single canvas. When you are working on Voiceflow, everything you can see on the canvas is all stored within a single flow. 

Flows are like boxes that contain your building blocks. Flows can contain other flows, allowing you to stack them and organize thousands of Voiceflow blocks into easy, manageable sections that you can duplicate and reuse.

**The flows diagram**

Flow blocks work like a file system for your Alexa skills - you can see this on the left by clicking the flows icon. 

![img](https://downloads.intercomcdn.com/i/o/110239055/35ee204bab802df1864303b9/image.png)

Here, you'll see your flows file system which displays on the left. Within the flow diagram you have two sections:

- **Structure:** your flow structure shows you all of your flows and how they relate to each other. You can see which flows are inside of which flows.
- **Flows:** this is your total list of all the available flows you have within your project.

**Flows within flows (subflows)**

You can have flows within flows in Voiceflow. You can see what this looks like by looking at the flow structure.

![img](https://downloads.intercomcdn.com/i/o/110239237/cc046272009687c3849b30e8/image.png)

Above, we can see that we have a flow called "Layer 1" below the ROOT flow. 

Example You can think of these flows within flows like chapters within a book. You can go several layers deep with flows. Such as having a stories skill like Storyflow where the user follows the main flow to find the story they want. Then, each story is held within a flow. The user enters that story's flow, and is presented with two chapters they can start with - each held within a separate flow. This is now three flow layers that allows you to store massive amounts of information and moving parts within a single skill.

**The ROOT flow**

The ROOT flow is the main flow for your project. When you start a new project, you will see the ROOT flow as the only flow. You cannot change the name of the flow, or delete this flow. Every flow used will be a sub-flow of the ROOT flow.

**Flow settings**

Each flow (except for the ROOT) has a settings gear next to it which allows you to make changes.

![img](https://downloads.intercomcdn.com/i/o/110239364/b0fd9dfbc04048052d90fdcc/image.png)

There are three settings for each flow block:

- **Edit name:** change the name of your flow
- **Copy:** duplicate the flow
- **Delete:** delete the flow

1. **Editing flow names** You can edit every flow name except for the ROOT. When you do this, you cannot rename a flow to a name that is already taken. 
2. **Copying flows** When copying flows you will copy just the single flow. For example, if you are copying a flow that has a flow within it, you will only be able to copy one layer at a time. Doing so will produce an exact duplicate of the flow you had copied.
3. **Deleting a flow** When you delete a flow you are deleting it permanently. It is highly recommended you do not delete flows unless you 100% are sure of doing so.

**Other (unused) flows & Command flows**

The list of 'other flows' is the list of flows that you have made, but that are not currently being used in your project, so they are not represented in your flow tree. 

![img](https://downloads.intercomcdn.com/i/o/110239564/fb0805f902374905777b4dee/image.png)

Command flows are also in this 'other flows' section, even though they are technically in use.

**Reusing flows**

You can reuse flows by dragging a new flow block onto the canvas and rather than hitting the 'create new flow' button, you can select from the list of existing flows. You can do this by clicking on your newly placed flow block, and on the right menu you'll see the bar to 'select existing flow'.

![img](https://downloads.intercomcdn.com/i/o/110239689/5a9a905604340395ec69fe80/image.png)

By doing this you'll be able to reuse the flow. If the other flow was in the 'other flows' menu, you will see this flow be taken out of that menu, and placed back into the flow tree according to where you placed your flow block.

**Creating flows**

Within the flow block, you can hit the button create flow to create a new flow within your flow tree. If you do not create the flow within the flow block, the flow will not exist in your flow tree and will lead to a dead-end block for the user.

Once you hit 'Create New Flow', you will be brought into a new canvas where you'll only have a start block. From here you can build your new flow.

Once you create the flow, you will see your new flow active on the left flow bar showing your flow diagram. The active flow you are on is always highlighted in blue.

![img](https://downloads.intercomcdn.com/i/o/110239839/ec4f81add1252cb5c30df76f/image.png)

**Local variables in flows**

Flows have their own variables called local variables. For example, if you were to have two different flows called 'A' and 'B', each flow would have its own unique set of local variables. This means that you can have variables with the same name, such as {score} in two different flows without them colliding.

Local variables are different than global variables which are accessible throughout your project and will collide between flows

**Sharing local variables between flows**

If you want to have local variables shared across flows, you can do so by using the variable mapping feature on the settings bar (right bar when you click on a block) of each block.

Each flow block, except the ROOT flow, can have input, and output variables. Flow blocks can have both, either, or no variable inputs and outputs.

- **Input variables:** local variables being passed into that flow from the flow above it in the flow tree diagram
- **Output variables:** local variables that are passed out of the flow diagram, back into the flow above it in the tree diagram. 

An example of when you would want to use input and output local variables on a flow would be a flow for a calculator. Let's run that example. You input two numbers, {num1} and {num2},  you want to multiply together using a flow called calculator. You want to give the calculator flow two numbers, and get back the one multiplied number.

The calculator flow would have its own variables inside because every flow has its own variables. The variables inside the calculator flow are called {number_1} and {number_2}. These two variables are multiplied together inside the calculator flow block using a set block, where the final value of these multiplied numbers is stored inside the variable {final_number}. This is what the calculator flow looks like:

![img](https://downloads.intercomcdn.com/i/o/110240294/4f918743b467b27e2e03ee96/image.png)

In the ROOT flow which holds the calculator flow, we ask the user and capture the two numbers we want multiplied: {num1} and {num2}. We need to 'pass in' the {num1} and {num2} to the calculator flow. To do this, we want to use 'variable maps' which lets us pass the value of variables amongst flows. There are input, and output variable maps.

**You can add a variable mapping by clicking on the flow block with an active flow. For a variable to show up to be mapped, it must be already used within the sub-flow.** 

![img](https://downloads.intercomcdn.com/i/o/110241324/8ea794880a8bc7589abdf5fe/image.png)

For input variables, these are the variables we want to pass into the variables inside the flow. So, we want to pass the value of {num1} to {number_1} inside the calculatorflow. We want to do the same for {num1} and {number_2}. Now, we have successfully passed the values of our ROOT variables into the sub-flow calculator.

To get the final multiplied number out from the calculator flow stored in the sub-flow variable {final_number}, we need to use an output variable mapping. We can create a new variable in our route flow designed to capture this new output number. We created the new ROOT flow variable {final_num}. Last step - we can add a variable mapping to pull the {final_number} sub-flow variable and store that in the ROOT flow variable {final_num}. You can see this below:

![img](https://downloads.intercomcdn.com/i/o/110241484/66f190ea306db5712945baee/image.png)

And that's it! We've successfully used a flow block as a calculator. This allows us to keep project more organized by putting functionality into compartments within our project called flows.
