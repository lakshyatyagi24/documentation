**# Intents and slots** 





**## Intents** 



Intents allow you to understand and capture the **Intention** of what a user is saying.



Creating an intent consists of two parts:



\1. Giving your intent a name

\2. Giving your intent utterances



**### Naming your intent**



The name of your intent does not affect your intent in any way. It is a way for you or other collaborators on your project to easily identify your intent. A good name should be easy to understand and clearly define what the intent is looking for.



<img src="https://i.imgur.com/9ohSsSU.png" alt="img" style="zoom:50%;" />



**### Utterances**



Utterances are examples of what your user can say to trigger your intent. You should include as many utterances as possible to give your intent a better chance at accurately being triggered when a user speaks.



**### Intent Example**



An example of an intent with an utterance is an intent named `order_pizza` which looks for the many ways a user might want to order a pizza. An example of an intent might be::



Name: `order_pizza`



\- What are your options for ordering a pizza?

\- How can I order a pizza?

\- I want a pizza

\- I want to order a pepperoni pizza

\- I want to order a cheese pizza

\- I want to order a vegetarian pizza

\- I want to order a pizza



As you can see, there are numerous ways to order a pizza and we need to account for as many of them as possible when designing our projects.



<img src="https://i.imgur.com/AAbTBe8.png" alt="img" style="zoom:50%;" />



**## Slots**



Slots act as variables that allow you to take in specific words that a user is saying in their utterances. Slots allow you to save portions of what a user says as well as provide a larger variety of options instead of having to build a custom utterance for every intent.



An examples of Slot may be:



Slot name: `{toppings}`



Slot utterances: cheese, pepperoni, vegetarian, canadian, hawaiian



You can now use this slot inside of an utterance like the following:



Name: `order_pizza`



\- I want to order a pizza

\- I want a `{toppings}` pizza

\- I want a pizza



The slot will look for any of the values that were specified in the slot utterance (cheese, pepperoni, vegetarian, canadian, hawaiian) and will trigger this intent. The value that is spoken by the user will also be saved to the slot and have the ability to be used anywhere throughout Voiceflow.



<img src="https://i.imgur.com/Rp5QBkc.png" alt="img" style="zoom:50%;" />





Synonyms can also be added for each of the utterances of your slot. These will allow your user to say a variety of words and trigger the root word of the synonym. For example, if the user says veggie or mushroom, the word vegetarian will be triggered and saved in your Slot.



<img src="https://i.imgur.com/5dvuF5T.png" alt="img" style="zoom:50%;" />



<img src="https://i.imgur.com/JHFgdQd.png" alt="img" style="zoom:50%;" />