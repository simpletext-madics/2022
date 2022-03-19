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
* *snt_id*: a unique passage (sentence) identifier
* *source_snt*: passage texte
* *doc_id*: a unique source document identifier
* *query_id*: a query ID
* *query_text*: simplification should be done with regard to this query

*Input example:*

*{"snt_id":"G11.1_2892036907_2","source_snt":"With the ever increasing number of unmanned aerial vehicles getting involved in activities in the civilian and commercial domain, there is an increased need for autonomy in these systems too.","doc_id":2892036907,"query_id":"G11.1","query_text":"drones"}*

*Output format:*  

Simplified passages in a TSV tabulated file with the following fields:
* *run_id*: Run ID starting with **team_id_**
* *manual*: Whether the run is manual {0,1}
* *snt_id*: a unique passage (sentence) identifier from the input file 
* *simplified_snt*: Text of the simplified passage 

*Output example*:
{"run_id":"BTU","manual":1,"snt_id":"G11.1_2892036907_2","simplified_snt":"Drones are increasingly used in the civilian and commercial domain and need to be autonomous."}

### Evaluation
The simplified passages will be evaluated manually with eventual use of aggregating metrics.

### Result submission:
Participants should put their run results into the folder Documents created for their user and **submit them by email** to *contact@simpletext-project.com*.

The email subject has to be in the format **\[CLEF TASK 3] TEAM_ID**. 

Runs should be submitted as a <ins>ZIP folder of the corresponding JSON files</ins>. Manual runs are allowed to be submitted in a CSV format. 

A confirmation email will be sent within 2 days after the submission deadline. 
