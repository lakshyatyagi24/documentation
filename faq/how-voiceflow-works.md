# How Voiceflow works

Learn how Voiceflow's platform works.

**Voiceflow provides an easy to use and fast visual interface for building voice apps on Amazon Alexa & Google Assistant.**

The Voiceflow creator platform links to your existing Amazon Developer & Google Developer accounts. 

When you create a project on Voiceflow, it is agnostic to any platform until you upload. Upon uploading to Alexa or Google, Voiceflow generates an interaction model which acts as the "front-end" of your voice app.

![img](https://downloads.intercomcdn.com/i/o/107853165/e5733c167ff0d98b1d2c1d74/how.png)

Your voice app will have its backend point to Voiceflow which will generate a system of logic specific to your app to power the interface. This will also allow Voiceflow to provide you with an easy-to-implement analytics system.

You can modify the interaction model within ASK or the Actions console to add more custom elements. However, every time Voiceflow uploads your project it will override previous custom changes made in either native console (ASK or Actions).