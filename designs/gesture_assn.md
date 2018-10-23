---
layout: page
title: Design for Fun
exclude: true
---

- **Group size:** Teams of 4
- **Demo Day:** 4/13 _in class_
- **Design Doc Due:** 4/16, 11:59 PM

## Overview

In this design sprint, you will build an interface that prioritizes _fun_. To do this, you have two options, both which will use [Leap Motion Controllers](https://www.leapmotion.com/):

1. Choose an existing game/application on the web, and then remap the controls from keyboard/mouse to a 3D user interfaces using Leap Motion. Since you are not responsible for the generation of content, this will allow you to focus your design on the input.
2. If you want to experiment with a more expressive (maybe audio?) output, you can use [Wekinator](http://www.wekinator.org/) with [Leap Motion Controllers](https://www.leapmotion.com/) as its primary input (see this [demo code on wekinator's website](http://www.wekinator.org/examples/#Leap_Motion_hardware_sensor)). You can choose the output.

In either case, your design goal is simply to maximize the enjoyment that people have with your app.  

**Note:** Think about how you want to document your design process. For example, given the physical nature of 3D UIs, you may need to

### Ideation

> In traditional UIs, we usually try to design without regard for the display or the input device (i.e., display- and device-independence) ... But in 3D UIs, what works on one display or with one device very rarely works exactly the same way on different systems. - Doug Bowman, 3D User Interfaces


In most of our assignments so far, I have had you ideate without the burden or limitations of the technology. However, in this case, your hardware (monitor size, for example) is likely to have a significant impact on interaction. In addition, the Leap Motions may surprise you in the ways that they are accurate and/or inaccurate.

I would recommend that you get a rough sense of the Leap Motion's capabilities right from the start - perhaps assigning a person or two on your team to begin playing with the devices while the rest of your group brainstorms.

**Remember:** Note that the goal of **fun** is different than an efficient or usable interface.

Your brainstorming shouldn't consist of just writing down sketches and trying to intellectually determine 'fun'. Do it! Try the gestures yourselves! Fun isn't just embedded in the application, but in the interaction design... are some motions more fun/engaging than others, even if they might be less accurate?

### Formative Testing
Before you build it, [Wizard-of-Oz](http://www.usabilitynet.org/tools/wizard.htm) your idea with other students. To do this, use the following process:
- Define a set of actions for input
- Have a participant use those actions to interact with the game. The participant should be looking at the application monitor, but someone in YOUR group (_the controller_) should have access to the keyboard/mouse.
- _The controller_ should ONLY look at your participant, NOT the screen. When the participant performs an action, the controller hits the corresponding button (or move the mouse). While you may not be quite as responsive as the leap motion, it will let other people experiment with your design.


For an example, see the [in-class prototyping we did in HCI during Spring 2016](https://drive.google.com/open?id=0B9wW7gtF6dvRa3M1ZUVhTGMtMnc). In this video, a student in the bottom left corner (only occasionally in the screen) is hitting buttons while the participant jumps and punches to play [Robot Unicorn Attack](http://www.adultswim.com/games/web/robot-unicorn-attack).


### Build It and Test It
There are a couple of files that you may want to download:

1. [Leap Motion Java Template Code](https://drive.google.com/open?id=0B9wW7gtF6dvRZ0pyVEVzdnE5UFk)
2. [Sample Projects in which Leap Motion is substituted for controls on various websites and games](https://drive.google.com/open?id=0B9wW7gtF6dvRLUxGdnpnQzVFZGM)

See the hints created by Gabbi below about compiling and running Leap Motion programs. As much as you can, don't forget to test with real people!


### Deliverables
- As always: Your design reflection as a Medium blog post. **You WILL need a demo video**.
- Please upload your code to a publicly accessible repository (for example, Github or Gitlab). Other people with a Leap Motion should ideally be able to download your code and run your program. **Include this link in your design doc**



## Using the Leap Motion
See the preliminary tips for Leap Motion provided by Gabbi LaBorwit's ('20) experience trying to complete this assignment.

### __Getting Started__
  - [Download](https://developer.leapmotion.com/sdk/v2) the SDK.
  - Create a Java program that turns your hand into a virtual mouse/scroll bar by following [this tutorial](https://www.youtube.com/watch?v=ucttSu-XPb8&list=PLgTGpidiW0iQGk-zYzmcDw6XtEMYh69j4&index=11). Use the `template` folder provided to work in, and the file labelled `template.java` to code in.

- *Note*: You'll need to rename the Java file to whatever you name your main function (a class in this case). If you're unsure where this is, look at the comment explanation towards the bottom of your template document.
    - The template file provided gives some explanations, but it may be useful to look over the following section for more detailed explanations on some of the more important functions.

- *Running/testing programs:*  
    1. Compile the application:
          - *Macs:*  
          `javac -classpath ./LeapJava.jar FILENAME.java`
          - *Windows:*  
          `javac -classpath LeapJava.jar FILENAME.java`
    2. Run the program:
          - *Macs:*  
          `java -classpath "./LeapJava.jar:." FILENAME`
          - *Windows:*  
          `java -classpath "LeapJava.jar;." FILENAME`
    3. You should then see the message “Connected” printed to Terminal indicating your program/detector is connected and ready to go!


### __Leap Motion 101__ (& a couple Java things)
  - `onFrame(Controller controller) {}`
    - To collect data, Leap Motion detectors are constantly taking snapshots called *frames*. The data gathered from these snapshots is used in the function `onFrame(..)` in which the bulk, if not all, of your program is built in.
  - `Robot()`
    - Robot is used to fulfill input events for the purposes of automation, self-running demos, and other applications where control of the mouse and keyboard is needed. (*Source: [Oracle](https://docs.oracle.com/javase/7/docs/api/java/awt/Robot.html)*)
  - Gestures:
    - Pre-defined hand/finger motion objects your detector can pick up on.
    - Types:
      - `TYPE_CIRCLE`: detects twirling your hand/finger(s) in a circle.
      - `TYPE_SWIPE`: detects a hand motion similar to swatting a fly away.
      - `TYPE_SCREEN_TAP`: detects if you're finger/hand moved close to the screen in order to perform a mouse click, etc.
      - `TYPE_KEY_TAP`: detects a tapping motion from a finger.
  - Useful hand functions:
    - `roll()`: how tilted your hand is to the right or left
    - `pitch()`: how tilted forward or backward your hand is
    - `yaw()`: how close or far your hand is from the screen (think of this as the depth of your hand in relation to the screen).
    - To find the x, y, and z coordinates (aka roll, pitch, and yaw) of your hand at any time, use the code `hand.palmPosition()` (hand referring to the hand object you must create).
      - A useful [picture + description](https://developer.leapmotion.com/documentation/java/api/Leap.Vector.html#javaclasscom_1_1leapmotion_1_1leap_1_1_vector) demonstrating how the detector picks up the x, y, and z coordinates.
  - Integrating the keyboard:
    - Have `robot` type for you based on different gestures you perform and ways you move!
    - The code: `robot.keyPress(KeyEvent.VK_KEYHERE);`
    - Key options can be found [here](https://docs.oracle.com/javase/7/docs/api/java/awt/event/KeyEvent.html).
  - Misc.
    - Closed fingers or fist: to check whether a finger is tucked in or not Leap Motion uses the function `.isExtended()`, returning `true` if the finger is not closed and 'false' if it is.



#### Other Notes
 - Explains the hand code in beginning of Sample.java code ([here](https://www.youtube.com/watch?v=RsYLRekb9e0&list=PLgTGpidiW0iQGk-zYzmcDw6XtEMYh69j4&index=4))
