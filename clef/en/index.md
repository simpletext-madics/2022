[Home](./) | [Call for papers](./CFP) | [Important dates](./dates) | [Tasks](./tasks)  | [Tools](./tools) 
[Program](./program) | [Publications](./publications) | [Organisers](./organisers) | [Contact](./contact) | [<img src="https://github.com/simpletext-madics/2021/blob/main/clef/FR.png?raw=true" width="30">](https://simpletext-madics.github.io/2022/clef/)

---

<img align="left" src="https://github.com/simpletext-madics/2021/blob/main/clef/simpletext-logo-blue.png?raw=true" width="100"/>  

## SimpleText: Automatic Simplification of Scientific Texts

*SimpleText is a new lab organised as a part of [CLEF-2022 conference](https://clef2022.clef-initiative.eu/index.php), initiated by [CLEF initiative](http://www.clef-initiative.eu/).*

### Lab topic and goals

SimpleText tackles technical challenges and evaluation challenges by providing appropriate data and benchmarks for text simplification. 
<br/>We propose three tasks: 
* (1) passage selection and summarization
* (2) comprehensibility
* (3) readability of texts

To face these challenges, SimpleText aims to answer the following research questions: 
<br/>RQ1 - What textual expression carrying information should be simplified (document and passage to be included in the simplified summary)? 
<br/>RQ2 - What kind of background information should be provided (what terms should be contextualised by giving a definition and/or application)? What information is the most relevant or helpful? 
<br/>RQ3 - How to improve the readability of a given short text (e.g. by reducing vocabulary and syntactic complexity) with acceptable rate of information distortion? 

### Significance for the field & Relevance to CLEF

Information access systems provide users with key information from reliable sources such as scientific literature; however, non-experts may tend to avoid these sources due to its complex language or their lack of background knowledge. Text simplification removes some of these barriers. SimpleText will be a step forward to make research really open, accessible and understandable for everyone and help to counter fake news based on scientific results. It will allow people to read faster, which will make them more aware of scientific results. This is especially important with an explosion of open science during the current COVID-19 pandemic. Simplified texts are more accessible for non-native speakers, young readers and people with reading disabilities. Also, text simplification allows the improvement of natural language processing (NLP) applications, including machine translation results. Automatic text simplification could be useful for various domains such as scientific communication, science journalism, politics and education. Text simplification can be used in translation (computer-aided translation & website localization, pre-editing) and technical writing.

Although few studies have been carried out in the field of automatic text simplification [1], [2], it still remains a challenging task. To the best of our knowledge, no multilingual IR dataset exists where a summary is written in a different language than a full text. The vast majority of the literature is dedicated to texts in English. Few works were carried out for French data [3]–[7] and they do not consider the tasks of information selection nor provide background knowledge. In contrast to previous projects, SimpleText aims to provide lacking background knowledge but keeping the text as short as possible in order to help a user understand a complex text which cannot be further simplified without severe information distortion. Searching for background knowledge is close to INEX/CLEF Tweet Contextualization track 2011-2014 [27] and CLEF Cultural micro-blog Contextualization 2016, 2017 Workshop [34], but SimpleText differs from them by making a focus on a selection of notions to be explained and the helpfulness of the information provided rather than its relevance.

### Scenarios

The goal is to create a simplified summary of multiple scientific documents based on a given query which provides the user with an instant simplified summary on a specific topic he/she is interested in or to generate a daily digest, for example for ArXiv. 

### Evaluation setup, metrics, and tasks 

English dataset: We use the Citation Network Dataset: DBLP+Citation, ACM Citation network (https://www.aminer.org/citation). An elastic search index is provided to participants accessible through a GUI API. This Index is adequate to:
<br/>-	apply basic passage retrieval methods based on vector or language IR models
<br/>-	generate Latent Dirichlet Allocation models, 
<br/>-	train Graph Neural Networks for citation recommendation as carried out in https://stellargraph.readthedocs.io/ for example,
<br/>-	apply deep bi directionnal transformers for query expansion...
English queries: For this edition queries are a selection of recent press titles from The Guardian enriched with keywords manually extracted from the content of the articles. It has been checked that each keyword allows to extract at least 5 relevant abstracts. The use of these keywords is optional. 
<br/>Input format for all tasks:
<br/>●	Topics are in the MD format
<br/>●	Full text articles from The Guardian (link, folder with full texts in the MD format)
<br/>●	ElasticSearch index on the data server
<br/>●	DBLP full dump in the JSON.GZ format
<br/>●	DBLP abstracts extracted for each topic in the following MD format (doc_id, year, abstract)

---

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [<img src="https://github.com/simpletext-madics/2021/blob/main/clef/logo-clef-2021.png?raw=true" width="150">](http://www.clef-initiative.eu/) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [<img src="https://github.com/simpletext-madics/2021/blob/main/clef/logo-clef-initiative.png?raw=true" width="200">](http://clef2021.clef-initiative.eu/) 
