# SimpleText@CLEF-2022 Tasks

[Home](./) | [Call for papers](./CFP) | [Important dates](./dates) | [Tasks](./tasks)  | [Tools](./tools) 
[Program](./program) | [Publications](./publications) | [Organisers](./organisers) | [Contact](./contact) |


---

## SimpleText Task Guidelines

We invite you to submit both automatic and manual runs! Manual intervention should be reported.

---

<button>[Access](./tasks)</button> | <button>[Shared task 1](./task1)</button> | <button>[Shared task 2](./task2)</button> | <button>[Shared task 3](./task3)</button>| <button>[Unshared task 4](./task4)</button>

<br>

## Task 2: What is unclear? Given a passage and a query, rank terms/concepts that are required to be explained for understanding this passage (definitions, context, applications,..).

The goal of this task is to decide which terms (up to 5) require explanation and contextualization to help a reader to understand a complex scientific text – for example, with regard to a query, terms that need to be contextualized (with a definition, example and/or use-case). For each passage, participants should provide a ranked list of difficult terms with corresponding scores on the scale 1-3 (3 to be the most difficult terms, while the meaning of terms scored 1 can be dervied or guessed) and on the scale 1-5 (5 to be the most difficult terms). Passages (sentences) are considered to be independent, i.e. difficult term repitition is allowed. Term pooling and automatic metrics (accuracy of term binary classification, NDCG for term ranking, kappa statistics...) will be used to evaluate these results.

**Intput format:** 
The train and and the test data are provided in JSON and CSV formats with the following fields:
* *snt_id*: a unique passage (sentence) identifier
* *source_snt*: passage texte
* *doc_id*: a unique source document identifier
* *query_id*: a query ID
* *query_text*: difficult terms should be extracted from sentences with regard to this query

*Input example:*

*{"snt_id":"G06.2_2548923997_3","source_snt":"These communication systems render self-driving vehicles vulnerable to many types of malicious attacks, such as Sybil attacks, Denial of Service (DoS), black hole, grey hole and wormhole attacks.","doc_id":2548923997,"query_id":"G06.2","query_text":"self driving"}*

**Output format:** 

List of terms to be contextualized in a **JSON format** or a tabulated file TSV (for manual runs) with the following fields:
* *run_id*: Run ID starting with **team_id_**
* *manual*: Whether the run is manual {0,1}
* *snt_id*: a unique passage (sentence) identifier from the input file 
* *term*: Term or other phrase to be explained
* *term_rank_snt*: term difficulty rank within the given sentence
* *score_5*: term difficulty score on the scale from 1 to 5 (5 to be the most difficult terms)
* *score_3*: term difficulty score on the scale from 1 to 3 (3 to be the most difficult terms)

*Output example*:

*{"run_id":"NP","manual":1,"snt_id":"G06.2_2548923997_3","term":"black hole attack","term_rank_snt":1,"score_5":5,"score_3":3},{"run_id":"NP","manual":1,"snt_id":"G06.2_2548923997_3","term":"grey hole attack","term_rank_snt":2,"score_5":5,"score_3":3},{"run_id":"NP","manual":1,"snt_id":"G06.2_2548923997_3","term":"Sybil attack","term_rank_snt":3,"score_5":5,"score_3":3},{"run_id":"NP","manual":1,"snt_id":"G06.2_2548923997_3","term":"wormhole attack","term_rank_snt":4,"score_5":5,"score_3":3},{"run_id":"NP","manual":1,"snt_id":"G06.2_2548923997_3","term":"Denial of service attack","term_rank_snt":5,"score_5":4,"score_3":3}*

### Evaluation
Term pooling and automatic metrics (accuracy of term binary classification, NDCG for term ranking, kappa statistics...) will be used to evaluate these results.

### Result submission:
Participants should put their run results into the folder Documents created for their user and **submit them by email** to *contact@simpletext-project.com*.

The email subject has to be in the format **\[CLEF TASK 2] TEAM_ID**. 

Runs should be submitted as a <ins>ZIP folder of the corresponding JSON files</ins>. Manual runs are allowed to be submitted in a CSV format. 

A confirmation email will be sent within 2 days after the submission deadline. 
