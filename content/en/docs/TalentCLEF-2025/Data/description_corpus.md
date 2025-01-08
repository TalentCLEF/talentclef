---
title: Description of the Corpus
date: 2017-01-01
categories: [Examples]
weight: 1
tags: [test, sample, docs]
---
{{< alert color="warning" >}}We take the legal and ethical implications of using AI in Human Resources very seriously. It is important to note that the data we utilize inherently excludes any personal information, focusing solely on job titles and skills without involving personal/company information or geographic location.{{< /alert >}}

This page contains the corpus information for TalentCLEF 2025 tasks. You can access the link to download in [datasets](/docs/talentclef-2025/data/datasets/) page.

<details>
<summary><strong>Task A: Multilingual Job Title Matching Corpus</strong></summary>
<strong>Summary:</strong>

The corpus used for Task A consists of a set of job titles in three languages: English, Spanish and German, from different job domains and professional sectors. These job titles have been collected and processed in order to facilitate the identification and comparison of equivalent titles across languages. 

The training corpus has been generated using public terminologies, ensuring that the job titles are representative of a wide range of job domains and aligned with standard market terminology.

On the other hand, the validation and test corpora have been annotated by domain experts, following well-defined guidelines to ensure consistency and quality of labels. This annotation process, performed with specialized tools, included several stages of quality control to ensure that the labels were accurate and that the annotated titles accurately reflected the relationships between the different languages in a work environment.

<strong>Data:</strong>

1. **Training Set**: 
The training data is provided in a tabular format with three columns:
    - *family_id*: The ISCO family id representing the group to which the job identifier belongs.
    - *id*: An ESCO identifier indicating the origin of the pair's job titles.
    - *jobtitle_1*: The first job title in the pair.
    - *jobtitle_2*: A second job title related to *jobtitle_1*.

    Each dataset is provided in separate files for each language involved in the task. The files are named according to the language, with the following format:
    - `taskA_training_en.tsv`: Contains related job titles in English.
    - `taskA_training_es.tsv`: Contains related job titles in Spanish.
    - `taskA_training_de.tsv`: Contains related job titles in German.

    An example of the content of these files is shown below:

    
  | family_id                                         | id                                                                                             | jobtitle_1               | jobtitle_2                  |
|---------------------------------------------------|------------------------------------------------------------------------------------------------|---------------------------|-----------------------------|
| http://data.europa.eu/esco/isco/C2512            | http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1                    | desarrollador de software | desarrolladora de soluciones |
| http://data.europa.eu/esco/isco/C2512            | http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1                    | desarrollador de software | ingeniera de aplicaciones   |
| http://data.europa.eu/esco/isco/C2512            | http://data.europa.eu/esco/occupation/d0aa0792-4345-474b-9365-686cf4869d2e                    | diseñador de software     | ingeniero de software       |


2. **Validation Set**:
    The validation set is structured into three diferent files: *queries*, *corpus elements* and *q_rels*, and is provided separately for each language.
    - *Queries*: The queries file contains the following fields:
        - *q_id*: A unique identifier for the query.
        - *jobtitle*: The job title used as the query.

    - *Corpus Elements*: The corpus elements file contains the following fields:
        - *c_id*: A unique identifier for each corpus element.
        - *jobtitle*: The job title present in the corpus.

    - *q_rels*: This file maps the relationship between the query and the corpus elements:
        - *q_id*: The identifier of the query.
        - *c_id*: The identifier of the corresponding corpus element.
        - *relevance*: A binary score (0 or 1) indicating the relevance of the corpus element to the query, where 1 signifies relevant and 0 non-relevant.

    We will provide validation set in *english*, *spanish*, *german* and *chinese*.

    Example of the content of these files for english:


    <div style="display: flex; gap: 20px;">

    <div style="flex: 1;">
    
    #### queries
    | q_id | jobtitle    |
    |------|-------------|
    | 1    | 3d animator |

    </div>

    <div style="flex: 1;">
    
    #### corpus_elements
    | c_id | jobtitle                   |
    |------|-----------------------------|
    | 1    | animation artist            |
    | 2    | 3d character animator       |
    | 3    | character technical director|
    | 4    | character designer          |
    | 5    | animation lead              |
    | 6    | 3d generalist               |
    | 7    | animator                    |
    | 8    | character rigger            |
    | 9    | character animator          |

    </div>

    <div style="flex: 1;">

    #### q_rels
    | q_id | c_id | relevance |
    |------|------|-----------|
    | 1    | 2    | 1         |
    | 1    | 3    | 1         |
    | 1    | 4    | 1         |
    | 1    | 5    | 1         |
    | 1    | 6    | 1         |
    | 1    | 7    | 1         |
    | 1    | 8    | 1         |
    | 1    | 9    | 1         |

    </div>

    </div>



3. **Test Set**:
The test set consists of two components, which are designed to evaluate system predictions based on language and job title retrieval tasks. The participant should generate a *q_rels* based on the queries and corpus elements provided. 

    - *Queries*: Contains the following fields:
        - *q_id*: A unique identifier for the query.
        - *jobtitle*: The job title used as the query.
        - *lang*: The language of the corpus element's job title.

    - *Corpus Elements*: Contains:
        - *q_id*: A unique identifier for each corpus element.
        - *jobtitle*:  The job title from the corpus element.
        - *lang*: The language of the corpus element's job title.

</details>

<details>
<summary><strong>Task B: Job Title-Based Skill Prediction Corpus</strong></summary>

<strong>Summary:</strong>

The dataset is designed to support job title-based skill prediction tasks in English across various job domains and professional sectors. It includes job titles and associated skills collected and processed to facilitate the training of models to solve this task. 

As with Task A, the training data uses public terminologies to represent a broad spectrum of job domains, while the validation and test sets are annotated by domain experts. This expert annotation follows strict guidelines and quality control measures to ensure consistent labeling and accurate representation of job-title-to-skill relationships.

<strong>Data:</strong>
1. **Training Set**: 

For generating the training data for Task B, the information available in ESCO has been used.  We have prepared the training data in three separate files: `job2skill.tsv`, `jobid2terms.json` and `skillid2terms.json`.

Para la generación de datos de entrenamiento para la Task B se ha utilizado la información presente en ESCO. El traininn data se provee en 3 diferent files: `job2skill.tsv`, `jobid2terms.json` y `skillid2terms.json`.

- `job2skill.tsv`: This file has been curated to include the most representative skills for each job title in ESCO. A filtering process has been applied to the number of skills per job title to avoid outliers. This file contains three columns:
    - *job_id*: ESCO identifier for the job position.
    - *skill_id*: ESCO identifier for the skill.
    - *rel_type*:Indicator specifying whether the *skill_id* is essential or optional for a specific *job_id*. It can have the value "essential" or "optional."



    An example of the content of this file is shown below:

    | job_id                                                                 | skill_id                                                              | rel_type    |
|------------------------------------------------------------------------|-----------------------------------------------------------------------|-------------|
| [http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1](http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1) | [http://data.europa.eu/esco/skill/8b94aa1e-89c9-459d-b3b4-1dfab8dec2df](http://data.europa.eu/esco/skill/8b94aa1e-89c9-459d-b3b4-1dfab8dec2df) | essential   |
| [http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1](http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1) | [http://data.europa.eu/esco/skill/f84a433f-34f1-4083-b0a3-24802623509c](http://data.europa.eu/esco/skill/f84a433f-34f1-4083-b0a3-24802623509c) | essential   |
| [http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1](http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1) | [http://data.europa.eu/esco/skill/fd33c66c-70c4-40e6-b87c-5495bd3bf26e](http://data.europa.eu/esco/skill/fd33c66c-70c4-40e6-b87c-5495bd3bf26e) | optional    |



- `jobid2terms.json`: This JSON file contains *job_id* identifiers used in the training set for Task A as keys, and a list of valid lexical variants for each identifier as values.

    ```json
    {
        "http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1": [
            "application developer", "application programmer", "applications engineer",
            "application software developer", "battery software developer",
            "developer of software", "programmer", "soft developer",
            "software developer", "software developers", "software engineer",
            "software specialist", "solutions developer"
        ]
        ...
    }
    ```

- `skillid2terms.json`: This JSON file contains *skill_id* identifiers as keys, and a list of valid lexical variants for each identifier as values.

    ```json
    {
        "http://data.europa.eu/esco/skill/f84a433f-34f1-4083-b0a3-24802623509c": [
            "web services", "web services systems"
        ],
        "http://data.europa.eu/esco/skill/fd33c66c-70c4-40e6-b87c-5495bd3bf26e": [
            "design user interface"
        ]
    }
    ```



2. **Validation Set**:
    The validation set is divided into three diferent files: *queries*, *corpus elements* and *q_rels*:
    - *Queries*: Contains the following fields:
        - *q_id*: A unique identifier for the query.
        - *jobtitle*: The job title used as the query.

    - *Corpus Elements*: Contains:
        - *c_id*: A unique identifier for each corpus element.
        - *skill*: The skill included as a corpus element.

    - *q_rels*: This file maps the relationship between the query and the corpus elements:
        - *q_id*: The identifier of the query.
        - *c_id*: The identifier of the corresponding corpus element.
        - *relevance*: A binary score (0 or 1) indicating the relevance of the corpus element to the query, where 1 signifies relevant and 0 non-relevant.

3. **Test Set**:
    The test set consists of two files, `queries` and `corpus elements`. The participant should generate a *q_rels* file as prediction based on the queries and corpus elements provided. 

    - *Queries*: Contains the following fields:
        - *q_id*: A unique identifier for the query.
        - *jobtitle*: The job title used as the query.

    - *Corpus Elements*: Contains:
        - *q_id*: A unique identifier for each corpus element.
        - *skill*:  The skill associated with the corpus element.


</details>