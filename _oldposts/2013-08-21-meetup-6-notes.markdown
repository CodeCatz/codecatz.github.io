---
layout: post
title:  "Meetup 6 notes: Reviewing complexicators, forking"
date:   2013-08-21 22:52:49
categories: meetup
---

It's time for the CodeCatz to take the training wheels off and get our paws dirty! And by that we mean starting to work on some serious(-ish) projects.

We spent most of today's meeting reviewing the code for our complexicators and the way they work with the Flask web app. We figured out how different parts of the app interact with each other. Behold the end result:

![Web app - how everything is connected]({{ site.url }}/assets/img/web-app-form-flow.jpg)

Then we looked at an even more complex example of the app, which uses if statements in templates, an additional Python script, and checks for errors in the server.py file ([code here](https://github.com/ialja/beautiful-web), feel free to fork and explore). We discussed the pros and cons of having HTML form validation on the client side (i.e. inside the browser with JavaScript/jQuery) or server side. Next time we want to explore some jQuery form validation. 

We want to have even more interactive discussions. So pick a topic, an interesting tool, feature, give it a try and present it at the next meetup. We now have a new GitHub repo [CodeCatz/kibble](https://github.com/CodeCatz/kibble). Read the instructions, learn how to fork and send pull requests. 

Yeah, it sounds a bit complicated, but it will be kitten play once you get it in your fingers. We also made the following drawing for reference: 

![Git forking and cloning]({{ site.url }}/assets/img/git-fork-clone.jpg)

![Git forking workflow]({{ site.url }}/assets/img/git-fork-workflow.jpg)

The litterbox wiki now has a [Wish list](https://github.com/CodeCatz/litterbox/wiki/Wish-list-and--ideas) of topics we'd like to explore. Feel free to add, explore the topics during the week and impress us at the next meeting. Whoop!

Keep on coding, Catz!

#### Homework

Until next week:

- pimp up your complexicator web app if you want to;
- cover most of the Learn Python the Hard Way lessons, we'd like to talk about Object Oriented Programming;
- take a look at the wish list and explore one of the topics on your own;
- think of other cool things you'd like to do;
- bonus points: learn how to fork the kibble repo.


*P.S.: I'm sure there be typos in this post. Why don't you fix them?*

*P.P.S.: Sorry for crappy pic quality. Dirty whiteboard, annoying reflections.*