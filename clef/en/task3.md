# SimpleText@CLEF-2022 Tasks

[Home](./) | [Call for papers](./CFP) | [Important dates](./dates) | [Pilot tasks](./tasks)  | [Tools](./tools) 
[Program](./program) | [Publications](./publications) | [Organisers](./organisers) | [Contact](./contact) | [<img src="https://github.com/simpletext-madics/2021/blob/main/clef/FR.png?raw=true" width="30">](../fr/task3)


---

## SimpleText Task Guidelines

We invite you to submit both automatic and manual runs! Manual intervention should be reported.

---

<button>[Access](./tasks)</button> | <button>[Task 1](./task1)</button> | <button>[Task 2](./task2)</button> | <button>[Task 3](./task3)</button>

<br>

## Task 3: Scientific text simplification – Language simplification

The goal of this task is to provide a simplified version of text passages. Participants will be provided with queries and abstracts of scientific papers. The abstracts can be split into sentences as in the exemple [https://guacamole.univ-avignon.fr/nextcloud/index.php/s/SQTdS2Yowf9dxNa](https://guacamole.univ-avignon.fr/nextcloud/index.php/s/SQTdS2Yowf9dxNa). The simplified passages will be evaluated manually with eventual use of aggregating metrics.

*Output format:*  

Simplified passages in a TSV tabulated file with the following fields:
* *run_id*: Run ID starting with team_id_
* *manual*: Whether the run is manual {0,1}
* *topic_id*: Topic ID 
* *topic_text*: Topic text
* *source_passage*: Source passage text 
* *simplified_passage*: Text of the simplified passage 

run_id &nbsp;&nbsp;&nbsp;&nbsp; manual &nbsp;&nbsp;&nbsp;&nbsp; topic_id &nbsp;&nbsp;&nbsp;&nbsp; topic_text &nbsp;&nbsp;&nbsp;&nbsp; doc_id &nbsp;&nbsp;&nbsp;&nbsp; source_passage &nbsp;&nbsp;&nbsp;&nbsp; simplified_passage

### Evaluation
The simplified passages will be evaluated manually with eventual use of aggregating metrics.

OUTPUT example:

| run_id | manual | topic_id | topic_text | doc_id | source_passage | simplified_passage |
|:-------|:-------|:---------|:-----------|:-------|:---------------|:-------------------|
| BTU | 1 | 1 | Digital assistants like Siri and Alexa entrench gender biases, says UN | 3003409254 | Automated decision making based on big data and machine learning (ML) algorithms can result in discriminatory decisions against certain protected groups defined upon personal data like gender, race, sexual orientation etc. Such algorithms designed to discover patterns in big data might not only pick up any encoded societal biases in the training data, but even worse, they might reinforce such biases resulting in more severe discrimination. | Automated decision-making may include sexist and racist biases and even reinforce them because their algorithms are based on the most prominent social representation in the dataset they use. |
