## What you will learn

- how to use the Reminder Block in conjunction with the User Info and Permission Blocks.
- how to set the reminder in 3 ways: Timer, Scheduled for one-time-only, Scheduled for reccuring.


![img](https://i.imgur.com/HNj0CXD.gif)

## Check user's permission to set reminders


To start you will need the **User Info Block** to check if the user has authorized reminders permission for your skill. Then, choose **Reminders** from User Info Type.


![img](https://i.imgur.com/AVElTsT.png)


On the User Info's **No Access port**, which means the user has not granted reminders permission yet, link a **Speak block** to explain why you're using the **Reminder block** in your skill and to give the user more informations on how to authorize the skill in the **Alexa app** or on [**alexa.amazon.com**](http://alexa.amazon.com/)

![Imgur](https://i.imgur.com/WblXrnc.png)


![img](https://i.imgur.com/jHj9Zl8.png)

In the following example, I'm using the **reminder_text** variable as the reminder text in the **Reminder block** and I've set the reminder time to notify the user in **one minute**. As for the text, you can also use variables for the Hours, Minutes and Seconds fields.

![img](https://i.imgur.com/0MV3OZR.png)

Add the **Permission block** just after the **Speak block** to end this path. Then, select **reminders** for Permissions Request.

![Imgur](https://i.imgur.com/Xk3tHWQ.png)

You can then link the **Reminder block** on the remaining port of the **User Info block**, which means the user has permitted your skill to set reminders.

![Imgur](https://i.imgur.com/uqCBpt6.png)

## Set a reminder as timer

In the following example, I'm using the **reminder_text** variable as the reminder text in the **Reminder block** and I've set the reminder time to notify the user in **one minute**. As for the text, you can also use variables for the Hours, Minutes and Seconds fields.

![Imgur](https://i.imgur.com/qDGxrhd.png)


After **uploading** your skill to **Alexa**, like your future users, you must allow access to the reminder from the **Alexa app** or [alexa.amazon.com](http://alexa.amazon.com/).

![Imgur](https://i.imgur.com/Nv8ZYQt.png)

Here, I'm using [alexa.amazon.com](http://alexa.amazon.com/) to authorize the skill to access the Reminder.

Click on **Update Permissions**

![img](https://downloads.intercomcdn.com/i/o/124670838/ecb97127757a7a046415278b/Image+2019-05-30+at+3.07.32+PM.png)

Go to **SETTINGS**

![img](https://downloads.intercomcdn.com/i/o/124665726/baff71e4f38031367e5d9139/image.png)

And click on **MANAGE PERMISSIONS**

![img](https://downloads.intercomcdn.com/i/o/124665880/f8eaf5a5a9d6ec7101e2cf1b/image.png)

**Enable** the Reminders and hit the **SAVE PERMISSIONS** button.

![img](https://downloads.intercomcdn.com/i/o/124666239/cb1fbbf7a6b8788b95edfe12/image.png)

![img](https://downloads.intercomcdn.com/i/o/124666138/e7b858496a3b1bea0efe9736/Screen+Recording+2019-05-30+at+03.09+PM.gif)

In another way, you can manage permission on your Alexa app. Permission Block will send a card to Alexa app, which leads the users to allow your skill to access to reminders. You can see a card in home screen of Alexa app or Activity menu.

These are the samples of a card in home screen and in Activity menu. Tap on **Manage** on a home card, or **UPDATE PERMISSIONS** on a card in Activity.

![Imgur](https://i.imgur.com/vh9kg7W.png)

![Imgur](https://i.imgur.com/rLWbzsa.png)

Check the box for reminders and tap on **SAVE PERMISSIONS**.

![Imgur](https://i.imgur.com/xapflHk.png)

Well done, you can now test your skill on a device or from the Alexa application (reminders are not available in the simulator).

## Scheduled Reminder for one-time-only

If you set reminders for one-time-only on the specific date and time, choose **scheduled** and set date and time.

![Imgur](https://i.imgur.com/OG5R85r.png)

Basically, you don't need to set the specific timezone. **User Timezone** will uses the timezone of the user's device.

## Scheduled Reminder for Recurring

Voiceflow also lets you set up automatic reminders to let you send recurring reminders to your users by enabling **Reccurence**. These reminders can be sent daily or weekly on a specific day.

![Imgur](https://i.imgur.com/ANm0T7Y.png)

### Daily

In order to set a reminder to run everyday at a specified time, choose **Daily** and fill in time (in the screenshot below, it is set to 12:00 PM). You don't need to fill in date.

![img](https://i.imgur.com/trl5QpW.png)


Then, set your reminder message and you are good to go with daily recurring messages!

### Weekly

In order to set a reminder to occur weekly, select the **Weekly** and the day you would like your reminder to occur on. In the below screenshot, a reminder is scheduled for every Monday at 12:00 PM Eastern Standard time.


![img](https://i.imgur.com/9JB0Uls.png)
