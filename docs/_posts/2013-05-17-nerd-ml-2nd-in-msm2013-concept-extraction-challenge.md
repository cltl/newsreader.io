---
layout: post
title: "NERD-ML 2nd in MSM2013 Concept Extraction Challenge"
date: 2013-05-17 18:11:43 +0000
categories:
  - "Presentations"
tags:
  - "challenge"
  - "msm2013"
  - "ner"
  - "nerd"
  - "presentation"
  - "publication"
  - "www2013"
---
Together with [Giuseppe Rizzo](http://www.eurecom.fr/~rizzo/) and [Raphaël Troncy](http://www.eurecom.fr/~troncy/) from [EURECOM](http://www.eurecom.fr), NewsReader team member [Marieke van Erp](http://www.mariekevanerp.com) participated in the [MSM2013 Concept Extraction Challenge](http://oak.dcs.shef.ac.uk/msm2013/challenge.html) with a system called NERD-ML. This system was developed  to identify and classify named entities in microposts (Tweets). Their system ranked 2nd in the challenge, only 0.01 points in F-score behind the best system.

NERD-ML is built on top of the [NERD](http://nerd.eurecom.fr) framework developed at EURECOM that makes it possible to easily query different named entity extractors that are available on the web. With NERD-ML, this framework was extended to take the output of the individual extractors and learn which extractors perform best on which data through an additional machine learning layer, improving the performance of the system over the individual extractors.

Giuseppe Rizzo presented NERD-ML at the [Making Sense of Microposts workshop](http://oak.dcs.shef.ac.uk/msm2013/index.html) at [WWW2013](http://www2013.org/) in Rio de Janeiro this week. You can find the preprint of the abstract describing the system [here](http://www.eurecom.fr/~rizzo/publication/Erp_Rizzo-MSM2013.pdf) and the presentation below.
