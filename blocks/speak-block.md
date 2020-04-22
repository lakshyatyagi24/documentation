# What You'll Learn 🧠
- What the Speak block does
- How to make your Voice Assistant speak
- How to use different Alexa voices throughout your skill
- How to use variables within the Speak block
- How to use 'Output Random Entry' 

## Overview
The Speak block allows you to output speech and audio for the user. With the Speak block, you can have your assistant talk to the user in a variety of voices, as well as play audio files.

## Speak block basics

To output speech, drag in a Speak block and click on it. On the far left panel, you'll see a text box where you can enter text to output to the user.


You can type anything!

## Using different voices

With the Speak block, you may use several different voices - categorized by accent region. When you drag in and click on a Speak block, you can type in the text you would like to output, and then choose the voice you would like to be used.


## Multiple Voices in One Speak Block
Within one Speak block you can say several things in different voices. Below, you can see output in two sentences - each in a different voice by adding another section. 


## Using Variables in the Speak Block
You can use variables within your speak blocks to personalize the user's skill experience, or convey dynamic information such as the answer to a calculation, or an API response. 

To use a variable in the Speak block, hit the right facing curly brace button '{' which will pop the drop-down list for available variables to use in your speak block. 


You can use multiple variables in a single Speak block.

## Playing Audio Files
Using the Speak block you can have play short audio files for the user. To do this, within the Speak block hit "Audio".



When you do this, you'll create a new section for an Audio file which will be played in order with your Speak block sequence, or at random if you have that option toggled. 
Here, you can upload an audio file to be hosted on Voiceflow, or, you can link to a file you are hosting on your location. 

Once you have added a file you will see the length of the file, and be able to preview the sound. You are able to traverse through your audio file by clicking on different parts of the audio player.




### Alexa specific limitations:

Files for the Speak block can only be up to 240 seconds if uploading to Alexa, and will be played at a reduced sound quality due to Alexa technical restrictions.

When using the speak block, if you were to use back to back blocks with audio uploaded, the audio time within them is added. This is because all blocks will process concurrently until the user is faced with user input (i.e. choice block, interaction block, etc.) The limit applies to the total, until there is user input, then this limit resets.
For example: using two back to back speak blocks with 2 mins and 3 mins wouldn't work, because that would total five mins. But using speak/choice/speak would, because the time is 'reset' after user input.


## Outputting Random Speech
You can output a random 'section' from within your speak block. For example, if you were to have two different greetings, or two different sound effects, you can output a random one to play, rather than play all the sections in sequence as a normal Speak block does.

To do this, hit the three dot button and select "Randomize Outputs". To reset to sequential outputting, hit the three dot button and select "Unrandomize Outputs".



## Change the Vocalization of Your Text with SSML Tags
To output different sounding speech, you may use SSML tags within you Speak block. SSML is a special format created to modify how voice assistants talk.

We have an in-depth tutorial on using SSML tags here.