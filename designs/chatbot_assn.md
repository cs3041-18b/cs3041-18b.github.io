---
layout: page
title: Design for Tension
exclude: true
---

- **Group size:** Teams of 4
- **Demo Day:** 11/27 _in class_
- **Design Doc Due:** 11/29, 5:59 PM

In this design sprint, you will create a chatbot that **attempts to tackle a tense topic, such as political divides**. This is (intentionally) an overly lofty design objective. Your goal isn't to solve your problem, but to try and tackle one small component of it. For example, you could try to create a bot that pushes people outside of their filter bubbles by pointing them towards news sources they might be unlikely to see. Maybe you create something that forces people to reflect on their own beliefs for just a moment.

**Be ambitious.**

As you should have seen from your reading, conversational interfaces such as chatbots or voice interaction (Amazon's Echo, Siri) present a unique set of challenges - how do you make interaction seem natural? How do you engage users without annoying them? What are the advantages of a conversational interface vs. a website? - are you leveraging them?

To do this, you will go through the stages of design that we have discussed to this point. For this assignment, we will focus more intensely on **user testing** your prototypes. Expect to spend some time with students either in or outside of class.

### Do a Little Homework
We won't have time to fully engage with ethnographic methods in this module, but if you don't have any ideas, try searching around the internet first. What issues have caused political polarization and/or continue to propagate it (what is the problem?)? What solutions have been proposed? Can you help?

**You should determine a rough framing for your chatbot** - What user group is it designed for? What will their expectations be? What are the overall goals of your application? What platform are you targeting (user expectations for a texting bot are different from a Slackbot)?

At this point, you should be able to articulate a _how-might-we_ statement. For example, _how might we build a Slackbot to help teenagers be exposed to opposing viewpoints_?

### Ideate
**Brainstorm conversations that will reach your objective.** You can do this informally with your own team. How can you guide someone to a goal via conversation? What information do you need? How quickly can you get to that goal? Where can it go wrong?

Experiment with a number of approaches. Establishing a personality or identity for your bot will be important. This should match your audience as well as your design goals. Remember basic interface design rules - allowing people to feel in control of the situation, making their options clear, etc.

**Formalize your conversation into concrete rules that you can follow.** For example, look at the flow charts presented in [_How to design a robust chatbot interaction_](https://uxdesign.cc/how-to-design-a-robust-chatbot-interaction-8bb6dfae34fb). This will allow you to rapidly iterate on your idea in the next section. You may also do this in Google Docs.

### Formative User Testing

**Before you start programming,** you can iterate rapidly on this design through informal user testing. Have one person on your team act as the 'bot' with someone who is unfamiliar with your system (someone in another group, a friend, or a family member). Try to have a conversation with that person by following you rules above (stick to them!). This should quickly highlight cases in which your rules fail or ways in which your design goals are not met. Remember to document this process, potentially with video, or, more likely transcripts. You'll want to reference these artifacts in your reflections later on. 

Given that we won't have class on Tuesday, Nov. 20th, my recommendation is for groups to prototype their chat ASAP, and then for each group member to conduct at least one user test before the 20th. During class time on the 20th, meet online (via Skype etc.), discuss the results of your user testing, and make changes to your chat model. Then implement your chatbot (preferably using Flow XO) by demo day on the 27th. You are free to modify this schedule as needed as long as your chatbot is ready to go in class on the 27th! 

**REMEMBER TO BE DELIBERATE ABOUT YOUR USER TESTING**. Although getting feedback on the entire chatbot experience is important, are there specific aspects that you'd like to focus on? Perhaps each group member could test a slightly different variation in order to determine which responses/questions lead to the best outcomes. Think about what types of user information will help you to design your final chatbot and design your tests accordingly.

### Build and Refine based on Technical Limitations
Now you're going to do the best you can to create your chatbot (see the sections below for some tips on developing your chatbot). But this is also when you run into a core challenge in HCI - you might not be able to recreate exactly what you imagined. How can you reshape your interactions without compromising your design goal?

Develop your chatbot and then **test it with real people**. Don't just assume it's effective. Try it out. There are several options for building your chatbot:

- [Flow XO](https://flowxo.com): **HIGHLY RECOMMENDED**. Options to connect to multiple platforms, relatively straightforward construction environment, and some nice plugins to increase the capabilities of your bots. Also includes an interface to API.ai if you want to leverage more powerful NLP + ML. [Getting Started](https://medium.com/flowxo/get-started-with-flow-xo-747eb1f6f97b) \| [Some Tutorials](https://medium.com/flowxo)

- [Chatfuel](https://chatfuel.com/): A flow-based chatbot for Facebook Messenger. You will need to have a Facebook account to use Chatfuel and create a a Facebook Page (at least as far as I can tell). _HINT: You can create a Facebook Page and then immediately unpublish it... but still use the app_

- [Build a Slackbot with Python](https://medium.com/@nidhog/how-to-make-a-chatbot-on-slack-with-python-82015517f19c): Note that this will require you to build much more from scratch... and may limit the capabilities of your bot.

- [Talkbot](https://talkbot.io): another flow-based chatbot constructor for Facebook. Same rules apply as Chatfuel. Note that this is only a 15 day trial, so if you use it, make sure it overlaps with deadlines.

- [Botsify](https://botsify.com/): _another_ Facebook-based chatbot creator.


## Deliverables
- As always: Your design reflection as a Medium blog post. Since your bot may not live forever, **you WILL need a demo video that captures all important conversational aspects**. A single video can be made for the entire group, or each member can make their own individual video (or some combination of the above).
  - For this sprint, be sure to reflect on your interaction with users and how that drove your design
- Make sure that your bot is accessible to chat during our demo day.
