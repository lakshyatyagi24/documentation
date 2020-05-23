# Uploading Your Project to Google Assistant

A guide on how to link your project to Google Actions and Dialogflow

# **What You'll Learn 🧠**

- How to link your project to Google Actions and Dialogflow

# **Step 1 ➤ Creating an Account on Google Actions**

- Create an account on Google Actions (if you haven't already).
- You must create this account to link your project to Google Actions and Dialogflow.

Visit the [Google Actions Homepage](https://developers.google.com/actions/).

- Click [Go To Actions Console] and log in your with Google account.

![img](https://cdn.zappy.app/9e8b5980d5f13849954fb297b395d2c4.png)

# **Step 2 ➤ Creating a New Google Actions Project**

- You can think of a Google Actions project as the Google equivalent of an Alexa skill.
- However, on the *Google Assistant platform*, for *every unique skill you wish to publish*, you must *create a new project on the Google Actions console*.

To create a new Google Actions project, hit [Add/Import Project].



![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-Lk4vPZBG4Hl2SmkrQBh%2F-Lk4zepyqJiuOKd5aOIA%2Fimage.png?alt=media&token=0c259850-4a42-4f95-9a50-59a6ce528f31)



If this is the first time you are using this account, a window will appear, simply answer the questions and click on Agree and continue.

![img](https://cdn.zappy.app/32d6f774569c9a49f230a4a1b1edcce6.png)

A pop-up will appear. Enter a Project Name and click [Create Project].

![img](https://cdn.zappy.app/06c8da2f8dd245c49c79dcda3ae01c7e.png)

- Select the [Conversational] template in the bottom right corner.
- This will allow you to connect your Google Actions project with a Dialogflow agent ⏤ a requirement for integrating with Voiceflow.

![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-Lk52bwj2EKvOklKZmdD%2F-Lk52e0vmOvYXSYdkfdd%2Fimage.png?alt=media&token=1de3a912-a708-4162-b8c1-97b75c4ff8b7)

- Your Google Assistant project is now created! We'll attach a Dialogflow agent to it in the next section.

# **Step 3 ➤ Creating a New Dialogflow Agent**

- Dialogflow, another Google service, is used as Google Assistant's NLU engine.
- It receives your choices, intents, and slots (called "entities" in Dialogflow) and creates a language model that will be used in your skill.
- Along with a Google Actions project, you will also need to create a new Dialogflow agent for every Voiceflow project that you wish to publish to Google.

You should now be at the home page of your project on the Google Actions console. Under Build your Action, click on [Add Action(s)] in the menu bar to the left.

![img](https://cdn.zappy.app/9f36e1076a901adcd0e8cde473562a3d.png)

- Select [Get started]

![img](https://cdn.zappy.app/ccd211014f1019d45a4a92634eeda0d2.png)

- A 'Create Action' pop-up should appear. Select the Custom intent option and click [Build] and this should open the Dialogflow Console in a new tab.

![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-Lk5BS4PuuMRvYRp1CCF%2F-Lk5CivCUd9YCtVu5Fzz%2Fimage.png?alt=media&token=6b78d1f1-7b19-4c24-a98c-c444233a8822)

- If you see your project name (Test-Project, in this case) and the phrase "Agent will be linked with [project id] Google Project" under the 'Google Project' section, your Google Actions project has been successfully linked with Dialogflow.

Click [Create] to continue.

![img](https://cdn.zappy.app/ce6cefca7ecdeb4e00eb68f252f175ae.png)

*If you see a* ***blank agent name and no listed project in the 'Google Project' section\****, you are logged into the wrong account on* [*Dialogflow*](https://dialogflow.com/) *and must log out. Log back in with the same Google account that you used to create your Google Actions project and repeat the steps in this section.*

![img](https://gblobscdn.gitbook.com/assets%2Fcreator%2F-LgtQ3OQ5vf3eXZiNpGl%2F-LgtWTk5GejmU_ljrwiX%2F8.jpeg?generation=1560038207986823&alt=media)

![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-LmEPhSF_q5zYqsyePaX%2F-LmERtz9CeeXBK8cpGwo%2Fimage.png?alt=media&token=964e3ed4-29f8-4c02-822a-35c0ea1af277)

Logout from Dialgflow if you're not on the same account.

*Log in with the same account, go back to the Google Actions Console window and hit the* ***Get started*** *again.*

![img](https://cdn.zappy.app/ccd211014f1019d45a4a92634eeda0d2.png)

![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-LmEPhSF_q5zYqsyePaX%2F-LmETEfja09Z-TAt9Xdz%2Fimage.png?alt=media&token=f5edcd67-1663-47e8-b1b6-08b56464dff8)

*You should now see the Agent linked to the correct project*

![img](https://cdn.zappy.app/ce6cefca7ecdeb4e00eb68f252f175ae.png)



At this point you have successfully created your agent. Hooray! Now you will need to generate a set of credentials which allows Voiceflow to manage your project on your behalf.

Click the settings icon on the left menu bar.

![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-Lk5BS4PuuMRvYRp1CCF%2F-Lk5EjCxKiNmQdeCRNPy%2Fimage.png?alt=media&token=342da888-5b1e-478e-90f0-5c2bac2b89c7)



Click the 'Service Account' link.

![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-Lk5LK95htVODtHXLX3P%2F-Lk5LuEb9sr17lB-Q94u%2Fimage.png?alt=media&token=307f09b8-7371-46a7-9153-ae5291179443)

This will take you to the IAM & Admin service accounts page.

If you get an 'Unauthorized Access' error message, you might be logged into the wrong Google account. On the IAM & Admin service accounts page, log back in with the same account that you used to create the Google Actions project and Dialogflow agent.

On the left-hand side menu bar, you'll see that you're now in the IAM & admin user management home page, click [CREATE SERVICE ACCOUNT] at the top.

![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-Lk5LK95htVODtHXLX3P%2F-Lk5N6XNPB7mtS8ifWMy%2Fimage.png?alt=media&token=b47d0050-3ff6-4c49-917e-285505c9c095)

In the 'Service account name' field, type in Voiceflow Creator Tool, select the name and click [CREATE].

![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-Lk5LK95htVODtHXLX3P%2F-Lk5OMeU5ubNLK8xdWCk%2Fimage.png?alt=media&token=4731232e-a452-4e6e-ba3d-555a1d2d3dfc)

After selecting [CREATE], you will be redirected to the next page. Click on the 'Select a role' box, and type in 'Dialogflow API Admin'. Select the option [Dialogflow API Admin] from the drop down menu and hit [CONTINUE].

![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-Lk5LK95htVODtHXLX3P%2F-Lk5PbkA5E-UOT9Uq8X5%2Fimage.png?alt=media&token=8a588cde-8d59-4e20-9393-50cdaf07ea75)

Voiceflow will use this service account to manage your Dialogflow agent for your Google Assistant project.

On the next page, click [ + CREATE KEY ]



![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-Lk5kox3-vE1hjOCLIob%2F-Lk5ks8yUB0-Izi6jJnb%2Fimage.png?alt=media&token=d78ddb4a-2402-4ff0-a22a-97f6f92f2a36)



In the pop-up that appears, select 'JSON' as the key type and click [CREATE]. This should download a credentials file to your computer

![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-Lk5kox3-vE1hjOCLIob%2F-Lk5lMR8yJBnZIPqz4v4%2Fimage.png?alt=media&token=01d5f5e1-193c-48d0-aa87-c70761938568)

Upload the file you just downloaded to Voiceflow in the Google publishing page under the 'Google Assistant Credentials File' field.

![img](https://downloads.intercomcdn.com/i/o/211442250/783d229796f73dd2d09cc2d0/vocieflow+2020-05-22+at+16.28.17%402x.png)



# **That's It! 🎉**

- Your project is ready to publish to Google Assistant
- To make changes to your project's Directory Information on Google (Such as Invocation Name, Display Icon, and Locales), see [Deploying Your Google Assistant Project to Production](https://voiceflow.github.io/documentation/#/adapting-for-google/deploying-your-google-assistant-project-to-production)