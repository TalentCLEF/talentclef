---
title: Description of the Corpus
date: 2017-01-01
categories: [Examples]
weight: 1
tags: [test, sample, docs]
---
{{< alert color="warning" >}}We take the legal and ethical implications of using AI in Human Resources very seriously. It is important to note that the data we utilize inherently excludes any personal information, focusing solely on job titles and skills without involving personal/company information or geographic location.{{< /alert >}}

{{< alert color="info" >}} Dataset files and detailed format specifications will be added here as they are released according to the official schedule.{{< /alert >}}


This page contains the corpus information for TalentCLEF 2026 tasks. You can access the link to download in [datasets](/docs/talentclef-2026/data/datasets/) page.


<details>
<summary><strong>Task A: Contextualized Job-Person Matching</strong></summary>
<strong>Summary:</strong>

The Task A corpus consists of job descriptions and résumés (CVs) in two languages: English and Spanish. Documents are synthetically generated from structured data derived from real job descriptions and curricula vitae, preserving realism while protecting privacy. The dataset covers multiple professional domains and sectors, selected via clustering over semantic vector representations to ensure diversity and representativeness.

Synthetic documents were generated in English and then manually reviewed to ensure quality and internal coherence. Job–candidate matches were annotated by human experts, who determined whether each résumé is suitable for a given job offer. The Spanish version was created through parallel translation using LLMs and validated by human reviewers to ensure semantic consistency and content equivalence across languages.

<strong>Data:</strong>

1. **Training Set**:

    No training set is provided for this task. However, participants are encouraged to use external resources or data from previous TalentCLEF editions if needed for their problem modeling and solution development.

2. **Development Set**: 

    For each language (English and Spanish),the development set is structured into three different components: *queries*, *corpus*, and *qrels.tsv*.

    - **Queries**: A folder containing 10 job description files. Each file is named with its unique identifier (e.g., `1234`, `5678`), and the file name serves as the `q_id` for that query.

    - **Corpus**: A folder containing 472 résumé files. Each file is named with its unique identifier (e.g., `1`, `2`, `3`), and the file name serves as the `c_id` for that corpus document.

    - **qrels.tsv**: This file defines the relationship between the queries and the corpus elements. It does not include a column header, but one is shown here for illustrative purposes:
        - *q_id*: The identifier of the query (corresponding to the query file name).
        - *iter*: A reserved field (always 0).
        - *c_id*: The identifier of the corresponding corpus element (corresponding to the corpus file name).
        - *relevance*: A binary score (0 or 1) indicating the relevance of the corpus element to the query, where 1 signifies relevant and 0 non-relevant.

        Example structure of qrels.tsv:

        | q_id | iter | c_id | relevance |
        |------|------|------|-----------|
        | 1234 | 0    | 1    | 1         |
        | 1234 | 0    | 5    | 0         |
        | 1234 | 0    | 12   | 1         |
        | 5678 | 0    | 2    | 1         |
        | 5678 | 0    | 8    | 0         |

3. **Test Set**:

</details>

<details>
<summary><strong>Task B: Job-Skill Matching with Skill Type Classification</strong></summary>

<strong>Summary:</strong>

This dataset supports job title–based skill prediction in English across multiple job domains and professional sectors. It includes job titles and associated skills, curated and processed to facilitate training and evaluation for this task.

Participants must retrieve the skills from a gazetteer that best match each job title and classify each retrieved skill as <em>core</em> or <em>contextual</em>. Core skills are required to perform a job regardless of employer or work setting (i.e., essential for the role). Contextual skills depend on factors such as the organization, industry, or specific project, and can therefore be considered optional.

For example, a <strong>software engineer</strong> may be required to <em>develop mobile applications</em> in some contexts depending on the product and technical stack, but will generally be expected to <em>write code</em>. In this case, <em>write code</em> is a core skill, while <em>mobile application development</em> is a contextual skill.


<strong>Data:</strong>
1. **Training Set**: 

    For generating the training data for Task B, the information available in ESCO has been used. We have prepared the training data in three separate files: `job2skill.tsv`, `jobid2terms.json` and `skillid2terms.json`.

    - `job2skill.tsv`: This file has been curated to include the most representative skills for each job title in ESCO. A filtering process has been applied to the number of skills per job title to avoid outliers. This file contains three columns:
        - *job_id*: ESCO identifier for the job position.
        - *skill_id*: ESCO identifier for the skill.
        - *rel_type*: Indicator specifying whether the *skill_id* is core or contextual for a specific *job_id*. It can have the value "essential" or "optional", labels that are aligned to the "core" and "contextual" labels that will be used in the development and test set.

        An example of the content of this file is shown below:

        | job_id                                                                 | skill_id                                                              | rel_type    |
    |------------------------------------------------------------------------|-----------------------------------------------------------------------|-------------|
    | [http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1](http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1) | [http://data.europa.eu/esco/skill/8b94aa1e-89c9-459d-b3b4-1dfab8dec2df](http://data.europa.eu/esco/skill/8b94aa1e-89c9-459d-b3b4-1dfab8dec2df) | essential   |
    | [http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1](http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1) | [http://data.europa.eu/esco/skill/f84a433f-34f1-4083-b0a3-24802623509c](http://data.europa.eu/esco/skill/f84a433f-34f1-4083-b0a3-24802623509c) | essential   |
    | [http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1](http://data.europa.eu/esco/occupation/f2b15a0e-e65a-438a-affb-29b9d50b77d1) | [http://data.europa.eu/esco/skill/fd33c66c-70c4-40e6-b87c-5495bd3bf26e](http://data.europa.eu/esco/skill/fd33c66c-70c4-40e6-b87c-5495bd3bf26e) | optional    |



    - `jobid2terms.json`: This JSON file contains *job_id* identifiers used in the training set for Task B as keys, and a list of valid lexical variants for each identifier as values.

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

3. **Test Set**:

</details>