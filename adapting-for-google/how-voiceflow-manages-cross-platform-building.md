# How Voiceflow manages cross-platform building.

Learn how Voiceflow works with both Alexa and Google at the same time.

Voiceflow makes it easy to build Alexa Skills & Google Actions - at the same time, using the same project and canvas.

Here are the things you need to know when developing cross-platform for Alexa & Google:

# **1. How to switch between Google & Alexa development**

When inside a project, you can seamlessly switch between developing for Google and Alexa. To switch platform, flip the switch on the navigation bar:

![img](https://cdn.zappy.app/24f204fca00aab4a50fab9a05c581af6.png)

# **2. What happens when you switch your development platform**

Alexa and Google are similar platforms that still have many differences. Depending on the availability of a feature for each platform, you will have access to the blocks in the Platform section.

For example, the Purchase block is only available on Alexa currently. Below, when we are switched to Google, we can't see it in the Platform section.

![img](https://cdn.zappy.app/b2cb146c81b84022fdcf936ddd904c00.png)


# **3. The platform variable**

The "platform variable" is the built-in variable that allows you to determine what platform the user is on when they activate your voice app.

You can find the platform variable within the Model window (press M to open the window) in the "Variables" section. Built-in variables cannot be deleted, and are indicated by the 'Built in' info.

![img](https://cdn.zappy.app/179594a66e705ae0cb888e5b333d8a88.png)

Using the {platform} variable, you can determine what platform the user is on. This is handy when you want to have a different experience for Google Users vs Alexa Users.

## ****How to separate platforms within the same project****

To separate platforms, we want to use an IF block at the very beginning of our project and split users depending on their platform. Using our IF block, we want to have the two following conditions:

IF {platform} = google [go down path 1]

IF {platform} = alexa [go down path 2]

Within the IF block, it looks like this:

![img](https://cdn.zappy.app/43fa8e8544d68aecddbf43542b9aaf90.png)

Within our project, we can now split users depending on their platform - and have them head into different flows. Example below:

![img](https://cdn.zappy.app/4c127477a28b20ddd40940e5e2e5be38.png)

Now, using the {platform} variable and flows, you can build entirely different user experiences for users on either Alexa or Google - all within the same project.

The {platform} variable can also be used to separate experiences within your skill - for example - if the user opts for payments and this is only an Alexa feature, use the IF block to separate users depending on the platform they're on so that Alexa users proceed to payment, and Google users pass right by or are informed payment will be coming soon.