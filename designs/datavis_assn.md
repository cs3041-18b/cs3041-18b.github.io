---
layout: page
title: Design for Understanding
exclude: true
---

- **Group size:** Teams of 4 (likely working pairs)
- **Demo Day:** 3/30 _in class_
- **Design Doc Due:** 4/2, 11:59 PM


## Overview
Mapping data to visual features is a powerful method for communicating information by leveraging the rapid perceptual pathways in our brain.  In this design sprint, you will use visual methods to communicate data - but for different end goals. Your job is to use two different lenses to approach the same dataset:

- **Clear communication and reasoning:** In this framing, you can assume that you have the user's attention and that they do not need training in traditional charts. Use your knowledge of perception + data representation to construct a series of graphs that give an in-depth, unbiased, clear portrait of your data.
- **Persuasive communication and storytelling:** In this framing, your goal is to represent the data (visually, through audio, through interaction) in the most _compelling_ way possible. What will have the most long-lasting impact on users? What will they _remember_?

Since you'll be working in teams of four (4) for this project, I recommend that you split your team into pairs. However, depending on your design, you may choose to allocate your resources in the way you see best.

### Choose a Dataset
Before you begin, choose a dataset. While you may use any dataset, be aware that cleaning the datasets into a usable format can be a major headache. You can use any dataset that you find online. Here are a few good starting points.

- [_CORGIS (The Collection of Really Great, Interesting, Situated Datasets)_](https://think.cs.vt.edu/corgis/): cleaned, well-organized datasets that should be very simple to load into your program.
- [_Datasets underlying FiveThirtyEight stories_](https://github.com/fivethirtyeight/data): Mostly cleaned, but may come in different formats.
- [_Data is Plural newsletter_](https://docs.google.com/spreadsheets/d/1wZhPLMCHKJvwOkP4juclhjFgqIY8fQFMemwKL2c64vk): fascinating datasets, but may not be cleaned/curated

### Your Technology
Both are valuable perspectives, and there are tradeoffs between the two. To help match your tools with your objectives, we'll use two.

- [**Vega**](https://vega.github.io/vega/) or [**Vega-Lite:**](https://vega.github.io/vega-lite/) These are both templating tools that sit on top of the very popular d3js visualization library. While they are less expressive than d3js, they will allow you to rapidly (hopefully) construct data visualizations. Vega will allow you to be a little more creative and integrate interaction (_recommended_).

- [**P5js**](https://p5js.org/): p5js is an expressive, accessible javascript library that enables pixel-level control. While it is more difficult to construct basic charts than vega or vega-lite, it empowers more creative interpretations of data that are either more abstract or that incorporate sound.

### Your Two Portraits

- _For Clear Communication:_ You should construct a series of graphs that tell the story of the data. The properties of the data should align with your chart choice. Together, your charts (_AT LEAST_ 3) should explore the data from different perspectives. For example, [Airline on-time performance](http://square.github.io/crossfilter/). While you may not have the degree of interaction of this demo, note how it gives different perspectives of the same data.

- _For Persuasion:_ There are very few guidelines here. I would encourage you to be creative and optimize for impact. For example, here is a visual/audio interpretation of data that I created (note: you need audio): [15 Years of Mass Shootings in America](https://github.com/evanpeck/15-Years-of-Mass-Shootings-in-America).


### Your Design Process
Before you got to this class, you should have read about the [five design-sheet (FdS)](http://fds.design/) approach for information visualization. You should walk through [all five stages](http://fds.design/wp-content/uploads/2015/06/five-design-sheet-approach-JCR.pdf) of FdS. Make sure to get feedback from other students in the class as part of your design process!

> Over the course of the term, I am going to give fewer and fewer detailed instructions about how to run your design process. This is intentional! As we become more familiar with it, I expect you to be able to apply it yourself to any new technological domain

### Build it.
Just build it. Note that you may run into tensions between your imagined visualization and the one that you have time to create. That's okay! Technical tradeoffs are a reality that any designer must encounter. Adjust your design (as needed), and be sure to discuss these tradeoffs in your design document.


## Deliverables
- As always: Your design reflection as a Medium blog post. Like the last assignment, **you do not need a demo video**
  - Be sure to reflect on the contrast between the two ways you have chosen to communicate your data. There are certainly tradeoffs between the two.
- Both of your designs should be hosted on WPI's servers with publicly accessible links. These links should be clearly included into your design reflection.

-------------------
## Some Tech Tips
Over the past summer, I had a colleague complete each of these assignments to help me determine where students might encounter problems. From this project on, I will include her notes on the tech you'll be using.


### Getting Started: Creating a website
_If you've never hosted a website on WPI's Linux servers before, start by following the steps [here](https://its.wpi.edu/Article/Create-a-Personal-or-Group-Website-at-WPI)._

-------------------

## Tips for Getting Data into p5js

### Getting started
  1. Download the [complete p5.js library](https://p5js.org/download/) and unzip the file.
  2. Go through [this](https://p5js.org/get-started/) ~2 minute tutorial. It's extremely helpful and even if you already know what you're doing you get to make a pretty fun demo and you'll need the documents later on in the assignment.


### Creating a data table
  1. Once you've chosen a dataset to work with, download the data as a `.csv` file and save it in your working directory.
   - To make life easier, use the empty-example folder from the tutorial as your working directory and work out of the index.html and sketch.js files within it.
  2. Delete the code in your sketch.js. Replace it with the the code found [here](https://p5js.org/reference/#/p5/loadTable).
   - This just makes it so we don't have to create an entirely new file and reconnect all the documents.
  3. In the third line of actual code (not including comments) replace `"assets/mammals.csv"` with the file path to the .csv file you're using.
    - Your third line of code should now look something like this:
    `table = loadTable("FILENAME.csv", "csv", "header")`
  4. Look over the sketch.js example I provided. It's marked it up with comprehensive explanations and places you need to change the code around. Make sure you read over it before proceeding to the next step.
    - You can try running it with your
    index.html file if you want to see it in action.
  5. Now that you've read how, in your sketch.js code change ``"name"`` in the line `print(table.getColumn("name"));` to the column you're trying to get (if you haven't already).


### Viewing your table
  1. Run your index.html document on a web browser
  2. Open up developer tools
    - *[This article](https://www.lifewire.com/web-browser-developer-tools-3988965) shows how to open the developer toolbox on any browser*
  3. Click on the "javascript console" tab in your developer toolbox (might just be "console" on some browsers).
  4. You should now be able to see the "printed" statements from your sketch.js document.

### Build your story
The options here are too diverse to describe in a single point. However, if you want to start with existing code, see my [15 Years of Mass Shootings in America](https://github.com/evanpeck/15-Years-of-Mass-Shootings-in-America) github repository.


---------

## Tips for Vega Lite (or Vega)

### Introducing Vega-Lite:
  1. Open up Vega-Lite's [online editor](https://vega.github.io/new-editor/?mode=vega-lite) to work out of
  2. Look through the charts and graphs we're given (found in the dropdown menu) to see the different possibilities for visualizing data with Vega-Lite.
  3. Go through their first two [tutorials](https://vega.github.io/vega-lite/tutorials/getting_started.html#embed) titled "The Data" and "Encoding Data with Marks". Code along with the tutorial in order to get a better feel for the library. Some helpful tips:
      1. Entire code should be wrapped in `{}`.
      2. Almost every value you enter must be wrapped in `""`– excludes punctuation and numerical values in the `data: values` field.
      3. The `encoding` field is where you'll enter the bulk of the information about your dataset. Most importantly the x- and y-axis data go here. *[Learn about the different data types here](https://vega.github.io/vega-lite/docs/encoding.html#data-type)*.
      4. Create a legend using [this documentation](https://vega.github.io/vega-lite/docs/legend.html).
  4. When you're done going through the tutorial, use the data found in [this](https://github.com/plotly/datasets/blob/master/2014_apple_stock.csv) csv file to create a chart or graph.
      - To use data from an online link, replace `"data": { "values": [..] },` with <br> `"data": { "url": "URL", "format": {"type": "TYPE"} },` where `TYPE` is the type of file used (csv in our case).
      - When you're entering the x- and y-axis "fields", instead of typing `a` and `b` you'll type in the names of the columns you'd like to display the data for. In this example there are only two columns so your x field would be "AAPL_x" and your y-field would be "AAPL_y".
  5. Once you finish playing around with your chart or feel like you understand how the code works, move on to the next task.


### Publishing your Visualization:
  1. Once you're diagram is finished open the `index.html` in the `public_html` folder that you created earlier in a text editor.
  2. Delete anything that's already in the file and use the code given [here](https://vega.github.io/vega-lite/tutorials/getting_started.html#embed) (if your computer isn't already there, go to the section titled "Publish your Visualization Online") to guide you in adding your chart or graph to your webpage.
      - Don't forget to include `var vlSpec = {` before entering your diagram code as well as the optional code for vega-lite that we need `var opt = {"mode": "vega-lite"};` towards the bottom.
  3. Once completed, you should be able to see your diagram
