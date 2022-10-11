# SimpleText@CLEF-2022 Home

---

[Home](./) | [Call for papers](./CFP) | [Important dates](./dates) | [Tasks](./tasks)  | [Tools](./tools) | 
[Program](./program) | [Publications](./publications) | [Organisers](./organisers) | [Contact](./contact) | [CLEF-2023](https://simpletext-project.com/2023/clef)
<!--- <img src="https://github.com/simpletext-madics/2021/blob/main/clef/FR.png?raw=true" width="30">https://simpletext-project.com/2022/clef/') --->

---

<img align="left" src="https://github.com/simpletext-madics/2021/blob/main/clef/simpletext-logo-blue.png?raw=true" width="100"/>  

## SimpleText: Automatic Simplification of Scientific Texts


### Lab topic and goals

SimpleText tackles technical challenges and evaluation challenges by providing appropriate data and benchmarks for text simplification. 
<br/>We propose the following tasks: 
* [TASK 1   What is in (or out)?](./task1)
Select passages to include in a simplified summary, given a query
* [TASK 2   What is unclear?](./task2)
Given a passage and a query, rank terms/concepts that are required to be explained for understanding this passage (definitions, context, applications,..) 
* [TASK 3   Rewrite this!](./task3)
Given a query, simplify passages from scientific abstracts 
* [UNSHARED TASK](./task4)
We welcome any submission that uses our data!


To face these challenges, SimpleText aims to answer the following research questions: 
<br/>RQ1 — What textual expression carrying information should be simplified (document and passage to be included in the simplified summary)?
<br/>RQ2 — What kind of background information should be provided (what terms should be contextualised giving a definition and/or application)? What information is the most relevant or helpful? 
<br/>RQ3 — How to improve the readability of a given short text (e.g. by reducing vocabulary and syntactic complexity) with acceptable rate of information distortion? 

### Significance for the field & Relevance to CLEF

Being science literate is an important ability for people. It is one
of the keys for critical thinking, objective decision-making and
judgment of the validity and significance of findings and arguments,
which allows discerning facts from fiction. Thus, having a basic
scientific knowledge may also help maintain one’s health, both
physiological and mental. The COVID-19 pandemic provides a good
example of such a matter. Understanding the issue itself, being aware
of and applying social distancing rules and sanitary policies,
choosing to use or avoid particular treatment or prevention procedures
can become crucial. In the context of a pandemic, the qualified and
timely information should reach everyone and be accessible. That is
what motivates projects such as [EasyCovid](https://easycovid19.org/).

However, scientific texts are often hard to understand as they require
solid background knowledge and use tricky terminology. Although there
were some recent efforts on text simplification, removing
such understanding barriers between scientific texts and general
public in an automatic manner is still an open challenge. SimpleText
Lab brings together researchers and practitioners working on the
generation of simplified summaries of scientific texts. It is a new
evaluation lab that follows up the [SimpleText-2021 Workshop](https://simpletext-project.com/2021/clef/en/). All
perspectives on automatic science popularisation are welcome,
including but not limited to: Natural Language Processing (NLP),
Information Retrieval (IR), Linguistics, Scientific Journalism, etc.

### Scenarios

The goal is to create a simplified summary of multiple scientific
documents based on a given query which provides the user with an
instant simplified summary on a specific topic he/she is interested in
or to generate a daily digest, for example for ArXiv.

### Evaluation setup, metrics, and tasks 

Dataset: We use the [Citation Network
Dataset](https://www.aminer.org/citation): DBLP+Citation, ACM Citation
network. An elastic search index is provided to participants
accessible through a GUI API. This Index is adequate to:
<br/>•	Apply basic passage retrieval methods based on vector or language IR models
<br/>•	Generate Latent Dirichlet Allocation models, 
<br/>•	Train Graph Neural Networks for citation recommendation as carried out in [Stellar Graph](https://stellargraph.readthedocs.io/) for example,
<br/>•	Apply deep bidirectionnal transformers for query expansion...

The data is two-fold: *Medecine* and *Computer Science*, two domains
among the most popular in forums like
[ELI5](https://www.reddit.com/r/explainlikeimfive/).


English queries: For this edition queries are a selection of recent press titles from The Guardian enriched with keywords manually extracted from the content of the articles. It has been checked that each keyword allows to extract at least 5 relevant abstracts. The use of these keywords is optional. 
<br/>Input format for all tasks:
<br/>•	Topics are in the MD format
<br/>•	Full text articles from The Guardian (link, folder with full texts in the MD format)
<br/>•	ElasticSearch index on the data server
<br/>•	DBLP full dump in the JSON.GZ format
<br/>•	DBLP abstracts extracted for each topic in the following MD format (doc_id, year, abstract)

## How to Cite
If you extend or use this work, please cite the [paper](https://doi.org/10.1007/978-3-031-13643-6_28) where it was introduced:
```
Liana Ermakova, Eric SanJuan, Jaap Kamps, Stéphane Huet, Irina Ovchinnikova, Diana Nurbakova, 
Sílvia Araújo, Radia Hannachi, Elise Mathurin, and Patrice Bellot. 2022. 
Overview of the CLEF 2022 SimpleText Lab: Automatic Simplification of Scientific Texts. 
In Experimental IR Meets Multilinguality, Multimodality, and Interaction: 13th International 
Conference of the CLEF Association, CLEF 2022, Bologna, Italy, September 5–8, 2022, Proceedings. 
Springer-Verlag, Berlin, Heidelberg, 470–494. https://doi.org/10.1007/978-3-031-13643-6_28
```
[Paper](https://doi.org/10.1007/978-3-031-13643-6_28)

[Dowload .BIB](../../BibTeX/ermakova_overview_2022.bib)

---

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [<img src="https://github.com/simpletext-madics/2022/blob/main/clef/en/clef_logo_2022.png?raw=true" width="150">](http://www.clef-initiative.eu/) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src="https://github.com/simpletext-madics/2021/blob/main/clef/logo-clef-initiative.png?raw=true" width="200">
