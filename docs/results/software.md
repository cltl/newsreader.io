---
layout: page
title: "Software"
permalink: /results/software/
---
On this page, you can find the different software modules developed by the NewsReader project. The easiest setup is provided by the virtual machine package that contains the complete pipelines. For those interested in trying out different parts of the pipelines, all separate modules are listed below as well. Please note that the pipelines take [NAF](http://wordpress.let.vupr.nl/naf/) files as input, for which we have made available Java and Python libraries.
With each module, we specify who developed it. The quickest way to get help with a module is to contact that person. If a publication is associated with a module, it will be specified on the module's page.

### 'Black box' setup

For each of the processing pipelines (English, Spanish, Italian and Dutch), we have a downloadable virtual machine package that sets up the pipeline with the default settings as described in [Deliverable D4.2.2 Event Detection v2](http://www.newsreader-project.eu/files/2012/12/NWR-D4-2-2.pdf).

- **[English Virtual Machine](https://github.com/ixa-ehu/nwr-english-pipeline-vm)**: The instructions to download the virtual machine (VM) with all the required modules and NLP processors to run the **English pipeline** developed within the Newsreader project for event extraction is available at [this page](https://github.com/ixa-ehu/nwr-english-pipeline-vm)

- **[Spanish Virtual Machine](https://github.com/ixa-ehu/nwr-spanish-pipeline-vm)**: The instructions to download the virtual machine (VM) with all the required modules and NLP processors to run the **Spanish pipeline** developed within the Newsreader project for event extraction is available at [this page](https://github.com/ixa-ehu/nwr-spanish-pipeline-vm)
- **[Italian Virtual Machine](https://bitbucket.org/qwaider/nwr-italian-pipeline-vm)**: The instructions to download the virtual machine (VM) with all the required modules and NLP processors to run the **Italian pipeline** developed within the Newsreader project for event extraction is available at [this page](https://bitbucket.org/qwaider/nwr-italian-pipeline-vm)

- **[VMC from scratch](https://github.com/ixa-ehu/vmc-from-scratch)**: You can also download the instructions to automatically build the distributed pipeline for NLP processing from [this page](https://github.com/ixa-ehu/vmc-from-scratch)

### Hadoop package for batch processing (by SURFsara)

All modules for English and the overall setup to run the pipeline on a Hadoop cluster.
[direct download (±5GB)](http://beehub.nl/surfsara-hadoop/public/newsreader-hadoop.tar.gz)

### KnowledgeStore

- [KnowledgeStore](https://knowledgestore.fbk.eu/): A scalable, fault-tolerant, and Semantic Web grounded storage system to jointly store, manage, retrieve, and semantically query, both structured and unstructured data.

- [RDFpro](http://rdfpro.fbk.eu/): An extensible tool for building stream-oriented RDF processing pipelines, originated from the need of a tool supporting typical Linked Data integration tasks, involving dataset sizes up to few billions triples.

- [ESO reasoner](https://github.com/dkmfbk/eso-reasoner): An additional module for RDFpro (see above) that applies the rules of the [Event Situation Ontology (ESO)](/results/event-and-situation-ontology/ "Event and Situation Ontology") and creates the resulting Situation(s).

### 

### Simple API

- [NewsReader Simple API](https://bitbucket.org/scraperwikids/newsreader_api_flask_app.): an API that wraps a set of parameterised SPARQL queries to access the KnowledgeStore RDF structured content, and calls to the KnowledgeStore CRUD endpoint to retrieve unstructured resources.

### Converting NAF to RDF

- [vua-naf2sem](https://github.com/cltl/EventCoreference): Set of functions within the EventCoreference module that reads NAF files and creates the RDF-TRiG format according to the GAF-SEM model where events, events and relations are represented as unique instances with pointers to their mentions in text. It also creates the RDF-TRiG for the GRASP perspective model. The output can be loaded into the KnowledgeStore.

#### NAF and KAF parsers

- [KafSaxParser](https://github.com/cltl/KafSaxParser): Java library that reads and writes NAF and has an internal data structure for all NAF layers in memory.

- [pynaf](https://github.com/ixa-ehu/pynaf): Python library that reads and writes NAF and has an internal data structure for all NAF layers in memory.

- [kaflib](https://github.com/ixa-ehu/kaflib): Java library that reads and writes NAF and has an internal data structure for all NAF layers in memory.

- [KafNafParser](https://github.com/cltl/KafNafParserPy): Python module that produces and interprets NAF and KAF and can convert between the two.

### 

### Individual pipeline modules and libraries

#### English and multilingual modules

- [newsparser](https://github.com/newsreader/newsparser): tool to extract metadata from large numbers of news articles and store them in a compressed archive.

- [ixa-pipe-tok](https://github.com/ixa-ehu/ixa-pipe-tok): A multilingual rule-based tokenizer for English, Spanish and Dutch compliant with Penn Treebank and Ancora Corpus tokenization.

- [ixa-pipe-pos](https://github.com/ixa-ehu/ixa-pipe-pos): English/Spanish POS tagging with Perceptron models (Collins 2002) as implemented by Apache OpenNLP using the WSJ and Ancora corpus respectively.

- [ixa-pipe-parse](https://github.com/ixa-ehu/ixa-pipe-parse): English/Spanish Constituent Parsing with Maximum Entropy models (Ratnaparkhi 1999) as implemented by Apache OpenNLP using the Penn and Ancora Treebanks respectively.

- [ixa-pipe-nerc](https://github.com/ixa-ehu/ixa-pipe-nerc): English/Spanish/Dutch Named Entity Recognition with Perceptron models (Collins 2002) as implemented by Apache OpenNLP on CoNLL datasets for NER.

- [ixa-pipe-ned](https://github.com/ixa-ehu/ixa-pipe-ned): A client to query the DBpedia Spotlight for Named Entity Disambiguation (Mendes et al., 2011). This tool depends on the DBpedia Spotlight: <https://github.com/dbpedia-spotlight/dbpedia-spotlight> and is used for English, Dutch, Italian and Spanish.

- [ixa-pipe-wikify](https://github.com/ixa-ehu/ixa-pipe-wikify): A client to query the DBpedia Spotlight for wikification. This tool depends on the DBpedia Spotlight: <https://github.com/dbpedia-spotlight/dbpedia-spotlight> and is used for English and Spanish.

- [ixa-pipe-topic](https://github.com/ixa-ehu/ixa-pipe-topic): a module to extract a set of topics based on the Multilingual Eurovoc thesaurus descriptors and the JRC Eurovoc Indexer JEX. It is used for English and Spanish.

- [vua-svm-wsd](https://github.com/cltl/svm_wsd): This program svm\_wsd implements a machine learning Word Sense Disambiguation system based on Support Vector Machines. It is used in the Dutch pipeline.

- [wsd-ukb](https://github.com/ixa-ehu/ukb): This program applies the so-called Personalized PageRank on a Lexical Knowledge Base (LKB) to rank the vertices of the LKB for word sense disambiguation for English and Spanish.

- [MATE-based Parser and SRL](https://github.com/newsreader/ixa-pipe-srl): a tool providing lemmatization, POS-tagging, dependencies and semantic roles for English and Spanish based on the MATE-tools (Björkelund et al., 2010).

- [CorefGraph](https://bitbucket.org/Josu/corefgraph): a python reimplementation of the coreference resolution tool proposed by the Stanford NLP group (Lee et al., 2013) for English and Spanish.

- [vua-ontotagger](https://github.com/cltl/OntoTagger): module that inserts ontological labels to Wordnet synsets associated with terms or directly to the lemmas of the term based on the external resources provided. It is typically used to assign Predicate Matrix mappings to synsets.

- [vua-factualityr](https://github.com/newsreader/vua_factuality): module that indicates the certainty (certain/probable/possible) of an event, whether the event is confirmed or denied (pos/neg) and whether it is in the future (future/non-future).

- [vua-opinion-miner](https://github.com/cltl/opinion_miner_deluxe): Opinion miner based on machine learning for English and Dutch.

- [vua-eventcoreference](https://github.com/cltl/EventCoreference): set of functions in the EventCoreference module that read NAF files of English, Spanish and Dutch text and determines intra-document event-coreference based on lemmas and wordnet synsets.

- [TimePro](https://bitbucket.org/qwaider/textpro-en/src): English module to recognize temporal expression (part of TextPro tool)

- [HeidelTime NAF-wrapper](https://github.com/cltl/NAF-HeidelTime): NAF-wrapper around Strötgen (2013)'s HeidelTime that can be used for recognizing time expressions in Dutch and English, [see also](https://code.google.com/p/heideltime/). Note that the [Heideltime NAF-adaptation](https://github.com/ixa-ehu/ixa-pipe-time) is more robust than this wrapper. It works for Dutch and Spanish and can easily be adapted to work for English.

- [TempRelPro](https://github.com/paramitamirza/TempCauseRelPro): English module to recognize temporal relations (part of TextPro tool).

- [CausalRelPro](https://github.com/paramitamirza/TempCauseRelPro): English module to recognize causal relations (part of TextPro tool)

#### 

#### Dutch modules

- [ixa-pipe-tok](https://github.com/ixa-ehu/ixa-pipe-tok): A multilingual rule-based tokenizer for English, Spanish and Dutch compliant with Penn Treebank and Ancora Corpus tokenization.

- [Alpino\_naf\_wrapper](https://github.com/cltl/morphosyntactic_parser_nl): Naf-wrapper around the Alpino parser for Dutch (Bouma et al., 2001), which provides morphological (lemmas and POS tags) and syntactic information (constituents and dependencies), [see also](http://www.let.rug.nl/vannoord/alp/Alpino/).

- [ixa-pipe-nerc](https://github.com/ixa-ehu/ixa-pipe-nerc): English/Spanish/Dutch Named Entity Recognition with Perceptron models (Collins 2002) as implemented by Apache OpenNLP on CoNLL datasets for NER.

- [ixa-pipe-ned](https://github.com/ixa-ehu/ixa-pipe-ned): A client to query the DBpedia Spotlight for Named Entity Disambiguation (Mendes et al., 2011). This tool depends on the DBpedia Spotlight: <https://github.com/dbpedia-spotlight/dbpedia-spotlight> and is used for English, Dutch, Italian and Spanish.

- [dbpedia-ner](https://github.com/rubenIzquierdo/dbpedia_ner): A client to query the DBpedia Spotlight for Named Entity Recognition and Named Entity Disambiguation (Mendes et al., 2011). This tool depends on the DBpedia Spotlight: <https://github.com/dbpedia-spotlight/dbpedia-spotlight> and can be used for English, Dutch and Spanish.

- [vua-svm-wsd](https://github.com/cltl/svm_wsd): This program svm\_wsd implements a machine learning Word Sense Disambiguation system based on Support Vector Machines. It is used in the Dutch pipeline.

- [HeidelTime NAF-wrapper](https://github.com/cltl/NAF-HeidelTime): NAF-wrapper around Strötgen (2013)'s [HeidelTime](https://code.google.com/p/heideltime/) that can be used for recognizing time expressions in Dutch and English. This version uses Treetagger and only needs the NAF token-layer. The ixa-pipe-time wrapper ([Heideltime NAF-adaptation](https://github.com/ixa-ehu/ixa-pipe-time)) is more robust and recommended instead of this NAF-wrapper.

- [Heideltime NAF-adaptation](https://github.com/ixa-ehu/ixa-pipe-time): An integrated NAF-wrapper around Strötgen (2013)'s [HeidelTime](https://code.google.com/p/heideltime/) that can be used for recognizing time expressions in Spanish and Dutch. The wrapper works on the NAF term layer and can easily be adapted to English.

- [vua-ontotagger](https://github.com/cltl/OntoTagger): module that inserts ontological labels to Wordnet synsets associated with terms or directly to the lemmas of the term based on the external resources provided. It is typically used to assign Predicate Matrix mappings to synsets.

- [SONAR SRL](https://github.com/newsreader/vua-srl-nl): NAF-compliant reimplementation of De Clerq et al. (2012)'s SoNar SRL module.

- [vua-framenet-classifier](https://github.com/cltl/OntoTagger): module that reads NAF files of English, Spanish and Dutch text and applies FrameNet frames and roles to the SRL layer using the PredicateMatrix for the respective language.[see also](http://www.cltl.nl/results/software/eventcoreference/).

- [nominal-event-detection](https://github.com/cltl/OntoTagger): module that reads NAF files of Dutch and identifies which nouns refer to an event. This is another class within the vua-ontotagger package and it assume that the terms have been typed with class information through the ontotagger.

- [nominal-predicate-srl](https://github.com/newsreader/vua-srl-dutch-nominal-events/): a basic module that reads NAF files of Dutch and checks whether nominal events are modified by one or more prepositional phrases. These phrases are labelled as Arg1 or ArgM.

- [vua-eventcoreference](https://github.com/cltl/EventCoreference): set of functions in the EventCoreference module that read NAF files of English, Spanish and Dutch text and determines intra-document event-coreference based on lemmas and wordnet synsets.

- [vua-opinion-miner](https://github.com/cltl/opinion_miner_deluxe): Opinion miner based on machine learning for English and Dutch.

#### 

#### Italian modules

- [fbk-tokenpro](https://bitbucket.org/qwaider/textpro-ita/src/master/TextPro2.0): A tokenizer for Italian.

- [fbk-morphopro](https://bitbucket.org/qwaider/textpro-ita/src/master/TextPro2.0/modules/MorphoPro): A morphological analyzer for Italian.

- [fbk-tagpro](https://bitbucket.org/qwaider/textpro-ita/src/master/TextPro2.0/modules/TagPro): A POS-tagger for Italian using a Conditional Random Field algorithm assigning a subset of ELRA tagset.

- [fbk-lemmapro](https://bitbucket.org/qwaider/textpro-ita/src/master/TextPro2.0): A lemmatizer for Italian, disambiguating output of MorphoPro using TagPro.

- [fbk-entitypro](https://bitbucket.org/qwaider/textpro-ita/src/master/TextPro2.0/modules/EntityPro): A named entity recognition and classification system for Italian trained on ICAB (Magnini et al. 2006).

- [fbk-chunkpro](https://bitbucket.org/qwaider/textpro-ita/src/master/TextPro2.0/modules/ChunkPro): Module that provides chunks for Italian outputting constituents in of two categories: B-NP and B-VX.

- [fbk-depparserpro](https://bitbucket.org/qwaider/textpro-ita/src/master/TextPro2.0/modules/DepParserPro): Dependency parser for Italian based on the Malt Parser (Lavelli et al. 2013).

- [fbk-eventpro](https://bitbucket.org/qwaider/textpro-ita/src/master/TextPro2.0/modules/EventPro): module that identifies events and classifies them according to TimeML using a svm trained on the EVENTI-EVALITA2014 data.

- [fbk-factpro](https://bitbucket.org/qwaider/textpro-ita/src/master/TextPro2.0/modules/FactPro): module that determines factuality values according to the newsreader annotation guidelines trained on the Fact-Ita Bank corpus.

- [fbk-timepro](https://bitbucket.org/qwaider/textpro-ita/src/master/TextPro2.0/modules/TimePro): Italian module to identify and normalize time expressions. It uses a svm trained on the EVENTI-EVALITA2014 data.

- [fbk-temprelpro](https://bitbucket.org/qwaider/textpro-ita/src/master/TextPro2.0/modules/TempRelPro): Italian module to extract temporal relations between events and time expressions. It uses a svm trained on the EVENTI-EVALITA2014 data.

- [fbk-srl](https://bitbucket.org/qwaider/textpro-ita/src/master/FBK-SRL): SRL system for Italian based on dependency relations.

- [fbk-eventcoref](https://bitbucket.org/qwaider/textpro-ita/src/master/FBK-eventCoref): event coreference module for Italian.

- [fbk-timeanchor](https://bitbucket.org/qwaider/textpro-ita/src/master/FBK-timeAnchor): module that extracts relation between predicates and time anchors.

- [ixa-pipe-ned](https://github.com/ixa-ehu/ixa-pipe-ned): A client to query the DBpedia Spotlight for Named Entity Disambiguation (Mendes et al., 2011). This tool depends on the DBpedia Spotlight: <https://github.com/dbpedia-spotlight/dbpedia-spotlight> and is used for English, Dutch, Italian and Spanish.

#### 

#### Spanish modules

- [ixa-pipe-tok](https://github.com/ixa-ehu/ixa-pipe-tok): A multilingual rule-based tokenizer for English, Spanish and Dutch compliant with Penn Treebank and Ancora Corpus tokenization.

- [ixa-pipe-pos](https://github.com/ixa-ehu/ixa-pipe-pos): English/Spanish POS tagging with Perceptron models (Collins 2002) as implemented by Apache OpenNLP using the WSJ and Ancora corpus respectively.

- [ixa-pipe-parse](https://github.com/ixa-ehu/ixa-pipe-parse): English/Spanish Constituent Parsing with Maximum Entropy models (Ratnaparkhi 1999) as implemented by Apache OpenNLP using the Penn and Ancora Treebanks respectively.

- [ixa-pipe-nerc](https://github.com/ixa-ehu/ixa-pipe-nerc): English/Spanish/Dutch Named Entity Recognition with Perceptron models (Collins 2002) as implemented by Apache OpenNLP on CoNLL datasets for NER.

- [ixa-pipe-ned](https://github.com/ixa-ehu/ixa-pipe-ned): A client to query the DBpedia Spotlight for Named Entity Disambiguation (Mendes et al., 2011). This tool depends on the DBpedia Spotlight: <https://github.com/dbpedia-spotlight/dbpedia-spotlight> and is used for English, Dutch, Italian and Spanish.

- [ixa-pipe-wikify](https://github.com/ixa-ehu/ixa-pipe-wikify): A client to query the DBpedia Spotlight for wikification. This tool depends on the DBpedia Spotlight: <https://github.com/dbpedia-spotlight/dbpedia-spotlight> and is used for English and Spanish.

- [ixa-pipe-topic](https://github.com/ixa-ehu/ixa-pipe-topic): a module to extract a set of topics based on the Multilingual Eurovoc thesaurus descriptors and the JRC Eurovoc Indexer JEX. It is used for English and Spanish.

- [wsd-ukb](https://github.com/ixa-ehu/ukb): This program applies the so-called Personalized PageRank on a Lexical Knowledge Base (LKB) to rank the vertices of the LKB for word sense disambiguation for English and Spanish.

- [MATE-based Parser and SRL](https://github.com/newsreader/ixa-pipe-srl): a tool providing lemmatization, POS-tagging, dependencies and semantic roles for English and Spanish based on the MATE-tools (Björkelund et al., 2010).

- [CorefGraph](https://bitbucket.org/Josu/corefgraph): a python reimplementation of the coreference resolution tool proposed by the Stanford NLP group (Lee et al., 2013) for English and Spanish.

- [Heideltime NAF-adaptation](https://github.com/ixa-ehu/ixa-pipe-time): An integrated NAF-wrapper around Strötgen (2013)'s [HeidelTime](https://code.google.com/p/heideltime/) that can be used for recognizing time expressions in Spanish and Dutch. The wrapper works on the NAF term layer and can easily be adapted to English.

### Evaluation modules

- [Evaluation package](https://github.com/newsreader/evaluation): Modules for the evaluation of the event detection pipeline against the MEANTIME corpus.

### Additional modules and libraries

- [vua-multiwordtagger](https://github.com/cltl/MultiWordTagger): Java module that reads NAF with a term layer and uses a wordnet in WordNet-LMF format to detect multiword phrases. The output is NAF.

- [naf\_ukb](https://github.com/newsreader/naf_ukb): script to add sense information to NAF input, thus producing new NAF

- [vua-wordnettools](https://github.com/cltl/WordnetTools): Java module that reads any wordnet in WordNet-LMF format and carries out similarity measurements. This tools is used with the EventCoreference module.

- [NAF](https://github.com/newsreader/NAF): NewsReader Annotation Format documentation

All our software modules can be found on [GitHub](https://github.com/newsreader).
