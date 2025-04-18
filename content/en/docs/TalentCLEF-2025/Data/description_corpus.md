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

    - *qrels*: This file defines the relationship between the query and the corpus elements. It does not include a column header, but one is shown here for illustrative purposes.
        - *q_id*: The identifier of the query.
        - *iter*: A reserved field (always 0).
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
    | q_id |iter | c_id | relevance |
    |------|------|------|-----------|
    | 1    | 0    | 2    | 1         |
    | 1    | 0    | 3    | 1         |
    | 1    | 0    | 4    | 1         |
    | 1    | 0    | 5    | 1         |
    | 1    | 0    | 6    | 1         |
    | 1    | 0    | 7    | 1         |
    | 1    | 0    | 8    | 1         |
    | 1    | 0    | 9    | 1         |

    </div>

    </div>



3. **Test Set**:
The test set is provided with two files: queries and corpus elements, and is provided separately for each language. For every language pair, participants need to generate a TREC Run File that adheres to the format specified in the [submission format section](docs/talentclef-2025/evaluation/submission_format/). The data structure is similar to the one from the validation files.

    - *Queries*: Contains the following fields:
        - *q_id*: A unique identifier for the query.
        - *jobtitle*: The job title used as the query.

    - *Corpus Elements*: Contains:
        - *q_id*: A unique identifier for each corpus element.
        - *jobtitle*:  The job title from the corpus element.

</details>

<details>
<summary><strong>Task B: Job Title-Based Skill Prediction Corpus</strong></summary>

<strong>Summary:</strong>

The dataset is designed to support job title-based skill prediction tasks in English across various job domains and professional sectors. It includes job titles and associated skills collected and processed to facilitate the training of models to solve this task. 

As with Task A, the training data uses public terminologies to represent a broad spectrum of job domains, while the validation and test sets are annotated by domain experts. This expert annotation follows strict guidelines and quality control measures to ensure consistent labeling and accurate representation of job-title-to-skill relationships.

<strong>Data:</strong>
1. **Training Set**: 

For generating the training data for Task B, the information available in ESCO has been used.  We have prepared the training data in three separate files: `job2skill.tsv`, `jobid2terms.json` and `skillid2terms.json`.

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
        - *esco_uri*: The ESCO URIs associated to `c_id`.
        - *skill_aliases*: The list aliases of the ESCO skill

    - *q_rels*: This file maps the relationship between the query and the corpus elements:
        - *q_id*: The identifier of the query.
        - *iter*: A reserved field (always 0).
        - *c_id*: The identifier of the corresponding corpus element.
        - *relevance*: A binary score (0 or 1) indicating the relevance of the corpus element to the query, where 1 signifies relevant and 0 non-relevant.

    Example of the content of these files:

    <div style="display: flex; gap: 20px;">

    <div style="flex: 1;">
    
    #### queries
    | q_id | jobtitle    |
    |------|-------------|
    | dev_qb_jt_1    | corporate governance analyst |

    </div>

    <div style="flex: 1;">
    
    #### corpus_elements
    | c_id | esco_uri                   | skill_aliases |
    |------|-----------------------------|----------------------------|
    dev_cb_sk_1	| http://data.europa.eu/esco/skill/1c460d2d-90c6-4fc9-ad49-febb6e15605a |	['pricing plans', 'price strategies', 'pricing tactics', 'pricing strategies', 'pricing strategy']
dev_cb_sk_2	| http://data.europa.eu/esco/skill/301a6581-e983-4bb6-8b31-b3ee2cbc2392	| ['putting out fires', ..., 'fires putting out']
dev_cb_sk_3	| http://data.europa.eu/esco/skill/a4881e54-6055-4e61-855a-0a56ced7cfa3 |	['online assessment', 'analysis of web strategy', 'web presence assessment', 'web strategy assessment']
dev_cb_sk_4	| http://data.europa.eu/esco/skill/efda73b4-5212-40a7-b2f8-d2f754ffdf2b	| ['keeping up with trends', 'keep pace with trends', 'follow trends', ..., 'keep up with trends']
dev_cb_sk_5	| http://data.europa.eu/esco/skill/22a173f5-868c-4d82-87e6-beed500ce070	| ['prepare tax returns form', ..., 'make tax returns forms ready', 'preparing tax returns forms']
dev_cb_sk_6	| http://data.europa.eu/esco/skill/97b890ff-acd7-46ad-8d3a-4186f4d42bbf	| ['tuning procedures', ..., 'tuning skills', 'tuning techniques']
dev_cb_sk_7	| http://data.europa.eu/esco/skill/d5c20065-1d1f-446b-8143-9d1e180c512b	| ['iconography methods', 'iconography']

    </div>

    <div style="flex: 1;">

    #### q_rels
    | q_id |iter | c_id | relevance |
    |------|------|------|-----------|
    | dev_qb_jt_1    | 0    | dev_cb_sk_1034| 1         |
    | dev_qb_jt_1    | 0    |dev_cb_sk_1087| 1         |
    | dev_qb_jt_1    | 0    |dev_cb_sk_1088 | 1         |
    | dev_qb_jt_1    | 0    | dev_cb_sk_1099   | 1         |
    | dev_qb_jt_1    | 0    | dev_cb_sk_1104 | 1         |
    | dev_qb_jt_1    | 0    | dev_cb_sk_1107    | 1         |
    | dev_qb_jt_1    | 0    | dev_cb_sk_1110  | 1         |
    | dev_qb_jt_1    | 0    | dev_cb_sk_1112 | 1         |

    </div>

    </div>

3. **Test Set**:
    The test set consists of two files: `queries` and `corpus elements`. Participants are required to produce a TREC Run File adhering to the structure outlined in the [submission format section](docs/talentclef-2025/evaluation/submission_format/). The test set includes a background set in the queries. 

    - *Queries*: Contains the following fields:
        - *q_id*: A unique identifier for the query.
        - *jobtitle*: The job title used as the query.

    - *Corpus Elements*: Contains:
        - *c_id*: A unique identifier for each corpus element.
        - *esco_uri*: The ESCO URIs associated to `c_id`.
        - *skill_aliases*: The list aliases of the ESCO skill

</details>