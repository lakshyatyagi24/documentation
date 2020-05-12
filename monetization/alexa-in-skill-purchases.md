## What is an In-Skill Purchase (ISP)?

An ISP allows you to sell premium content where users can opt for one-time purchases, subscriptions or consumables. Skills can still be free to use, but ISPs are useful when you want to offer premium content (e.g. upgraded versions of a game skill). Currently, the ISP feature is only available in the US, UK, GERMANY and JAPAN.

## Where to learn more about ISP?

First, you need to learn why, when and how to use ISP and Amazon made a great course on this: [https://developer.amazon.com/en-US/alexa/alexa-skills-kit/resources/training-resources/design-for-in-skill-purchasing](https://developer.amazon.com/en-US/alexa/alexa-skills-kit/resources/training-resources/design-for-in-skill-purchasing)

## What Are the Different Types of In-Skill Purchases?

* **Subscription**: Allows customers to pay a flat recurring fee for access to content. Subscriptions are best for skills that will offer a large catalog of content or be updated frequently. Subscriptions are best when the content is refreshed frequently and reliably.
* **One-time purchase (OTP)**: Allows customers to pay for access to an experience that will remain available for use. OTPs are best for skills that will offer content or experiences that are easily grouped into themes or related chunks that customers may want to experience multiple times. They are also best for experiences that can be easily expanded or remixed with the addition of similar content. You could offer themed packs that go into a customer’s library of extra content they can finish at their leisure.
* **Consumable:** Allows customers to purchase in-skill products that can be used and then purchased again as part of the skill experience. Consumables work best in skills that will offer experiences that may easily be extended with the addition of content or features.

## **Best Practices for Building an Effective Monetized Skill**

* **1. Your Skill Supports a “What Can I Buy?” Utterance**
**Currently**, in order for your premium skill to be certified, Amazon require that you [provide support for purchase requests](https://developer.amazon.com/docs/in-skill-purchase/add-isps-to-a-skill.html#buy-requests). This includes supporting utterances such as “tell me what I can buy” and “what can I shop for.”
**Requirement**: Your skill must support the specific “what can I buy” utterance. This allows customers to learn about your premium content on-demand. This must be available both before the skill is launched (“Alexa, ask [skill invocation name] what can I buy?”) and after (“what can I buy?”). By supporting the “what can I buy” utterance, you allow customers to discover and engage with your premium content, helping to accelerate familiarity with and adoption of your in-skill products.
**Recommendation**: Your skill’s response to this utterance can be as simple as a description and benefits of the premium content, or you can take it one step further and include several in-skill products to grab the customer’s attention. It is up to you whether you choose to segue this response to an upsell or to return the customer to the skill. Also, in addition to “what can I buy,” we encourage you to also support commonly used phrases like “shop,” “subscribe,” “premium,” and other variants of purchase-related syntax.
****
* **2. Your Skill Supports a “What Did I Buy?” Utterance**
**Requirement**: Your skill must provide customers with an easy way to know what they have already purchased by supporting the “what did I buy” utterance. For one-time purchases and subscriptions, reply with everything the customer has purchased, as these features do not expire. For consumables, reply with what the customer has left (you do not have to list a consumable that the customer has purchased and depleted).
**Recommendation**: We suggest you send a card to the customer’s Alexa app whenever they make a purchase, reiterating they can access their full purchase history of available products by saying, “Alexa, what did I buy?”.
****
* **3. Your Upsell Encourages Customer to Learn More about Your In-Skill Product**
**Requirement**: An upsell is when you suggest an in-skill product to the customer. You design the upsell message, which ends with some variation of “…would you like to learn more?” If the customer says yes, then they are led to the purchase prompt, or the offer, which is handled by Amazon. The offer is where important transactional details such as price is relayed to the customer.
In your upsell, do not make customers feel like they must agree to buy your product to learn more about it. Instead, aim to captivate the customer so that they accept your upsell and proceed to the offer.
**Recommendation**: You can use your upsell to specify more details about your premium content, including the product’s scope, available quantity, and/or limits.
****
* **4. You Clearly Distinguish Premium Content from Free Content**
**Requirement**: When a customer asks your skill for something, be clear in your response what is free versus premium content. When offering a list of content, be explicit. For example:
Customer:_ “Alexa, ask PodcastMaster for a podcast about space.”_
**Do**:
Your skill: _“I’ve got several space podcasts like “Around the World” or “Space Crazy,” which are free, or you can access these 2 podcasts which contain premium content: “Neil’s Frontiers” and “Space Odyssey.” Which would you like?_
**Don’t:**
Your skill: _“I have several podcasts like that. You can listen to “Around the World. “Space Crazy” “Neil’s Frontiers” or ask about more podcasts. Which do you want?”_
Customer: _“Neil’s Frontiers.”_
Your skill: _“Sorry, you’ll need a subscription to access Neil’s Frontiers.”_
**Recommendation**: For product packs, you can include the number of items or amount of content included in the premium experience. Using the above example, you could _**add**_: _“I’ve got several space podcasts like…or you can access these 2 podcasts which contain premium content: “Neil’s Frontiers,” _**_where you can purchase a 1-month subscription_**_, and “Space Odyssey”, _**_where you can purchase a 3-pack of episodes_**_. Which would you like?”_
****
* **5. Your Skill Does Not Include Pricing Details**
**Currently**, the certification guidelines [state](https://developer.amazon.com/docs/in-skill-purchase/isp-certification-guide.html#user-experience-tests) that you must not include pricing details in the upsell message. The offer, which contains the price and transaction flow, is handled by Amazon
**Requirement**: Your upsell must not include price. Instead, include details such as why your product is relevant at this moment and its benefits to the customer (refer to #3 above for more guidance on what to include in your upsell messaging).
**Do**:
Your skill: _“New subscribers can try it free for 30 days. Want to learn more?”_
**Don’t:**
Your skill: _“New subscribers can try it free for 30 days, and will then be charged $2.99 a month. Prime subscribers get it for $1.99 a month. Want to sign up?”_
**Recommendation**: You can use this opportunity to excite customers about your premium content. Using the above example, you could **add**: “**A subscription unlocks exciting new space facts about other galaxies including names and descriptions of hundreds of stars and planets**. New subscribers can try it free for 30 days. Want to learn more?”
****
* **6. Your Skill’s Detail Page Includes Information about Your In-Skill Products**
**Currently**, for your premium skill to be certified, Amazon [require](https://developer.amazon.com/docs/in-skill-purchase/isp-certification-guide.html#functional-tests) you to state that your skill offers in-skill products (but does not include pricing details), identify the different types of products that you offer (one-time purchases, consumables, and/or subscriptions), and specify how they are used.
**Requirement**: Your Alexa Skills Store detail page must explicitly state the what and the why about your in-skill product offering. For example:
 * **The what**: This skill offers premium content, in the form of [subscriptions] and [onetime purchases].
 * **The why**: You can purchase various inskill products to enhance and extend gameplay.
You can edit your Alexa Skills Store detail page by going to the Publish tab on Voiceflow or the  [Distribution page](https://developer.amazon.com/docs/devconsole/launch-your-skill.html) in the developer console and editing the “Detailed Description” metadata field.
****
* **7. Your Skill Must Handle All Possible Outcomes of the Purchase User Flow**
**Currently**, for your monetized skill to be certified, Amazon [require](https://developer.amazon.com/docs/in-skill-purchase/isp-certification-guide.html#user-experience-tests) that you build a smooth flow from free skill content to upsell or offer and back to skill content (free or premium).
**Requirement:** Here are some messages you must include in your skill to ensure a seamless upsell and offer flow:
 * **Upsell declined result:** The customer hears the purchase suggestion (the upsell) but declines. The skill resumes and continues to provide the free content.
 * **Upsell accepted, offer declined result:** The customer accepts the purchase suggestion (the upsell), but declines the purchase prompt (the offer). The skill resumes and continues to provide the free content.
 * **Upsell accepted, offer accepted result: **The customer accepts the purchase prompt (the offer). The skill resumes with the premium content available.

(source: [Amazon](https://developer.amazon.com/blogs/alexa/post/cb72c35a-4c8b-44cb-82e9-84b2198de867/checklist-ensure-your-premium-alexa-skills-are-eligible-for-amazon-promotion?fbclid=IwAR3hRc6LCJMD8rRMqxLxavoSlFdz76WU_DpngLMSMoO1RAgUaucWYa5s7N0))

Skills that meet all seven of these requirements will be considered for Amazon promotional opportunities. While Amazon can’t guarantee that your skill will be selected for promotion, following these requirements will help you deliver a great experience for customers, which will in turn help drive revenue.


