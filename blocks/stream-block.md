## **What you'll learn**

- What the stream block is and how it works
- How and when to use the Stream block

**What is the Stream block** 



 The stream block allows you to stream audio files longer than 90 seconds at a higher quality than the audio block. The stream block supports the following file types:

- MP3
- AAC/MP4
- HLS/M4U

You can learn more about the kinds of audio [files supported by Alexa skills here](https://learn.voiceflow.com/build-alexa-skills-without-coding/alexa-skill-audio-files).



![img](https://i.imgur.com/cv3p2Jd.png)

**Stream block vs Audio block** 

The stream block works very differently than the [Audio block](https://learn.voiceflow.com/build-alexa-skills-without-coding/basic-blocks-tutorials/audio-blocks). Unlike the audio block, when a user hits your stream block - the user is **actually leaving your skill**. This functionality was built-in by Amazon. The user only returns to your skill if they say one of the Stream block's keyword functions. The accepted functions are below:

- Alexa, Pause
- Alexa, Next
- Alexa, Previous

Unless the user says one of these keywords while still streaming audio from the Stream block, your skill will be officially over. This is why it is suggested you use Audio blocks for almost all cases unless impossible. With Audio blocks, the user is still within your skill, and can access Command blocks and other in-skill features.

**Adding audio** 

To add audio files into the Stream block, you need to add a link to the audio that you want to stream. You can either paste the direct link into the text box or you can save it in a variable and use the variable directly in the textbox. **You must use an https url because it is a requirement to pass the certification of your skill with Alexa.**



![img](https://i.imgur.com/Z56UDCj.png)

**Loop audio by default** 

When you enable 'Loop audio', you are looping the audio files within the Stream block until the user either stops the skill, or, if you have Audio player functions enabled, asks for an audio player function. This means that the audio will continue to loop until the skill is stopped, or the user asks 'Alexa, next/previous/stop/pause'. 



**Audio player functions**

 The stream blocks functions can be activated at any time when using the Stream block. For the user to activate a function, they must say the wake word followed by the function they desire (e.g 'Alexa, next').

With Voiceflow, you can determine what happens next when the user says one of the pre-defined Stream block functions by using the next and previous outputs of the block.

When the user is in a Stream block and uses any of the pre-defined functions, they will be routed through the corresponding port. As an example, if the user says 'Alexa, next' while in your stream block - you can use a speak block and connect it to the next port, then have Alexa say the name of the next song before going into another stream block. That looks like this:

![img](https://i.imgur.com/GowDurC.png)





## Video 


