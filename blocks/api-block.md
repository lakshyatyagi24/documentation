## **What you'll learn**

- What the API block is and how it works
- How to use the API block



## What is the API block



The API block allows you to hit any API on the internet. This could mean Google sheets, Twitter or even your own services can be hit to send and retrievee information. The API block works similarly to any regular API request you would make. Because API's can be so vast and the rules are dictated by the specific API creator, you need to follow their documentation in order to make it work effectively. 

![img](https://i.imgur.com/BC2pYUm.png)

## How to use the API block

The API block consists of several parts:

- The request type
- The endpoint
- Headers, Body and Params
- Saving to variables
- Test Request 

![img](https://i.imgur.com/vThs844.png)

### Request types

There are 5 standard request types available through the API block.

- GET - Retrieves information from your data source
- POST - Creates information in your data source
- PUT - Completely updates information in your data source
- PATCH - Partially updates information in your data source
- DELETE - Deletees information in your data source

## Endpoint 

The endpoint is the URL that points to your API. Similar to website URL, your endpoint URL is where your requests will be sent to speak with your API.

An example API could look like the following:

```
https://api.twitter.com/1.1/search/tweets.json
```

### Headers, Body and Params

Your API may need additional information in order to give you information. This information can include data like Usenames, Passwords, Authentication tokens, etc. Typically these will be provided by your API provider in their documentation.

### Saving to variables

Once you have succesfully made an API call, you will receive back a JSON object. Once you have this, you will likely want to save some of the information you got back onto Voiceflow to speak back to the user, send to another API or compare to something that a user has said. You can do this using the "Transform into Variables section". Simply copy the object path, and paste it into the text box. Then select a variable that you would like to save to.



### Test Request

Testing the request will allow you to make sure that your API call is working before moving on in your project. If it succeeds, you will see a message saying "Success". You can click on the copy icon beside portions of the JSON to copy the object path and save it into a variable.
