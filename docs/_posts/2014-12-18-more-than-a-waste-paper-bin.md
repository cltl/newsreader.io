---
layout: post
title: "More than a waste paper bin: the data for From Porsches to Pizza"
date: 2014-12-18 10:03:04 +0000
categories:
  - "Events"
  - "Announcements"
tags:
  - "hackathon"
  - "january"
  - "cars"
---
A car metaphor seems in place to start: the NewsReader engine is a true gas guzzler, with an extreme thirst for raw data. We quenched this thirst by selecting and delivering several **millions** of news articles covering the global automotive industry for the NewsReader infrastructure to process and enrich.

A big chunk of this ‘NewsReaderised’ data set will be used for the hackathons in [Amsterdam](https://www.eventbrite.com/e/porsches-to-pizza-hack-6000000-automotive-news-articles-newsreader-tickets-14504369961) and [London](http://www.eventbrite.com/e/porsches-to-pizza-hack-6000000-automotive-news-articles-newsreader-tickets-14458478699), late January. 

 **Why automotive?**

Not because all NewsReader contributors are car nuts (some are, though), but because this industry is truly global, gets continuous press coverage in serious volumes and, last but not least: because this is an industry with highly complex relationship networks.

A couple of examples to shed some light on that complexity:

- competitors can simultaneously be partners/customers/suppliers;
- acquisition targets become buyers (the Volkswagen-Porsche bid war);
- suppliers get the critical mass to acquire their customers (2009: Magna-Opel);
- components are co-developed (lightweight materials, engines);
- senior managers easily ‘jump’ from one company to the other, and
- brands can change hands frequently (LandRover from BLM to BAe to BMW to Ford to Tata)

In the opinion of the team this complex ecosystem offers fertile soil for the type of data and event analysis NewsReader has been designed for.

 **Selecting documents**

Selecting the dataset for the hackathons was a balancing act: relevant documents on the one hand, but not too much of pre-filtering in this stage on the other. This balance should allow the NewsReader tooling to enrich the data in as unbiased a fashion as possible.

After some experimenting we settled for a relatively straightforward search string. The core of this query consists of the world’s major car brands linked with ‘OR’ connectors, effectively searching the [LexisNexis](http://www.lexisnexis.com) database for ALL documents mentioning these brands. We added an additional level of filtering, to reduce the volume of non-business relevant documents, i.e. coverage of sports events, car accidents/thefts, etcetera. For this purpose we built a second search string, containing ‘business buzz words’, like *merger, CEO, ownership, consolidation,* and so forth. The second and first strings were combined with an ‘AND’ connector, thus applying the ‘business filter’ to the topic-agnostic set of car news documents.

**Choosing a timeline**

We wanted a balanced coverage of news documents: a roughly comparable volume of documents per year, to get good volumes of data for the full length of the imaginary timeline we’d be populating. The LexisNexis archives do go back several decades, but you’ll see a correlation with the rise of digital systems in Publishing: coverage decreases substantially the further you go back in time, pre-1990s volumes are almost negligible compared to post-2000 volumes!

Thankfully the post-2000 volumes produced more than enough documents to get to the multi-million document set we needed, the final document retrieval requests covered the Jan 2003-April 2013 timeframe, supplying us with over 10 years of events to distil…

 **The data set**

The final raw data set contains over six million documents from international (print) news sources. Most of these will be from English-language publications because of the ‘second search string’ that filtered on business-relevant topics in English; taking a few samples has indicated that some non-English documents have slipped through.

A lesson learned: next time we either expand the scope to include multiple languages (NewsReader will be able to process English, Italian, Spanish, Dutch) by building multi-lingual queries, or we can narrow down the selection by adding a “Language=XXX” filter in our queries.

If you want to join our automotive Hack Day then you can sign up for the Amsterdam event [here](https://www.eventbrite.com/e/porsches-to-pizza-hack-6000000-automotive-news-articles-newsreader-tickets-14504369961) or for our London event [here](http://www.eventbrite.com/e/porsches-to-pizza-hack-6000000-automotive-news-articles-newsreader-tickets-14458478699).
