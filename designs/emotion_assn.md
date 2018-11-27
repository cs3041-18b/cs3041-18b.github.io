---
layout: page
title: Design for Wellbeing
exclude: true
---

- **Group size:** Teams of 4
- **Demo Day:** 12/4 _in class_
- **Design Doc Due:** 12/6, _before class_ [submit](https://docs.google.com/spreadsheets/d/1RpuIJYlHO48eitI6_wFl1ue-eHDES5EnkC9fUxvFW90/edit?usp=sharing)

In this design sprint, we will be considering what it will mean for our computer devices to be attentive to us in ways that haven't in the past. **We'll use [Affectiva libraries](https://knowledge.affectiva.com/v3.3/docs/getting-started-with-the-emotion-sdk-for-javascript) to design a website that responds to user emotion, with the end goal of [promoting wellbeing](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6679310)** (broadly defined on purpose!).

The idea of using technology to not only get something done, but also promote health and wellbeing, is an emerging, but important topic. Startups such as [happify](https://my.happify.com/), [smiling mind](http://smilingmind.com.au/), [spire](https://spire.io/), [muse](http://www.choosemuse.com/), and [empatica](https://www.empatica.com/) all push to help make people more compassionate or wiser or happier or healthier. [_Positive Computing_](http://www.positivecomputing.org/), a term coined by Rafael Calvo and Dorian Peters of University of Sydney, is increasingly being pointed to [an important emerging movement in technology design](https://www.washingtonpost.com/news/innovations/wp/2015/01/30/positive-computing-the-tech-buzzword-you-need-to-know-for-2015/?utm_term=.7faa5fd7fbe8). This is your chance to explore that space. 

### The Design Process
We're entering the final third of the term, which means it's time for me to stop telling you how to apply the design process. Instead, you'll need to work out yourself how best to **ideate**, **prototype**, and **test** in a new domain. _Understanding how to do this is the most important outcome of the course_. Technology will rapidly on shift and move for years after you leave WPI. If you can leave HCI with a process and methodology that informs _good design_ in any context, then this course is a success.

Discuss with your group members how you'd like to brainstorm ideas. After you've finished brainstorming and chosen an idea(s) to further explore, discuss the best methodologies for prototyping and user testing. What specifically are you going to test? How will your prototypes help conduct these tests? Think about each of these choices carefully, and be sure to record the reasoning behind each in your design reflection, as well as whether they proved to be good or bad decisions. Making a bad choice in this context in perfectly fine, especially if you can articulate why your decision didn't pan out and what you'd do differently next time.

**You will have time in class on 11/29 to work on this module (estimated ~1 hour)**. This time could be used to test quick prototypes on other students in the class, for ideation, or to develop your prototype implementations. It's up to you.

### Some Tips Before You Start

- **Play with the [Affectiva library](https://knowledge.affectiva.com/v3.3/docs) first to understand the data.** Before you can understand how a system might react to data, you need to understand the data itself. The best way to do this is  to visit [this demonstration which gives you access to the raw data as it monitors your emotions](https://jsfiddle.net/affectiva/opyh5e8d/show/) (you'll need a computer with a webcam). What seems reliable? What doesn't? You certainly won't use all of it. I would probably focus on a single dimension. You can also see how it [tracks emotions in response to YouTube videos](https://affectiva.github.io/youtube-demo/).

- **Design a SIMPLE, but meaningful response** You're quickly going to find out that emotion data is _very_ messy (welcome to the wild world of user state sensing!). That means that you can expect to spend quite a bit of time just fighting with the data. As a result, rather than ideate big, ambitious systems (which I love, but you probably won't have time for), brainstorm _simple_ changes or interactions that could have a meaningful impact. For some inspiration, it might be worth looking through [projects by the Affective Computing group at MIT](https://www.media.mit.edu/groups/affective-computing/projects/).

- **Consider the usefulness of a 'sometimes right' emotion detector.** The reality is that no matter the preprocessing, Affectiva is still likely to be wrong a fair amount of time. This means that some interactions are more appropriate than others. You wouldn't want an eject button in an airplane hard-wired to someone's emotional responses (okay, extreme example... but you get the point). But if you highlighted the text that someone wrote based on their emotions, a misclassification or two doesn't undermine the entire application. We talk about some of the tradeoffs in these adaptive strategies in section 4.2 of [a paper we published about brain-computer interfaces](http://www.danafergan.com/publications/solovey2015designing.pdf)

- **Focus on what should _trigger_ your system's response.** While the response itself is important, **when** that change occurs is possibly even more important. Consider what might happen if you made a change *every* time affectiva detected that a person was angry. Remember that Affectiva frequently samples data, so you may not want to respond with _every_ single state prediction, especially when it is messy. Some approaches I've seen in the past include generating a moving average of recent data to smooth out noisy data... then setting thresholds for response.

- **A warning.** Because of a combination of messy input + web programming, this has the potential to be the most challenging _technical_ project of the term. Take this into account when allocating your time!

### Deliverables
- As always: Your design reflection as a Medium blog post. **You WILL need to include a demo video, this can be shared by group members or created individually**.

## Some Technical Hints

For some quick examples/templates that you can work off of, consider the following generated by Gabbi LaBorwit:

- [A basic template](../docs/basic-template.zip)
- [A demo app that changes the filter on the webcam based on your emotion](../docs/customized-detector.zip)

To run these apps, you can either put them up in your server space on the Linux server or you can run them locally. For some examples, you might need to create a local server:
- use command-line to navigate to project folder and type `python -m SimpleHTTPServer 4444`
- Navigate to the page in your web browser at `127.0.0.1:4444`

... although I've also had success using the Affectiva API without using a web server i.e. just dragging your HTML file into a browser window to load it.

#### Javascript, DOM, and jQuery

Your output be a webpage that responds in some way to the emotional content of the user. This will likely involve manipulation of HTML using javascript. There are many, many specialized javascript libraries that may help you accomplish your goals (could you combine Affectiva with p5.js?). I would recommend that you search for them before trying to recreate the wheel. However, you can do a lot with plain vanilla JS these days. Ask questions in the Slack channel if you're looking for hints on the best way to realize an interface concept.