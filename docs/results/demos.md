---
layout: page
title: "Demos"
permalink: /results/demos/
---
## From English text, to NAF and from NAF to RDF

The next two demos show how we process English text files to detect events and participants. The first demo represents a pipeline of Natural Language Processing modules that generates a structure in the [NAF](http://wordpress.let.vupr.nl/naf/) format. The NAF output can be loaded as a file in the second demo, which creates a TriG structure in which instances of events and participants are represented with pointers to the mentions in the NAF structure. The TriG representations is based on the [SEM](http://wordpress.let.vupr.nl/sem/) format. These demos show our implementation of the [GAF](http://groundedannotationframework.org/) framework, combining mentions and instances and providing a layer for storing provenance (following the [PROV-O](http://www.w3.org/TR/prov-o/) guidelines).

- [Demo of the NewsReader NLP pipeline](http://ixa2.si.ehu.es/nrdemo/demo.php). Just copy in any English text and see what entities and events and other annotations are added automatically. The result is represented in the NAF format
- [Demo of the conversion of the NewsReader NLP output to TriG format](http://ic.vupr.nl/~ruben/vua-eventcoreference.ttl/). You can upload a file in NAF format and the service will generate the TriG file, representing instances of events and participants as well as provenance relations. The TriG file is converted to Turtle format and loaded in Visual RDF. A download button is provided to download the TriG file.  The NAF needs to have the following layers: text, terms, entities, coreferences, semantic roles. The previous NLP pipeline will generate NAF with these layers.

---

## Spanish text to NAF

The next demo shows the first version of the processing of Spanish texts. The pipeline uses the  [NAF](http://wordpress.let.vupr.nl/naf/)  as a layered annotation format for a number of NLP modules including tokenization, lemmatization, part-of-speech tagging, parsing, named entity recognition, named entity linking and semantic role labelling.

- [Demo of the NewsReader NLP pipeline](http://ixa2.si.ehu.es/nrdemo_es/demo.php). Just copy in any Spanish text and see what entities and other annotations are added automatically. The result is represented in the NAF format

---

## Dutch text to NAF

The next demo shows the first version of the processing of Dutch texts. The pipeline uses the [NAF](http://wordpress.let.vupr.nl/naf/)as a layered annotation format for a number of NLP modules including tokenization, lemmatization, part-of-speech tagging, parsing, named entity recognition, named entity linking word-sense-disambiguation, time expression detection and semantic role labelling.

- [Demo of the NewsReader NLP pipeline](http://kyoto.let.vu.nl/%7Ehuygen/test/test.php). Just paste in any Dutch text and see what annotations are generated automatically. The result is represented in the NAF format.

---

## Italian text to NAF

The next demo shows the first version of the processing of Italian texts. The pipeline uses the  [NAF](http://wordpress.let.vupr.nl/naf/)  as a layered annotation format for a number of NLP modules including tokenization, lemmatization, part-of-speech tagging, parsing, named entity recognition and temporal processing.

- [Demo of the NewsReader NLP pipeline](http://hlt-services2.fbk.eu:8080/nwrDemo/nwr). Just copy in any Italian text and see what entities and other annotations are added automatically. The result is represented in the NAF format.

---

## PIKES is a Knowledge Extraction Suite

The next demo shows [PIKES](http://pikes.fbk.eu), a new frame-based knowledge extraction framework. PIKES extracts entities and complex relations between them by identifying semantic frames in a text. It works in two integrated phases: First (phase 1: linguistic feature extraction), by performing several standard NLP tasks, a mention-based structured representation of the input text is built, organizing all the annotations produced by NLP tools (e.g., NERC, EL, TERN, SRL) in an RDF graph of mentions (i.e., spans of text denoting some entities or facts), according to SW vocabularies and principles. Then (phase 2: knowledge distillation), the mention graph is processed to distill a knowledge graph, where each node uniquely identifies an entity of the world, event or situation, and arcs represent relations between them (e.g., the participation and role of an entity in an event). This knowledge graph represents the knowledge conveyed by the text, in a way that abstracts from the specific occurrences of entities and relations in it.

- [Demo of PIKES](https://knowledgestore2.fbk.eu/pikes-demo/). Just type or copy in any English text and see the graphically enhanced results produced by PIKES. A demo video explaining how PIKES works is [available](https://www.youtube.com/watch?v=D0mcnUKc3sg).

---

## RDFpro: The Swiss-Army tool for RDF and Named Graph manipulation

[RDFpro](http://rdfpro.fbk.eu) (RDF Processor) is a public domain, Java command line tool and library for RDF processing. RDFpro offers a suite of stream-oriented, highly optimized RDF processors for common tasks that can be assembled in complex pipelines to efficiently process RDF data in one or more passes. RDFpro originated from the need of a tool supporting typical Linked Data integration tasks, involving dataset sizes up to few billions triples.  RDFpro can be used in three ways: (i) as a command line tool able to process large datasets; (ii) as a web tool suited to smaller amounts of data uploaded/downloaded with the browser; and (iii) as a Java library embedded in applications. Users can extend RDFpro via custom scripts and rulesets, while developers can create new processors by implementing a simple Java API and focusing on the specific task at hand, as efficient streaming, sorting, I/O, thread management, scripting, and composition facilities are already provided.

- [Demo of the RDFpro Web tool](https://knowledgestore2.fbk.eu/rdfpro-demo/). Just upload an RDF file (any format) and apply any of the available RDFpro processors. A demo video explaining how RDFpro web tool works is [available](https://www.youtube.com/watch?v=Vd2FCVRL8fk).

---

## Reasoning on Event implications using ESO

The next demo shows the second version of the [ESO](/results/event-and-situation-ontology/ "Event and Situation Ontology") reasoning module, updated to handle the ESO v2 ontology. It takes in input a TriG file produced by the [VUA event coreference module](http://ic.vupr.nl/~ruben/vua-eventcoreference.ttl/) , and produces pre-/post/during-situations according to the ESO v2 rules.

- [Demo of the ESO Reasoner](http://knowledgestore2.fbk.eu/reasoner). Just upload a TriG file produced by the VUA event coreference module (or use the example in the UI). You'll get a list of events in the TriG, enriched with the pre-/post/during-situations automatically inferred by the reasoner.

---

## KnowledgeStore

The next demo video shows how knowledge extracted from the NewsReader processing pipeline can be accessed, together with background knowledge, in the [KnowledgeStore](http://knowledgestore.fbk.eu), a scalable, fault-tolerant, and Semantic Web grounded storage system for interlinking unstructured and structured content.

- [Video Demo of the KnowledgeStore](http://youtu.be/YVOQaljLta4).

A publicly available KnowledgeStore instance, populated with the content extracted from Wikinews, can be accessed [here](https://knowledgestore2.fbk.eu/nwr/wikinews).
Synerscope implemented a NewsReader application to access the data in the KnowledgeStore within their visualization platform. Several [videos](/results/demos/synerscope/ "Synerscope") demonstrate how this application can be used to query and interact with the data.

---

## Synerscope

The next [page](http://www.newsreader-project.eu/results/demos/synerscope/) shows a couple of videos demonstrating how the KnowledgeStore data are visualised through the Synerscope tool. The Synerscope tool allows for multiple simultaneous views on the event centric and mention centric representation of the news. The videos show examples derived from 1.3 million English articles on the automotive industry for the period 2003 till 2013.

---

## Storyteller

NewsReader Storyteller is a tool to visualise events generated by the NewsReader software as structured stories on timelines. We define a story as a sequence of events structured according to some explanatory model (Vossen, Caselli, and Kontzopoulou 2015) in which:

1. there is at least one ***climax*** event that is the critical turning point in a sequence of events;
2. there is a series of events that precede the climax event and result in the critical situation. The preceding events are to some extent ***conditional*** for the climax event to take place according to some common sense explanatory model;
3. there is a series of events that follow the climax event as a ***consequence*** of the critical situation and common-sense response with respect to the climax;

Stories can be told in many ways and from many different perspectives. Storyteller visualises stories in 4 different ways, each focusing on different aspects:

1. actor centric stories
2. event centric stories
3. climax overview of all stories
4. source representation of the story as text

The stories are built from the SEM-RDF representations of events. We show a selection events for the MEANTIME data sets for *airbus, apple, chrysler\_gm\_ford* and *stock\_market* news articles. The demo can be accessed here: <http://nlesc.github.io/UncertaintyVisualization/>
The demo and data structures are explained on the next [page](/results/demos/json-timeline-structure/ "JSON Timeline structure").
P. Vossen, T. Caselli, and Y. Kontzopoulou, “Storylines for structuring massive streams of news,” in Proceedings of the 1st workshop on computing news storylines (cnews 2015) at the 53rd annual meeting of the association for computational linguistics and the 7th international joint conference on natural language processing (acl-ijcnlp 2015), Bejing, China, 2015.
