---
layout: post
title: "NWR\u2019s favourite ACL papers"
date: 2013-08-29 18:56:45 +0000
categories:
  - "Events"
tags:
  - "acl"
  - "acl2013"
  - "events"
  - "inspiration"
  - "papers"
  - "recap"
---
Several NewsReader members attended [ACL 2013](http://www.acl2013.org/site/) to present their own work [[1](http://aclweb.org/anthology-new/P/P13/P13-2130.pdf)] [[2](http://aclweb.org/anthology-new/P/P13/P13-1116.pdf)] [[3](http://aclweb.org/anthology-new/P/P13/P13-1166.pdf)] and to see what other colleagues in the field are working on. Here is a small selection of papers that are related to the NewsReader project and from which we are drawing inspiration for the next steps in our project.

[Recognizing Identical Events with Graph Kernels](http://aclweb.org/anthology-new/P/P13/P13-2139.pdf)

Goran Glavaš and Jan Šnajder

- How to detect whether two event mentions refer to the same event is still an open research question because there are so many different ways of referring to events, and as more information becomes available about events, our perception of it and how we refer to it changes (see [this 2010 LREC paper](http://www.lrec-conf.org/proceedings/lrec2010/pdf/205_Paper.pdf) for more on this). In “Recognizing Identical Events with Graph Kernels, the authors propose a graph-based approach in combination with machine learning to identify whether two event mentions refer to the same event. Within NWR we also use a graph-based representation for events so it is definitely an interesting idea to see how this approach would translate to the NWR case.

*[HEADY: News headline abstraction through event pattern clustering](http://aclweb.org/anthology-new/P/P13/P13-1122.pdf)*

Enrique Alfonseca; Daniele Pighin; Guillermo Garrido

- Another way to identify co-referring event mentions is presented in this paper where the authors generate headlines starting from large clusters of news and then identify co-referring event mentions by finding patterns where the same (Freebase) entities occur.

[Linking Tweets to News: A Framework to Enrich Short Text Data in Social Media](http://aclweb.org/anthology-new/P/P13/P13-1024.pdf)

Weiwei Guo, Hao Li, Heng Ji and Mona Diab

- Within NWR we are dealing with different accounts of the same event (coming from different sources). It is inevitable that some sources will provide more elaborate accounts than others. In this ACL contribution, the authors tackle the problem of linking very short messages that only deal with one aspect of a story to longer newswire articles. This is interesting for us to identify clusters of articles in which we can expect to find co-referring events as well as articles that were published right after an event and more overview articles used later.

[Temporal Signals Help Label Temporal Relations](http://aclweb.org/anthology-new/P/P13/P13-2114.pdf)

Leon Derczynski and Robert Gaizauskas

- A more researched, but still not solved problem is ordering events temporally. This approach to order events makes explicit use of temporal signals and the corpus is available for us to play with!

[Learning Latent Personas of Film Characters](http://aclweb.org/anthology-new/P/P13/P13-1035.pdf)

David Bamman, Brendan O’Connor and Noah A. Smith

- At first sight this paper seems not very central to NWR, but one of our goals is to help end-users identify ‘interesting stories’ inside the vast amount of possible story lines that can be generated from our data. “Learning Latent Personas of Film Characters” is about learning character types from movie plots, by using cross-links to Freebase information about actors and movie genres. Such an approach may help us perform a variation on topic clustering that can help us create personas for entities in the NWR domain.

Food for thought!
