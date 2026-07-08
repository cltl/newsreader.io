---
layout: post
title: "NewsReader World Cup Hack Day"
date: 2014-08-01 11:30:45 +0000
categories:
  - "Events"
tags:
  - "hackathon"
  - "london"
---
[![PiekPresents](https://blog.scraperwiki.com/wp-content/uploads/2014/07/PiekPresents_thumb.jpg "PiekPresents")](https://blog.scraperwiki.com/wp-content/uploads/2014/07/PiekPresents.jpg) Piek Vossen describing the NewsReader project
A long time ago\*, in a galaxy far, far away\*\* we ran the NewsReader World Cup Hack Day.
\*Actually it was on the 10th June .
\*\*It was in the Westminster Hub, London.
The NewsReader project has been running for about 18 months, so we are half way through. We’d always planned to use Hack Days to showcase the technology we have been building and to guide our future work. The World Cup Hack Day was the first of these events. We wanted to base the Hack Day around some timely news of a manageable size. The football World Cup fitted the bill. Currently the NewsReader technology works in a batch process so in the couple of months before the Hack Day we processed approximately 300,000 news articles relating to the World Cup. At ScraperWiki we made a Simple API to provide access to the data that the NewsReader technology outputs. We thought this necessary because the raw output is stored in an RDF triplestore and is accessed using SPARQL queries. SPARQL is a query language similar to SQL but is not as widely known, we didn’t want people to spend all day trying to get their first SPARQL query to work. Secondly, the dataset the NewsReader technology generates is several hundred million triples so even a “correct” query could easily cause the the SPARQL endpoint to appear unresponsive. By making the Simple API we could limit the queries made, and make sure that they were queries which ran in a reasonable time.
About 40 people turned up on the day; a big contingent from the BBC, a smattering of people from various organisations based in London and the core NewsReader team, enhanced with various colleagues we’d dragged along. After a brief introduction from Piek Vossen, who put some context around the Hack Day, and me – providing some technical details - the participants went into action.
They made a range of applications, most of them focused around extracting particular types of events, as defined by FrameNet. Gambling, fighting and commerce were common themes.  A rogue group from ScraperWiki ignored the Simple API, bought a 32 CPU with 60GB memory spot instance and wrote their own high performance search tool.
At the end of the day the participants presented their work, and prizes were awarded. Jim Johnson-Rollings from the BBC came first with a live demo of a tool which worked out which team a named football player had played for the course of his career. Second, was Team Fighty who built a tool to discover which football teams were most commonly associated with violence. Team Fail Fast, Fail Often tried out a wide range of things culminating in a swish [Gephi](http://gephi.github.io/) network visualisation. The prizes were regional foods from around the NewsReader consortium.
This was my first Hack Day, although ScraperWiki has run a number of such events in the past. We’d spent considerable effort in making the Simple API and it was great to see the hackers make such varied use of it. I was impressed how much they managed to do in such a short time.
The Simple API we developed, the presentation slides and some demo visualisations are available in this [bundle of links](http://tab.bz/ydtco).
The NewsReader team are grateful to all the participants for taking part and helping us with our project.
A big thanks also to the team at [The Hub Westminster](http://westminster.impacthub.net/) who gave us so much support on the day.
 
[![IMG_5200](https://blog.scraperwiki.com/wp-content/uploads/2014/07/IMG_5200_thumb.jpg "IMG_5200")](https://blog.scraperwiki.com/wp-content/uploads/2014/07/IMG_5200.jpg) Happy Hackers working away on the World Cup data at the Westminster Hub
