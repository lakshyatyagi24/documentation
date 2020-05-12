# Tracking user sessions

Learn how to better personalize your voice apps with Voiceflow's tracking variables.

**Blocks Used:**

- [IF Blocks](/blocks/if-block.md)
- [SET Blocks](/blocks/set-block.md)

**Tracking User Sessions Overview**
Voiceflow gives you the ability to track the number of sessions a user has had on your voice app through the use of persistent variables. This allows you to better personalize the experience of your users.

**Persistent variables**
Persistent variables means that variables created on a per-session basis do not reset when the user stops using your app. This allows you to do things like track the number of sessions a user has had in a variable, even though they close your skill. **Every global variable in Voiceflow is a persistent variable - meaning they last across sessions.**

**Example: User Onboarding**
In this example, we're going to build a user onboarding. Onboarding is when a user logs on for the first time, they are presented with a unique blocks sequence they will only get on the first session. This allows you to ask questions such as their name, favorite color, or any other piece of information you would like to use in your skill in the future.

In our example, we want to ask the user for their first name on the first session so that we can use it for all of our future needs to personalize the experience for them.

**Built-in variables (what we'll be using)**
Voiceflow has five built-in variable types which cannot be deleted. They are {sessions}, {user_ID}, {timestamp}, {platform}, {locale}. The built-in {sessions} variable counts the number of sessions a unique user has had with your app. On their first session, the variable will be equal to 1 as the built-in variables are updated as soon as a user launches your app.



**Step one: check the default variable for {sessions}** The first step of creating an onboarding is to split new users, and returning users right off the launch of the app. To do this, we're going to add an IF Block right after the start block which will check to see if {sessions} is equal to 1. If {sessions} is equal to 1, then that means it is the user's first session. If {sessions} does not equal 1, then this is not the user's first session and they are a returning user. 

So, in our IF block we want to have the ELSE condition go down the returning user path, and the #1 condition which checks if {sessions} = 1 to go to a speak block for new users to go down, and start the onboarding.

![img](https://cdn.zappy.app/4366c04834e125494cb2cf6f1251dd01.png)

**Step two: capturing the user's name to use for future sessions **We want to welcome the user to our skill in the 'new user' speak block, and then proceed to ask them for their name to be used in future sessions, followed by a capture block hooked up with the variable we are using to capture name. For the returning user speak block, we can proceed to have the user enter the normal skill without having to be asked their name.

![img](https://cdn.zappy.app/6721da05bcb56b354a384d9f1c6cc134.png)

You're done! Now, in all future sessions your user will have their name saved. If the user wishes to reset their name, you could add an [Intent block](https://learn.voiceflow.com/block-specific-tutorials/advanced-blocks/intent-block) with the intent 'reset skill' to reset all the variables and take them back to the onboarding.

Let's do that now.

**Resetting variables**

**Step one: add an** [Intent block](/blocks/intent-block.md) 
We want the user to, at any time, be able to reset their app's variables and start from the beginning. To do this, we need to add an INTENT block with the intent 'RESET'. When the user asks Alexa to RESET, no matter where they are in that flow (not sub-flow), this intent block will be activated.

![img](https://cdn.zappy.app/d8a76357c51c40d91f9273d60d642a13.png)

**Step two: reset app variables with a** [Set block](/blocks/set-block.md)
Next, we want to hook our RESET intent block up to a SET block which will reset all of our variables, most importantly the sessions variable. In this example, we reset the {sessions} variable to 1 which treats the user like its their first session. Then, we link the user back to our original [IF Block](/blocks/if-block.md). The user's {sessions} variable has been reset to 1, so they will activate the 'new user' condition on our IF block and be sent through onboarding again where they can reset their name variable.

![img](https://cdn.zappy.app/c51aa1f28a5f2f2ae2a628f0eddda195.png)

That's it! Hopefully you enjoy using the built-in variables to build some amazing voice apps