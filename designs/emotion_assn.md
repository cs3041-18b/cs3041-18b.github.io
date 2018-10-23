---
layout: page
title: Design for Wellbeing
exclude: true
---

- **Group size:** Teams of 4
- **Demo Day:** 4/19 _in class_
- **Design Doc Due:** 4/23, 11L59 PM

In this design sprint, we will be considering what it will mean for our computer devices to be attentive to us in ways that haven't in the past. **We'll use [Affectiva libraries](https://knowledge.affectiva.com/v3.3/docs/getting-started-with-the-emotion-sdk-for-javascript) to design a website that responds to user emotion, with the end goal of [promoting wellbeing](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6679310)** (broadly defined on purpose!).

The idea of using technology to not only get something done, but also promote health and wellbeing, is an emerging, but important topic. Startups such as [happify](https://my.happify.com/), [smiling mind](http://smilingmind.com.au/), [spire](https://spire.io/), [muse](http://www.choosemuse.com/), and [empatica](https://www.empatica.com/) all push to help make people more compassionate or wiser or happier or healthier. [_Positive Computing_](http://www.positivecomputing.org/), a term coined by Rafael Calvo and Dorian Peters of University of Sydney, is increasingly being pointed to [an important emerging movement in technology design](https://www.washingtonpost.com/news/innovations/wp/2015/01/30/positive-computing-the-tech-buzzword-you-need-to-know-for-2015/?utm_term=.7faa5fd7fbe8). This is your chance to explore that space. 

### The Design Process
To start out this design sprint you should....

...

...

...

...

We're getting towards last third of the term, which means it's time for me to stop telling you how to apply the design process. Instead, you'll need to work out yourself how best to **ideate**, **prototype**, and **test** in a new domain. _This is the most important outcome of the course_. Technology will rapidly on shift and move for years after you leave WPI. If you can leave HCI with a process and methodology that informs _good design_ in any context, then this course is a success.

### Some Tips Before You Start

- **Play with the [Affectiva library](https://knowledge.affectiva.com/v3.3/docs) first to understand the data.** Before you can understand how a system might react to data, you need to understand the data itself. The best way to do this is  to visit [this demonstration which gives you access to the raw data as it monitors your emotions](https://jsfiddle.net/affectiva/opyh5e8d/show/) (you'll need a computer with a webcam). What seems reliable? What doesn't? You certainly won't use all of it. I would probably focus on a single dimension. You can also see how it [tracks emotions in response to YouTube videos](https://affectiva.github.io/youtube-demo/).

- **Design a SIMPLE, but meaningful response** You're quickly going to find out that emotion data is _very_ messy (welcome to the wild world of user state sensing!). That means that you can expect to spend quite a bit of time just fighting with the data. As a result, rather than ideate big, ambitious systems (which I love, but you probably won't have time for), brainstorm _simple_ changes or interactions that could have a meaningful impact. For some inspiration, it might be worth looking through [projects by the Affective Computing group at MIT](http://affect.media.mit.edu/index.php).

- **Consider the usefulness of a 'sometimes right' emotion detector.** The reality is that no matter the preprocessing, Affectiva is still likely to be wrong a fair amount of time. This means that some interactions are more appropriate than others. You wouldn't want an eject button in an airplane hard-wired to someone's emotional responses (okay, extreme example... but you get the point). But if you highlighted the text that someone wrote based on their emotions, a misclassification or two doesn't undermine the entire application. We talk about some of the tradeoffs in these adaptive strategies in section 4.2 of [a paper we published about brain-computer interfaces](http://www.danafergan.com/publications/solovey2015designing.pdf)

- **Focus on what should _trigger_ your system's response.** While the response itself is important, **when** that change occurs is possibly even more important. Consider what might happen if you made a change *every* time affectiva detected that a person was angry. Remember that Affectiva frequently samples data, so you may not want to respond with _every_ single state prediction, especially when it is messy. Some approaches I've seen in the past include generating a moving average of recent data to smooth out noisy data... then setting thresholds for response.

- **A warning.** Because of a combination of messy input + web programming, this has the potential to be the most challenging _technical_ project of the term. Take this into account when allocating your time! Even in the earliest stages, it's worth having someone on the team begin familiarizing themselves with how to respond to and manipulate webpages. To help enforce this, **on Tuesday, April 17, we will have a team quiz rather than an individual quiz**. The quiz will involve both content from the reading _as well as_ simple HTML + javascript questions that are directly related to the given demonstration code (see below).

### Deliverables
- As always: Your design reflection as a Medium blog post. **You WILL need a demo video**.
- Your site should be publicly accessible so that others can visit it. **Include this link in your design doc**


## Some Technical Hints

For some quick examples/templates that you can work off of, consider the following generated by Gabbi LaBorwit:

- [A basic template](../docs/basic-template.zip)
- [A demo app that changes the filter on the webcam based on your emotion](../docs/customized-detector.zip)

To run these apps, you can either put them up in your server space on the Linux server or you can run them locally. Remember, to run them locally, you'll still need to create a local server:
- use command-line to navigate to project folder and type `python -m SimpleHTTPServer 4444`
- Navigate to the page in your web browser at `127.0.0.1:4444`

#### Javascript, DOM, and jQuery

Your output may be a webpage that responds in some way to the emotional content of the user. This will likely involve manipulation of HTML using javascript. While I provided resources in the readings to help get someone up to speed with [jQuery](https://jquery.com/), there are many, many specialized javascript libraries that may accomplish your goals more simply (could you combine this library with p5js? Maybe...). I would recommend that you search for them before trying to recreate the wheel. **If you know better tools, use them.**
