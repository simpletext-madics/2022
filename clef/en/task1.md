# SimpleText@CLEF-2022 Tasks


[Home](./) | [Call for papers](./CFP) | [Important dates](./dates) | [Tasks](./tasks)  | [Tools](./tools) 
[Program](./program) | [Publications](./publications) | [Organisers](./organisers) | [Contact](./contact) | [CLEF-2023](https://simpletext-project.com/2023/clef)


---

## SimpleText Task Guidelines

We invite you to submit both automatic and manual runs! Manual intervention should be reported.

---

<button>[Access](./tasks)</button> | <button>[Shared task 1](./task1)</button> | <button>[Shared task 2](./task2)</button> | <button>[Shared task 3](./task3)</button>| <button>[Unshared task 4](./task4)</button>

<br>

## Task 1:  What is in (or out)? Select passages to include in a simplified summary, given a query.

The task aims at finding references in computer science that could be inserted as citations in original press articles of general audience for illustration, fact checking or actualization. For each of the selected references, more relevant sentences need to be extracted. These passages can be complex and require further simplification to be carried out in tasks 2 and 3. Task 1 focus on content retrieval.

**Corpus: DBLP + abstracts**

We use the Citation Network Dataset: DBLP+Citation, [ACM Citation network](https://www.aminer.org/citation). An ElasticSearch index is provided to participants accessible through a GUI API. A json dump of the index is also available for participants.

**Topics: Press articles**

Topics are a selection of 40 press article. 20 from a major international newspaper for a general audience and 20 from [Tech Xplore](https://techxplore.com/), enriched with queries manually extracted from the content of the article. It has been checked that at least 5 relevant abstracts can be found for for each query.

**Output format:**
 
Results should be provided in a TREC style tabulated format (with a ".csv" extention). The following columns are required (include these as the first line):

1. run_id: Run ID starting with teamid, followed by "_task1_" and run_name
2. manual: Whether the run is manual {0,1}
3. topic_id: Topic ID
4. query_id: Query ID used to retrieve the document (if one of the queries provided for the topic was used; 0 otherwise)
5. doc_id: ID of the retrieved document (to be extracted from the json output)
6. passage: Text of the selected passage
 
For each topic, the maximum number of distinct DBLP references (_id json field) is 100 and the total length of passages should not exceed 1000 tokens.

*Output example*:

| run_id | manual | topic_id | query_id | doc_id | passage |
|:-------|:-------|:---------|:-------|:--------|:-----|
| ST1_task1_1 | 0 | G01 | G01.1 | 1564531496 | A CDA is a mobile user device, similar to a Personal Digital Assistant (PDA). It supports the citizen when dealing with public authorities and proves his rights - if desired, even without revealing his identity. |
| ST1_task1_1 | 0 | G01 | G01.1 | 3000234933 | People are becoming increasingly comfortable using Digital Assistants (DAs) to interact with services or connected objects |
| ST1_task1_1 | 0 | G01 | G01.2 | 1448624402 | As extensive experimental research has shown individuals suffer from diverse biases in decision-making. |

*Output format checker*

You can use this python3 script to check the output format. The script requires Python 3 and the Pandas library:
[Download python output checker](../check_format.py)

**Disclaimer:** By downloading and using these data, you agree to the terms of use. Any use of the data for any purpose other than academic research, would be in violation of the intended use of these data. 

Therefore, by downloading and using these data you give the following assurances with respect to the SimpleText data:
1. You will not use nor permit others to use the data in the SimpleText datasets in any way except for classes and academic research.
2. You will not at any time disclose, give, or transmit (in any manner or form or for any purpose) the data (or any portion thereof) to any location or person, including but not limiting to making the data available on the Internet, and copying the data onto any cloud-based storage system.
3. You will not release nor permit others to release the dataset or any part of it to any person. 

In case of violation of the conditions for access to the data for scientific purposes, this access may be withdrawn from the research entity and/or from the researcher. The research entity may also be liable to pay compensation for damages for third parties or asked to take disciplinary action against the offending researcher. 


### Evaluation  
Sentence pooling and automatic metrics will be used to evaluate these results. The relevance of the source document will be evaluated as well as potential unresolved anaphora issues.

### Result submission:
Participants should put their run results into the folder Documents created for their user and **submit them by email** to *contact@simpletext-project.com*.

The email subject has to be in the format **\[CLEF TASK 1] TEAM_ID**. 

Runs should be submitted as a file in a TSV format. 

A confirmation email will be sent within 2 days after the submission deadline. 

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
