**## What you'll learn**



\- What flows are, and how they work

\- How to create flows

\- How to create flows within flows

\- How to duplicate flows, and reuse existing flows

\- How to transfer local variables between flows



***\*What are flows?\****



A flow is a set of blocks in Voiceflow organized within a single canvas. When you are working on Voiceflow, everything you can see on the canvas is all stored within a single flow. 



Flows can contain other flows, allowing you to stack them and organize thousands of Voiceflow blocks into easy, manageable sections that you can duplicate and reuse.

Flow blocks work like a file system for your projects - you can see this on the left by clicking the flows tab or hitting the Flows hotkey (CMD + > on Mac and Ctrl + > on Windows)

![img](https://i.imgur.com/lCdCmxm.png)



***Flow diagram\****

Once a flow has been entered, you are shown a version of the start block that carries on from where the flow block beggins. This block acts similary to the standard start block in the ROOT flow but will not be the starting point of the project, only for the specific flow that it is in.

![img](https://i.imgur.com/doEKJSL.png)



***\*The ROOT flow\****



The ROOT flow is the main flow for your project. When you start a new project, you will see the ROOT flow as the only flow. You cannot change the name of the flow, or delete this flow. Every flow used will be a sub-flow of the ROOT flow.



There are three settings for each flow block:



\- ***\*Rename:\**** change the name of your flow

\- ***\*Duplicate:\**** duplicate the flow

\- ***\*Delete:\**** delete the flow



\1. ***\*Editing flow names\**** You can edit every flow name except for the ROOT. When you do this, you cannot rename a flow to a name that is already taken. 

\2. ***\*Copying flows\**** When copying flows you will copy just the single flow. For example, if you are copying a flow that has a flow within it, you will only be able to copy one layer at a time. Doing so will produce an exact duplicate of the flow you had copied.

\3. ***\*Deleting a flow\**** When you delete a flow you are deleting it permanently. It is highly recommended you do not delete flows unless you 100% are sure of doing so.



Flows Menu



![img](https://i.imgur.com/X8CWBhz.png)



The Flows menu has a list of flows as well as a search bar at the bottom that allows you to search through your flows.

***\*Reusing flows\****



You can reuse flows by dragging a new flow block onto the canvas and rather than hitting the 'create new flow' button, you can select from the list of existing flows. You can do this by clicking on your newly placed flow block, and on the right menu you'll see the bar to 'select existing flow'.



![img](https://downloads.intercomcdn.com/i/o/110239689/5a9a905604340395ec69fe80/image.png)



By doing this you'll be able to reuse the flow. If the other flow was in the 'other flows' menu, you will see this flow be taken out of that menu, and placed back into the flow tree according to where you placed your flow block.



***\*Creating flows\****



Within the flow block, you can hit the button create flow to create a new flow within your flow tree. If you do not create the flow within the flow block, the flow will not exist in your flow tree and will lead to a dead-end block for the user.



Once you hit 'Create New Flow', you will be brought into a new canvas where you'll only have a start block. From here you can build your new flow.



Once you create the flow, you will see your new flow active on the left flow bar showing your flow diagram. The active flow you are on is always highlighted in blue.



![img](https://downloads.intercomcdn.com/i/o/110239839/ec4f81add1252cb5c30df76f/image.png)



***\*Local variables in flows\****



![img](https://i.imgur.com/9AKANpZ.png)****

![img](https://i.imgur.com/E8dBXgn.png)

Flows have their own variables called local variables. For example, if you were to have two different flows called 'A' and 'B', each flow would have its own unique set of local variables. This means that you can have variables with the same name, such as {score} in two different flows without them colliding.



Local variables are different than global variables which are accessible throughout your project and will collide between flows



***\*Sharing local variables between flows\****



If you want to have local variables shared across flows, you can do so by using the variable mapping feature on the settings bar (right bar when you click on a block) of each block.



Each flow block, except the ROOT flow, can have input, and output variables. Flow blocks can have both, either, or no variable inputs and outputs.



\- ***\*Input variables:\**** local variables being passed into that flow from the flow above it in the flow tree diagram

\- ***\*Output variables:\**** local variables that are passed out of the flow diagram, back into the flow above it in the tree diagram. 

