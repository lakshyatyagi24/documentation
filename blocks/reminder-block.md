In this article you will learn how to use the reminder block in conjunction with the User Info and Permission blocks.

To start you will need the User Info block to check if the user has authorized access to the Reminder for your skill.Add a **User Info** block and click on **+ Add Permission Request**

![img](https://downloads.intercomcdn.com/i/o/124660326/6928a41dff935f72277de8d0/Screen+Recording+2019-05-30+at+02.34+PM.gif)

On the **User Info's fail port**, link a **Speak block** to explain why you're using the **Reminder block** in your skill and to give the user more informations on how to authorize the skill in the **Alexa app** or on [**alexa.amazon.com**](http://alexa.amazon.com/)

![img](https://downloads.intercomcdn.com/i/o/124661940/20f51cfe8b758d0ebc0ae7f3/Image+2019-05-30+at+2.47.43+PM.png)

Finally, add the **Permission block** just after the **Speak block** to end this path.

You can then link the **Reminder block** on the remaining port of the **User Info block**

![img](https://downloads.intercomcdn.com/i/o/124663062/4b48fdc0d0f5bc58b5c9d89e/Image+2019-05-30+at+2.55.18+PM.png)

In the following example, I'm using the **reminder_text** variable as the reminder text in the **Reminder block** and I've set the reminder time to notify the user in **one minute**. As for the text, you can also use variables for the Hours, Minutes and Seconds fields.

![img](https://downloads.intercomcdn.com/i/o/124663368/0bb6bbf921d68d5c2d750b0a/image.png)

After **uploading** your skill to **Alexa**, like your future users, you must allow access to the reminder from the **Alexa application** or [alexa.amazon.com](http://alexa.amazon.com/).

![img](https://downloads.intercomcdn.com/i/o/124665400/a6fc1ee661d124a57c2a2187/image.png)

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

Well done, you can now test your skill on a device or from the Alexa application (reminders are not available in the simulator).



# **Recurring Reminders**

Voiceflow also lets you set up automatic reminders to let you send recurring reminders to your users. These reminders can be sent daily or weekly on a specific day.



### **Daily**

In order to set a reminder to run everyday at a specified time, fill in the time (in the screenshot below, it is set to 12:00 PM)



![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-Lo2Q5bJ6zXK3S-B9ivT%2F-Lo2Vk6bfA0RRfKDNFq0%2FScreen%20Shot%202019-09-05%20at%206.14.54%20PM.png?alt=media&token=4f8d5896-b0eb-4189-a8b0-621cd989aa9f)

Once you have picked a time zone, just set your reminder message and you are good to go with daily recurring messages!

### **Weekly**

In order to set a reminder to occur weekly, select the "Weekly" tab and select the day you would like your reminder to occur on. In the below screenshot, a reminder is scheduled for every Monday at 12:00 PM Eastern Standard time.

![img](https://gblobscdn.gitbook.com/assets%2F-LgK_X2m6IAIYcINBjCj%2F-Lo2Q5bJ6zXK3S-B9ivT%2F-Lo2WXI5umOWcFvR-Ieq%2FScreen%20Shot%202019-09-05%20at%206.22.58%20PM.png?alt=media&token=a52efa21-96fa-40d4-8168-7d898dc7c026)
