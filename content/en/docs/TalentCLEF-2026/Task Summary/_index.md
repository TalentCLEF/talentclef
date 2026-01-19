---
title: "Task Summary"
weight: 1
type: docs

resources:
  - src: "talentclef_2026_schema.png"  
---

<style>
.full-width-image {
            width: 90%;
            height: auto; /* Maintains the aspect ratio */
        }
</style>


The TalentCLEF 2026 task is structured into two independent sub-tasks, each taking account a particular use case scenario:

<img src="talentclef2026_image.png" alt="TalentCLEF diagram" class="full-width-image">


#### **Task A:  Contextualized Job-Person Matching**

**Goal**: Develop systems capable of identifying and ranking the most suitable candidate résumés for a given job offer. For each job description in the test set, participants must provide a ranked list of candidate profiles according to their relevance to the position.

**Multilingual**: Participants are required to develop systems adapted to English and optionally systems that operate in cross-lingual scenarios involving English and Spanish.

**Data**: More information about data will be shown in <a  href='{{< relref "docs/talentclef-2026/data/description_corpus" >}}'> Data section</a>, but we will provide a synthetically generated dataset built from structured resources derived from real job descriptions and résumés, containing no personal information, and without posing privacy risks

- *Development Set*: Participants will receive a small manually annotated development set of 30 samples per language, consisting of a job description and its list of relevant résumés. A knowledge base of around 100 résumés will also be provided for participants to generate predictions by ranking it. 

- *Test set*: A background set of job offers will be provided. The evaluation, however, will be conducted on a subset of the background set, that will be a gold standard corpus of 50 job offers in each language annotated with the same methodology as the development set.

**Evaluation**: Details about evaluation will be placed in <a  href='{{< relref "docs/talentclef-2026/evaluation/" >}}'> Evaluation page</a>, but the model performance will be evaluated with information retrieval metrics, being the **Mean Average Precision (MAP) the official metric of the task**, although results will be provided in other metrics such as Mean Reciprocal Rank (MRR) and Precision@K(1,5,10).


#### **Task B: Job-Skill Matching with Skill Type Classification**

**Goal**: Develop systems capable of retrieving relevant skills associated with a given job title and additionally classifying each retrieved skill as either core, complementary or transversal. 


**Data**: More information about data will be shown in <a  href='{{< relref "docs/talentclef-2026/data/description_corpus" >}}'> Data section</a>, but essentially we will provide: 

- *Training set*: A training set of at least 5.000 job titles along with the professional skills required for each position will be provided. 

- *Development set*: The development set will consist of 200 job titles along with their related skills, normalized to ESCO terminology. The data will include a new annotation layer indicating the relevance of each skill for the job position, specifying whether the skill is considered core or contextual. Core skills are those required to perform a specific job independently of the work context or employer and can thus be seen as essential for the position, whereas contextual skills depend on factors such as the organization or industry and can therefore be seen as optional.

- *Test set*: The test set comprises a list of 500 job titles. The participants will be required to predict the related skills using the provided gazetteer, but also the skill type classification.

**Evaluation**: Details about evaluation will be shared soon in the <a  href='{{< relref "docs/talentclef-2026/evaluation/" >}}'> Evaluation page</a>, but the model performance will be evaluated with information retrieval metrics, such as the **Normalized Discounted Cumulative Gain (nDCG)** and **Mean Average Precision (MAP)**, although results will be provided also using other metrics such as Mean Reciprocal Rank (MRR) and Precision@K(1,5,10).


