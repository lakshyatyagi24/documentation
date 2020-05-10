# Choice Block

## What You'll Learn

- What Choice blocks are

- How to add choices for your users to make

- How choices work when the user answers properly



## Related articles

- Intents and Slots

## What Are Choice Blocks?

Choice blocks allow you to ask users to make a choice from a pre-defined list of choices. If the user says one of the choices listed in the choice block, it will follow that choice's path. If the user says something that isn't one of the listed choices, the user will follow the ELSE path.



<img src="https://i.imgur.com/wLosZqO.png" alt="img" style="zoom:50%;" />



## Adding Choices

To add choices, drag the choice block out from your block menu onto the canvas. You will automatically have a single choice ready. Select an intent from the drop down list to complete your choice block. 



<img src="https://i.imgur.com/W2dxMRF.png" alt="img" style="zoom:50%;" />



To add more choices to your choice block, hit the "Add Path" button and select and intent. You should see there are now multiple paths on the choice block, one for every path that you have defined.





<img src="https://i.imgur.com/HUI6JL6.png" alt="img" style="zoom:50%;" />



ELSE Port

If the user responds with something that is NOT one of the listed choice options, then the ELSE block port will be activated. For example, if the user was to say "Zebra" as a response choice block asking the user for a "Yes" or "No" answer, it would trigger the ELSE path. This is because "Zebra" is not close enough to "Yes," "No," or any of their synonyms to trigger either path.



Using ELSE As An Error Handler

You can use the ELSE on a Choice block as an "Error Handler". The Error Handler will repeat the available options back to the user, and ask them to choose again. This allows you to ensure they are always choosing from the available options on the list.



<img src="https://i.imgur.com/riGC5jE.png" alt="img" style="zoom:80%;" />