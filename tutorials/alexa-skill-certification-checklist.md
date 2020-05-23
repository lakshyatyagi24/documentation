# Alexa Skill Certification Checklist

Get help with submitting your Alexa skills successfully to the Alexa skill store.

## **What You'll Learn 🧠**

- Alexa's certification checklist
- How the process works
- How long certification typically takes

# **REQUIRED: 5 Things You Need to Submit Your Skills**

✅ Functional Help & Stop intents ✅ Help intent with a question ✅ Functional skill with all outcomes and paths tested ✅ Proper, non-misleading Alexa store information for publishing ✅ Privacy Policy & Terms of service (optional unless Children's skill) 

## **1. HELP & STOP INTENTS**

Every Alexa skill needs to have a functional Help & Stop intent that the user can access at any point within the skill. 

To make this easier for our users, we added the Help and Stop commands within the Start block by default. 

All you have to do is customize the speak blocks within these flows (if you wish). 

## **2. HELP INTENT WITH A QUESTION**

Within your Help intent, you must have a functional question which asks the user whether they would like to exit the skill, or remain in the skill.

The format should look something like this,

 ![img](https://cdn.zappy.app/8e6ee8bf655e6e52c454ff15a71fa389.png)


## **3. FUNCTIONAL SKILL WITH ALL OUTCOMES AND PATHS TESTED**

Every Alexa skill submitted to the Alexa store must be fully functional with every possible path and action within your skill being tested. A skill will be deemed as broken by Amazon if it abruptly ends without warning - even if that is the intended function of the skill.

The best way to test the functionality of your skill is to run a functional test on the Amazon Developer Console. You can find this under the 'Certification' tab.

![img](https://downloads.intercomcdn.com/i/o/113032933/e2b099269e85ebb67f72a49e/Screen+Shot+2019-04-02+at+11.11.04+AM.png)


## **4. PROPER, NON-MISLEADING ALEXA STORE INFORMATION FOR PUBLISHING**

When publishing your skill, do not use misleading or untrue information within your skill description, name, or invocation name. Be very clear and simple what your skill does, who the intended audience is, and how to activate the skill. 

## **5. PRIVACY POLICY & TERMS OF SERVICE**

If your Alexa skill:

- Has in-skill purchasing
- Is targeted at Children
- Collects user information
- Contains advertising

If your Alexa skill has any of these, you must have a valid Privacy Policy & Terms of Service. If you do not have one, Voiceflow will provide you with one - however - you are at your own risk for using our stock policy. For advanced skills we recommend having your own policy drafted. 

Not having a privacy policy whilst being in one of these 4 categories will result in your skill being rejected from certification.