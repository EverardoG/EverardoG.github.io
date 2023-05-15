---
title: 'Autonomous Tugboat'
subtitle: 'Adding autonomy to a small tugboat'
date: 2020-11-10 00:00:00
description:
featured_image: '/images/landing_page/landing_funrobo.png'
---

<img src="/images/landing_page/landing_funrobo.png" alt="drawing" width="800"/>

<p style="text-align: left;"> This is Lesley, an autonomous tugboat capable of navigating around foam icebergs and chasing down a stuff pink narwhal on a remotely control tugboat.</p>

### Overview 

**Timeline:** 2.5-week Final Project for Fall 2018 Fundamentals of Robotics Course at Olin College

**Collaborators:** Amy Phung, Robert Wechsler, Jordan Leadley, w. Professor David Barrett

The goal of this project was to add sensing capabilities and software to a remote controlled tugboat in order to autonomously complete four missions. The missions took place in an indoor circular pool, and the robot could be reset in between missions. Mission descriptions are listed below, and the [github repo is here](https://github.com/AmyPhung/FunRoboTugboat).

1. Circle the perimeter of the pool once without bumping the edge
2. Trace three figure 8s in the pool while avoiding foam icebergs
3. Trace one figure 8 around the pool and redock
4. Chase and tag a tugboat carrying a stuffed pink narwhal remotely controlled by the teaching assistant

### Demos

These are videos of Lesley, our autonomous tugboat, completing each mission during the final demo.

#### Mission 1: Circle the pool

<iframe width="560" height="315"
src="https://www.youtube.com/embed/ErhXkYFsTJ4" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

Here we see Lesley completing her first mission - circle the pool. The objective was to undock, and follow the pool wall until getting back to the dock, at which point the mission was complete. Here, we see Lesley take a sharp left out of the dock until she gets to the edge of the pool, at which point she begins following the pool wall. As she nears the dock, she takes a hard right to avoid a collision, and completes the mission.

#### Mission 2: Three figure 8s

<iframe width="560" height="315"
src="https://www.youtube.com/embed/WIVv6e_m0Sk" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

Here we see Lesley completing her second mission - three figure 8's around the pool. The objective was to undock, and then do three consecutive figure 8's around the foam icebergs in the pool. Once again, Lesley takes a sharp left out of the dock until she sees the pool wall. She follows the wall until her heading goes past a certain threshold. At that point, she begins circling the iceberg until her heading hits another threshold, letting her know it's time to straighten out. She repeats this process until she's performed the three figure 8's, and successfully completes the mission.

#### Mission 3: One figure 8 and redock

<iframe width="560" height="315"
src="https://www.youtube.com/embed/jrWSk9W6jTE" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

Here we see Lesley completing her third mission - one figure 8 around the pool, then dock. The objective was to undock, as per usual, perform a single figure 8 around the foam icebergs, and then dock. Lesley uses the same strategy for performing her figure 8 as before, but now breaks out of doing figure 8's after her first one. At that point, she straightens out towards the dock, and uses her PixyCam to align herself with the big red dot above the dock. She straightens herself towards the dock, and slows down as she reaches her destination, successfully completing mission 3.

#### Mission 4: Chase the pink narwhal

<iframe width="560" height="315"
src="https://www.youtube.com/embed/1c9tg1cHuf0" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

Here we see Lesley on her fourth and final mission - undock and chase the pink narwhal! The objective was to undock, locate, and tag the boat with the pink narwhal. Alas, I don't have video of the entire mission, so we'll have to settle for a small snippet. Lesley isn't particularly successful in this portion of the mission, as she fails to actually locate the narwhal, instead perceiving it as an obstacle and attempting to avoid it. This is due to the fact that Lesley can only see the narwhal with her PixyCam, which is mounted her front. Only later, does she finally see the narwhal, and tag it.

### My Contributions

I managed this team to ensure that we could deliver a robot boat that could accomplish all of our missions. I planned with my team how to set up our sensing array to best accomodate our autonomy algorithms, and created our sensor mounts. My technical contributions also included setting up remote communication with the robot, and writing and testing control software for the first two missions.

### Our Story

At the start, were given a small tugboat with batteries and motors already integrated, and access to high quality 3D printers, various sensors, and various micro controllers. Over the following weeks, we had to decide how we would approach the various missions, how our system would be architect-ed, create sensor mounts, develop control software, test our algorithms, etc. The final assessment of the project was how well it completed the missions, so the pressure to deliver was on!

I spent a lot of the first week planning with my team how we would approach the various missions, how we were going to design our system, and how we would manage ourselves as a team. This meant deciding what sensors we were using, where we were putting them, how we were mounting them, how we were dividing up tasks, and how we were going to approach the different missions. My primary technical task was to design and fabricate our sensor mounts. You can see these mounts as the orange parts of the boat with the sensors attached. I designed the mounts in Solidworks and 3D printed them in Olin's robotics lab.

With a fleshed out plan for system development in place, we divided and conquered sub systems our second week. I set up radio communication between our robot boat and an offshore laptop via an XBee radio. This made it so that we could remotely estop our robot, as well as set it to different modes based on what mission it needed to accomplish. This is also where I was tasked with creating a communications protocol between three Arduino Uno micro controllers - Arduino 1 gets camera data, Arduino 2 gets low level sensor data plus radio messages, and Arduino 3 actuates our rudder and propellers. This was a result of a single Arduino Uno not having enough pins for all of our intended electronics. While this architecture seemed promising, we noticed that our system exhibited significant latency when we tried to accomplish the first mission: circle the pool. At that point, Amy suggested switching all of our firmware to a single Arduino Mega. When we tested this, we no longer saw such a high latency, and decided to scrap the original multi-Arduino architecture.

For the last portion of the project, we had a fully integrated robotic system that was ready to take on the missions. Except, we still needed to write the control software to make sure the robot boat wouldn't bump into walls, over steer, go the wrong direction, etc. I developed a few different control schemes for tackling the first two missions - circle the pool, and do three consecutive figure 8's around the pool. Jordan and I tested these control schemes on our system, and iterated on our controllers until we achieved functional behavior. Amy and Robert tackled the last two missions.

### Systems Testing

These are videos I took while testing out the controllers for the first two missions.

<iframe width="560" height="315"
src="https://www.youtube.com/embed/tADk9if8Ee0" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

Lesley uses an on-board gyroscope to determine her heading at all times during her trip, as well as sharp IR sensors on her port to determine where she is relative to the pool wall. Her voyage begins with an undocking phase that ends once her heading is beyond a certain threshold. Then, she switches into a wall following state. Once she gets close to the dock, which is determined via heading, she makes a sharp right to avoid colliding with the dock. She straightens out to swim right past the dock, but unfortunately keeps going towards the pool wall. We never fixed this bug because perfect was the enemy of done on this project, and all she needed to do was get past the dock.

<iframe width="560" height="315"
src="https://www.youtube.com/embed/TQ_4-8VZOUQ" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

And wait there's more! Lesley can also run figure 8s around the icebergs in the pool. Here you can see a preliminary test of a more complex algorithm we designed. 

Lesley begins once again by undocking. When her heading hits a certain threshold, she switches into wall following mode, and begins chugging alongside the pool wall. Her heading hits another threshold, prompting her to make a hard right around the iceberg. She straightens out with yet another heading trigger. Lesley chugs along until her left sharp IR sensors see the next iceberg. She makes a hard left, and the process continues like this until we send her a stop command.




<!-- ![](/images/landing_page/landing_funrobo.png)

## Demo content

This page is a demo that shows everything you can do inside portfolio and blog posts.

We've included everything you need to create engaging posts about your work, and show off your case studies in a beautiful way.

**Obviously,** we’ve styled up *all the basic* text formatting options [available in markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

You can create lists:

* Simple bulleted lists
* Like this one
* Are cool

And:

1. Numbered lists
2. Like this other one
3. Are great too

You can also add blockquotes, which are shown at a larger width to help break up the layout and draw attention to key parts of your content:

> “Simple can be harder than complex: You have to work hard to get your thinking clean to make it simple. But it’s worth it in the end because once you get there, you can move mountains.”

The theme also supports markdown tables:

| Item                 | Author        | Supports tables? | Price |
|----------------------|---------------|------------------|-------|
| Duet Jekyll Theme    | Jekyll Themes | Yes              | $49   |
| Index Jekyll Theme   | Jekyll Themes | Yes              | $49   |
| Journal Jekyll Theme | Jekyll Themes | Yes              | $49   |

And footnotes[^1], which link to explanations[^2] at the bottom of the page[^3].

[^1]: Beautiful modern, minimal theme design.
[^2]: Powerful features to show off your work.
[^3]: Maintained and supported by the theme developer.

You can throw in some horizontal rules too:

---

### Image galleries

Here's a really neat custom feature we added – galleries:

<div class="gallery" data-columns="3">
	<img src="/images/demo/demo-portrait.jpg">
	<img src="/images/demo/demo-landscape.jpg">
	<img src="/images/demo/demo-square.jpg">
	<img src="/images/demo/demo-landscape-2.jpg">
</div>

Inspired by the Galleries feature from WordPress, we've made it easy to create grid layouts for your images. Just use a bit of simple HTML in your post to create a masonry grid image layout:

```html
<div class="gallery" data-columns="3">
    <img src="/images/demo/demo-portrait.jpg">
    <img src="/images/demo/demo-landscape.jpg">
    <img src="/images/demo/demo-square.jpg">
    <img src="/images/demo/demo-landscape-2.jpg">
</div>
```

*See what we did there? Code and syntax highlighting is built-in too!*

Change the number inside the 'columns' setting to create different types of gallery for all kinds of purposes. You can even click on each image to seamlessly enlarge it on the page.

---

### Image carousels

Here's another gallery with only one column, which creates a carousel slide-show instead.

A nice little feature: the carousel only advances when it is in view, so your visitors won't scroll down to find it half way through your images.

<div class="gallery" data-columns="1">
	<img src="/images/demo/demo-landscape.jpg">
	<img src="/images/demo/demo-landscape-2.jpg">
</div>

### What about videos?

Videos are an awesome way to show off your work in a more engaging and personal way, and we’ve made sure they work great on our themes. Just paste an embed code from YouTube or Vimeo, and the theme makes sure it displays perfectly:

<iframe src="https://player.vimeo.com/video/19536258?color=ffffff&title=0&byline=0&portrait=0" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

---

## Pretty cool, huh?

We've packed this theme with powerful features to show off your work. Why not put them to use on your new portfolio?

<a href="https://jekyllthemes.io/theme/index-portfolio-jekyll-theme" class="button button--large">Get This Theme</a> -->