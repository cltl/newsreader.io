---
layout: post
title: "Computational Models of Narrative (CMN\u201914)"
date: 2014-08-10 17:58:07 +0000
categories:
  - "Events"
  - "Presentations"
tags:
  - "cmn14"
  - "narratives"
  - "research"
  - "workshop"
---
Last week the [2014 Workshop Computational Models of Narrative](http://narrative.csail.mit.edu/cmn14/) took place in Quebec City, Canada and [Marieke](http://mariekevanerp.com) was there to present and discuss ideas for shaping the NewsReader narratives.

This year’s workshop had a special focus on Neuroscience, but really all sorts of domains got covered in the three day workshop. Whilst at first some of the topics seemed quite far from NewsReader (after all, it is rather unlikely that we will put people in fMRI scanners to measure their appreciation of the NWR generated stories, although we are still thinking about our evaluation setup 😉 ) most talks put an idea or pointers to literature to the fore that will help us shape our story lines. One particular interesting community that we hadn’t been in touch with much is the planning community, which seems to have some approaches to shaping narratives that may be quite applicable to NWR.

During the coffee breaks there was also ample opportunity for discussion, so we’re now digging into the literature and hopefully soon we will start playing around with different setups in the project. To get an idea of what we’re currently struggling with, you can check out [our position paper](http://drops.dagstuhl.de/opus/volltexte/2014/4660/pdf/27.pdf) at CMN which details the four main challenges we see in automatically deriving narratives from large amounts of data or [the accompanying slides](http://www.slideshare.net/MvanErp/finding-stories-in-1784532-events-scaling-up-computational-models-of-narrative) (although you probably want the text of the paper too with those).

Some of the highlights from the workshop that we’ll be looking at in NWR:

- [Modeling the Function of Narrative in Expertise – W. Korey MacDougall, Robert L. West and Christopher Genovesi](http://drops.dagstuhl.de/opus/volltexte/2014/4649/pdf/15.pdf) This paper describes research on the intersection of expert knowledge and narratives, for example a doctor needs to communicate with patients on a different level than with colleagues. The authors of this paper utilise concepts from cognitive modelling to construct different narratives. In NWR, we envision our systems to be useful to different users, some of which may be more knowledgeable of the domain than others, so we should probably be looking more into user modelling than we have been doing so far.

- [A Cognitive Framework for Understanding Counterintuitive Stories – M. Afzal Upal](http://drops.dagstuhl.de/opus/volltexte/2014/4659/pdf/26.pdf) It has fairly long been accepted that stories that are surprising (or counterintuitive),  are easier to remember. In this paper, experiments are presented to test whether this hypothesis is true by modelling some (counter)intuitive things (like “can walk through walls” -> “is a superhero”). What is interesting here for us is that a series of “intuitive expectation sets” are presented that express common features (which we can perhaps recast as knowledge) about concepts that we might be able to use as background knowledge. Furthermore, for NWR, we are not only looking for the obvious stories, but also for the one-off or the ‘weird’ stories, which may be found in the realm of the counterintuitive narratives.

- [Plot Analysis for Describing Punch Line Functions in Shinichi Hoshi’s Microfiction – Hajime Murai](http://drops.dagstuhl.de/opus/volltexte/2014/4650/pdf/16.pdf) Following up on trying to find the ‘interesting’ stories, this work presents an approach to model plots and punch lines. Although the work hasn’t fully crystallised yet and is geared towards analysis of existing stories, the framework might be able to capture what makes some narratives more interesting than others.

- [What Makes Stories Similar? Report on a Research Project, 2011–2014 – Bernhard Fisseni and Benedikt Löwe](http://drops.dagstuhl.de/opus/volltexte/2014/4640/pdf/7.pdf)  Within NWR, we expect to generate many different stories from the datasets, in order to present to users as more extensive search results than an unordered bag of documents. In order to rank the stories, we need to be able to compare them somehow, and similarity is one measure to do so. In this project, several dimensions and measures have been investigated to compare stories.

- [Modifying Entity Relationship Models for Collaborative Fiction Planning and its Impact on Potential Authors – Alan Tapscott, Joaquim Colàs, Ayman Moghnieh and Josep Blat](http://drops.dagstuhl.de/opus/volltexte/2014/4658/pdf/25.pdf) At first sight this paper seems to be dealing with a totally different universe than NWR, as the authors describe a model to structure, store and share plot data to aid collaborating fiction authors. Whilst we are not dealing with fictional universes in which we need to keep track of the different characters and their adventures, it is important for us to model what has happened in our domain and to whom. We are already modelling the events through the [Simple Event Model](https://newsreader.vossen.info/newsreader/sem/) but as yet we have no framework to model plots yet.

Plenty of work to do! CMN’15 will most likely take place in Atlanta around May. We hope to be able to present the first version of our narrative module there!
