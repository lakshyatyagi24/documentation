## What you will learn

- How to connect a Google account for sheets integration
- Tracking the number of times a user has opened your skill (sessions)
- How to capture a user's name and Amazon ID into a variable, to be referenced again in the future
- How to upload and test on ADC

## Create a Spreadsheet

Let's start by creating a new file on https://docs.google.com/spreadsheets​

In the top of the screen, select the "Blank" template to begin.​​

![Imgur](https://i.imgur.com/h2NVcRi.png)

Name your sheet! for this tutorial, we chose "Users," but you can name the sheet anything you'd like.

![Imgur](https://i.imgur.com/Op5VJbJ.gif)

Add three headers to your sheet: ID, Name and Sessions.

![Imgur](https://i.imgur.com/oK91PRQ.gif)

Keep this page open and go to Voiceflow to create a new project.

For the purpose of this example, we will create a skill that capture's the users' Amazon ID, name, and number of sessions, and put that information into our Google sheet.

## Create a data Using the Google Sheets Block

In your new project, add a Speak block with a welcome message and a prompt to ask the user's name.

![Imgur](https://i.imgur.com/JYKkwfG.png)

Next, add a Capture block with the US_FIRST_NAME as Input Type and create name variable in the Capture Input To field.

*Note: US_First_Name only works if you have the US, CA, or UK locales selected.*

![Imgur](https://i.imgur.com/5YCBNaX.gif)

Drag and drop the Google Sheets block from the Integration section to the canvas.

![Imgur](https://i.imgur.com/hIX4iBo.gif)

We are going to create a new record for the user, so select Create Data.

![Imgur](https://i.imgur.com/3CaBy3t.png)

Click on + Add User.

![Imgur](https://i.imgur.com/xcV6qGt.png)

And login with your Google account.

![Imgur](https://i.imgur.com/RnRdLdd.png)

Select which account you'd like to sign in with.

![Imgur](https://i.imgur.com/irMvu6M.png)

On the next popup window, click on Allow to link Voiceflow to Google Sheets.

![Imgur](https://i.imgur.com/QjCTEcQ.png)

Now you see your Google account is connected with Voiceflow. Click on Using Sheet.

![Imgur](https://i.imgur.com/xrdbByC.png)

Then, select the spreadsheet (Users) and the sheet you've just created (Sheet1 by default).

![Imgur](https://i.imgur.com/G9CKgFj.png)

In the With values step, use the Voiceflow variable {user_id} for ID (0), {name} for Name (1) and {sessions} for Sessions (2).

![Imgur](https://i.imgur.com/VfPonMd.gif)

You can also rename the block to Create User for example.

![Imgur](https://i.imgur.com/wSuHtwb.gif)

We are now ready to test it so click on the Test Integration button.

![Imgur](https://i.imgur.com/j4PTgWA.png)

On the next window, fill the fields with some test values and hit the Run Integration button.

![Imgur](https://i.imgur.com/NwREaRD.png)

You should have this response if everything went well

![Imgur](https://i.imgur.com/ioT6cwB.png)

And your spreadsheet now have a new row with the test values.

![Imgur](https://i.imgur.com/qL8ymMg.png)

This is great but if we run this skill multiple times, you will have a new record for each session.

So what about updating the user's record instead of creating a new one each time?

As we have already seen, we ask for the user's name at the beginning of our skill, so why not check if we already have a name for this user at each launch and if so, update the number of sessions for this user?

Let's use the If block to do just that

![Imgur](https://i.imgur.com/MNlHs3s.png)

Here we do a simple If to check that our name variable is equal to zero (If we don't have the user's name yet).

![Imgur](https://i.imgur.com/qFxR1xE.gif)

Our project looks like this now. If the variable name is 0, the If block will use the port correspoding to its condtion, if we already have the user's name we are going the Else port.

![Imgur](https://i.imgur.com/Mi83htH.png)

You can also combine blocks to one single Combined block so that its context in this flow will be much clearer.

![Imgur](https://i.imgur.com/D9JpiSK.gif)

## Retrieve and Update a data

Now that we've created the user, we can move on to updating the data.

Let's add two new Google Sheets blocks to our canvas. We've renamed the first Retrieve User and the second Update User.

![Imgur](https://i.imgur.com/WS00WcN.png)

Before continuing, let's take a look at how the Integration block works for the update.

In the Update User Integration block, select Update Data for I want to, your account in As user and the Users spreadsheet and the Sheet1.

As you can see, to perform an update we will need a row number. So we will have to find the row number corresponding to the user's record in the spreadsheet.

![Imgur](https://i.imgur.com/mX6oLYL.gif)

We will use another Integration block but this time we will do a search with the user id, as this number is unique, we are sure to find the corresponding record.

So in the Retrieve User Google Sheets block, I want to Retrieve Data, Using sheet Sheet1 With settings ID (0) = {user_id}

![Imgur](https://i.imgur.com/T2Gmo02.png)

Before going further, we will add the user_row variable to store the result of our search. Click the Interaction Model Manager icon in the lower left corner of the canvas.

![Imgur](https://i.imgur.com/Q9gT8Bs.png)

Then click on variables tab and add user_row variable.

![Imgur](https://i.imgur.com/BcLlbIP.gif)

Let's go back to the settings of the Update User Integration block to complete its configuration.
Fill in the fields as below and click on Next.

![Imgur](https://i.imgur.com/10FacQu.png)

Finally, let's add a speak block to welcome back our user with their name.

![Imgur](https://i.imgur.com/mRKofSO.png)

Of course, you can combine it with Retrieve User Google Sheets block.

![Imgur](https://i.imgur.com/wynpPi9.gif)

And two speak blocks at the end to confirm the creation and the update.

![Imgur](https://i.imgur.com/vJbakal.png)

![Imgur](https://i.imgur.com/0ZXmmo4.png)

Here is what your project should look like now.

![Imgur](https://i.imgur.com/zoQl8kc.png)

## Uploading to ADC and Testing

You can now upload your project to Alexa.

![Imgur](https://i.imgur.com/MVVUFjM.gif)

And test it in the Alexa Developer Console (ADC) simulator by clicking on the link in the confirmation message or directly on your device.
​​​​
![Imgur](https://i.imgur.com/0CXECT9.png)

![Imgur](https://i.imgur.com/mInC1Z6.png)

Here is the result in the spreadsheet after the creation of a user after the first launch of your skill.

![Imgur](https://i.imgur.com/lXCopDD.png)

And here is the result after the second launch

![Imgur](https://i.imgur.com/NTAMgY5.png)

![Imgur](https://i.imgur.com/Om2FK9m.png)

So, as you can see, we checked if we already had the user's name, we greeted him with his name and finally, updated the number of sessions for this user.

With what you have learned, you can now store and update user data as well as create your own analytics tool.
