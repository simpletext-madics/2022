# SimpleText@CLEF-2022 Tasks

[Home](./) | [Call for papers](./CFP) | [Important dates](./dates) | [Tasks](./tasks)  | [Tools](./tools) 
[Program](./program) | [Publications](./publications) | [Organisers](./organisers) | [Contact](./contact) |


---

## SimpleText Task Guidelines

We invite you to submit both automatic and manual runs! Manual intervention should be reported.

---

<button>[Access](./tasks)</button> | <button>[Shared task 1](./task1)</button> | <button>[Shared task 2](./task2)</button> | <button>[Shared task 3](./task3)</button>| <button>[Unshared task 4](./task4)</button>

<br>

## Task 3: Rewrite this! Given a query, simplify passages from scientific abstracts. 

The goal of this task is to provide a simplified version of text passages (sentences) with regard to a query. Participants will be provided with queries and abstracts of scientific papers. The abstracts can be split into sentences. The simplified passages will be evaluated manually with eventual use of aggregating metrics.

**Intput format:** 
The train and and the test data are provided in JSON and CSV formats with the following fields:
* *snt_id*: a unique passage (sentence) identifier
* *source_snt*: passage texte
* *doc_id*: a unique source document identifier
* *query_id*: a query ID
* *query_text*: simplification should be done with regard to this query

*Input example:*

*{"snt_id":"G11.1_2892036907_2","source_snt":"With the ever increasing number of unmanned aerial vehicles getting involved in activities in the civilian and commercial domain, there is an increased need for autonomy in these systems too.","doc_id":2892036907,"query_id":"G11.1","query_text":"drones"}*

**Output format:** 
List of terms to be contextualized in a **JSON format** or a tabulated file TSV (for manual runs) with the following fields:
* *run_id*: Run ID starting with **team_id_**
* *manual*: Whether the run is manual {0,1}
* *snt_id*: a unique passage (sentence) identifier from the input file 
* *simplified_snt*: Text of the simplified passage 

*Output example*:
{"run_id":"BTU","manual":1,"snt_id":"G11.1_2892036907_2","simplified_snt":"Drones are increasingly used in the civilian and commercial domain and need to be autonomous."}

**Disclaimer:** By downloading and using these data, you agree to the terms of use. Any use of the data for any purpose other than academic research, would be in violation of the intended use of these data. 

Therefore, by downloading and using these data you give the following assurances with respect to the SimpleText data:
1. You will not use nor permit others to use the data in the SimpleText datasets in any way except for classes and academic research.
2. You will not at any time disclose, give, or transmit (in any manner or form or for any purpose) the data (or any portion thereof) to any location or person, including but not limiting to making the data available on the Internet, and copying the data onto any cloud-based storage system.
3. You will not release nor permit others to release the dataset or any part of it to any person. 

In case of violation of the conditions for access to the data for scientific purposes, this access may be withdrawn from the research entity and/or from the researcher. The research entity may also be liable to pay compensation for damages for third parties or asked to take disciplinary action against the offending researcher. 

### Evaluation
The simplified passages will be evaluated manually with eventual use of aggregating metrics.

### Result submission:
Participants should put their run results into the folder Documents created for their user and **submit them by email** to *contact@simpletext-project.com*.

The email subject has to be in the format **\[CLEF TASK 3] TEAM_ID**. 

Runs should be submitted as a <ins>ZIP folder of the corresponding JSON files</ins>. Manual runs are allowed to be submitted in a CSV format. 

A confirmation email will be sent within 2 days after the submission deadline. 

## How to Cite
If you extend or use this work, please cite the [paper](https://link.springer.com/chapter/10.1007/978-3-030-99739-7_46) where it was introduced:
```
Ermakova, L., Bellot, P., Kamps, J., Nurbakova, D., Ovchinnikova, I., SanJuan, E., Mathurin, E., Araújo, S., Hannachi, R., Huet, S., 
& Poinsu, N. (2022). Automatic Simplification of Scientific Texts: SimpleText Lab at CLEF-2022. In M. Hagen, S. Verberne, C. Macdonald, 
C. Seifert, K. Balog, K. Nørvåg, & V. Setty (Eds.), Advances in Information Retrieval (Vol. 13186, pp. 364–373). Springer International Publishing. 
https://doi.org/10.1007/978-3-030-99739-7_46
```
[Paper](https://link.springer.com/chapter/10.1007/978-3-030-99739-7_46)

[Dowload .BIB](../bib/simpletext_ecir_2022.bib)
