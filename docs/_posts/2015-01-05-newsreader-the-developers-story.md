---
layout: post
title: "NewsReader: the developers story"
date: 2015-01-05 17:05:32 +0000
categories:
  - "Events"
tags:
  - "Hack Day"
  - "scraperwiki"
  - "Simple API"
---
[![newsreader](https://blog.scraperwiki.com/wp-content/uploads/2014/12/newsreader.png)](https://blog.scraperwiki.com/wp-content/uploads/2014/12/newsreader.png)

Our role at ScraperWiki is in providing mechanisms to enable developers to exploit the NewsReader technology, and to feed news into the system. As part of this work we have developed a simple REST API which gives access to the KnowledgeStore, the system which underpins NewsReader. The native query language of the KnowledgeStore is SPARQL – the query language of the semantic web. The Simple API provides a set of predefined queries which are easier for end users to work with than raw SPARQL, and help us as service managers by providing a predictable set of optimised queries. If you want to know more technical detail then we’ve written a paper about it ([here](http://ceur-ws.org/Vol-1268/paper2.pdf)).

The Simple API has seen live action at a Hack Day on World Cup news which we held in London in the summer. Attendees were able to develop a range of applications which probed violence, money and corruption in the realm of the World Cup. I blogged about our previous Hack Day [here](https://blog.scraperwiki.com/2014/06/world-cup-hack-day-london-10th-june-a-teaser/) and [here](https://blog.scraperwiki.com/2014/07/newsreader-world-cup-hack-day/). The Simple API, and the Hack Day helped us shake out some bugs and add features which will make it even better next time.

“Next time” is another Hack Day to be held in the Amsterdam on 21st January 2015, and London on the 30th January 2015. This time we have processed 6,000,000 articles relating to the car industry over the period 2005-2014. The motor industry is a trillion dollar a year business, so we can anticipate finding lots of valuable information in this horde.

From our previous experience the three things that NewsReader excels at are:

1. **Finding networks of interactions, identifying important players**. For the World Cup Hack Day we at ScraperWiki were handicapped slightly by having no interest in football! But the NewsReader technology enabled us to quickly identify that “Sepp Blatter”, “Jack Warner” and “Mohammed bin Hammam” were important in world football. This is illustrated in this slightly cryptic visualisation made using Gephi:[![beckham_and_blatter](https://blog.scraperwiki.com/wp-content/uploads/2014/06/beckham_and_blatter.png)](https://blog.scraperwiki.com/wp-content/uploads/2014/06/beckham_and_blatter.png)
2. **Finding events of a particular type.** the NewsReader technology carries out semantic role labeling: taking sentences and identifying what type of event is described in that sentence and what roles the participants took. This information is then aggregated and exposed using semantic web technology. In the World Cup Hack Day participants used this functionality to identify events involving violence, bribery, gambling, and other financial transactions;
3. **Establishing timelines.** In the World Cup data we could track the events involving “Mohammed bin Hammam” through time and the type of events he was involved in. This enabled us to quickly navigate to pertinent news articles.[![Timeline](https://blog.scraperwiki.com/wp-content/uploads/2014/06/Timeline-1024x611.jpg)](https://blog.scraperwiki.com/wp-content/uploads/2014/06/Timeline.jpg)

You can see fragments of code used to extract these data using the Simple API in these GitHub Gists ([here](https://gist.github.com/IanHopkinson/dee6cac1bd91e92732cf) and [here](https://gist.github.com/IanHopkinson/635e9fa156ec39285a05)), and dynamic visualisations illustrating these three features [here](http://public.tableausoftware.com/profile/ian.hopkinson#!/vizhome/blatter_and_beckham/NewsEvents) and [here](http://stevenmaude.github.io/newsreader-network-vis/).

The Simple API is up and running already, you can find it ([here](https://newsreader.scraperwiki.com/)). It is self-documenting, simply visit the root URL and you’ll see query examples with optional and compulsory parameters. Be aware though: the Simple API is under active development, and the underlying data in the KnowledgeStore is being optimised for the Hack Days so it may not be available when you visit.

If you want to join our automotive Hack Day then you can sign up for the Amsterdam event ([here](https://www.eventbrite.com/e/porsches-to-pizza-hack-6000000-automotive-news-articles-newsreader-tickets-14504369961)) and the London event ([here](http://www.eventbrite.com/e/porsches-to-pizza-hack-6000000-automotive-news-articles-newsreader-tickets-14458478699)).
