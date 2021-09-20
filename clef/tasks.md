
# SimpleText@CLEF-2021 Pilot tasks

[Home](./) | [Call for papers](./CFP) | [Important dates](./dates) | [Pilot tasks](./tasks)  
[Program](./program) | [Publications](./publications) | [Organisers](./organisers) | [Contact](./contact) | [<img src="../FR.png" width="30">](../fr/tasks)

---

## SimpleText Pilot Task Guidelines

We invite you to submit both automatic and manual runs! Manual intervention should be reported.

---

<button>[Access](./tasks)</button> | <button>[Pilot task 1](./task1)</button> | <button>[Pilot task 2](./task2)</button> | <button>[Pilot task 3](./task3)</button>

<br>

## Access
Please register at the SimpleText@CLEF workshop in order to access the data: [http://clef2021-labs-registration.dei.unipd.it/](http://clef2021-labs-registration.dei.unipd.it/)  
After registration, you will receive an email with information on how to log in to the data server: [https://guacamole.univ-avignon.fr](https://guacamole.univ-avignon.fr)

### Result submission:
Participants should put their run results into the folder Documents created for their user.

### 2021 DataSet
For this edition we use the Citation Network Dataset: DBLP+Citation, ACM Citation network ([https://www.aminer.org/citation](https://www.aminer.org/citation)). An elastic search index is provided to participants accessible through a GUI API. This Index is adequate to:
* apply basic passage retrieval methods based on vector or language IR models
* generate Latent Dirichlet Allocation models,
* train Graph Neural Networks for citation recommendation as carried out in [https://stellargraph.readthedocs.io/](https://stellargraph.readthedocs.io/) for example,
* apply deep bi directionnal transformers for query expansion.
* and much more…

### 2021 Queries
For this edition queries are a selection of recent press titles from The Guardian enriched with keywords manually extracted from the content of the article. It has been checked that each keyword allows to extract at least 5 relevant abstracts. The use of these keywords is optional.

*Input format for all tasks:*
* Topics are in the MD format

<img src="../Query1.png">

* Full text articles from The Guardian (link, folder query_related_content with full texts in the MD format)
* ElasticSearch index on the following data server (e.g.): [https://guacamole.univ-avignon.fr/nextcloud/index.php/apps/files/?dir=/simpleText/queries&fileid=570352](https://guacamole.univ-avignon.fr/nextcloud/index.php/apps/files/?dir=/simpleText/queries&fileid=570352)
* DBLP full dump in the JSON.GZ format
* DBLP abstracts extracted for each topic in the following MD format (doc_id, year, abstract):

<img src="../MDformat.png">
