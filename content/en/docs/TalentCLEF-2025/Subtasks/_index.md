---
title: "Subtasks"
weight: 1
type: docs

resources:
  - src: "talentclef_2025_schema.png"  
---

<style>
.full-width-image {
            width: 60%;
            height: auto; /* Maintains the aspect ratio */
        }
</style>


### Task summary

The TalentCLEF 2025 task is structured into two independent sub-tasks, each taking account a particularyuse case scenario:

<img src="talentclef_2025_schema.png" alt="Madrid Gran Via" class="full-width-image">


#### Task A: Multilingula Job Title Matching

**Goal**: Develop systems that can identify and rank job titles most similar to a given job title. For each job title in a provided test set, participants must generate a ranked list of similar job titles from a specified knowledge base.

**Multilingual**: Participants are required to develop systems adapted to English, Spanish, German, and optionally, Chinese. 

**Data**: More information about data will be shown in <a  href='{{< relref "description_corpus" >}}'> Data section </a>, but essentially we will provide: 

- *Training Set*: A collection of 15,000 pairs of related job titles per language (English, Spanish, and German), each labeled with a concept identifier, will be provided to facilitate the creation of cross-language training samples. No training data will be provided in Chinese, opening the possibility to use different techniques to improve the performance of the models in this language.

- *Development Set*: Participants will receive a manually annotated evaluation set of 100 samples per language, consisting of a job title and its list of related job titles. A knowledge base of 2,500 job titles in each task language will also be provided for participants to generate predictions by ranking it. Additionally, cross-lingual data will be also released to allow them assess the models' ability to operate in that scenario.

- *Test set*: A background set comprising 5,000 job titles will be provided. The evaluation, however, will be conducted on a subset of the background set, that will be a gold standard corpus of 100 job titles in each language annotated with the same methodology as the development set. 

**Evaluation**: Details about evaluation will be placed in <a  href='{{< relref "evaluation" >}}'> evaluation page </a>, but the model performance will be evaluated with information retrieval metrics, being the **Mean Average Precision (MAP) the official metric of the task**, although results will be provided in other metrics such as Mean Reciprocal Rank (MRR) and Precision@K(1,5,10).


#### Task B: Job Title-Based Skill Prediction

**Goal**: Develop systems capable of retrieving relevant skills associated with a given job title. 


**Data**: More information about data will be shown in <a  href='{{< relref "description_corpus" >}}'> Data section </a>, but essentially we will provide: 

- *Training set*: A training set of at least 5.000 job titles along with the professional skills required for each position will be provided. This data is sourced from actual job descriptions and semi-automatically curated to ensure high accuracy in the training set.

- *Development set*: The development set will consist of 200 job titles along with their related skills, normalized to ESCO terminology. 

- *Test set*: The test set comprises a list of 500 job titles. The participants will be required to predict the related skills using the provided gazetteer. 

**Evaluation**: Details about evaluation will be placed in <a  href='{{< relref "evaluation" >}}'> evaluation page </a>, but the model performance in this task will be also evaluated with information retrieval metrics, being the **Mean Average Precision (MAP) the official metric of the task**, although results will be provided in other metrics such as Mean Reciprocal Rank (MRR) and Precision@K(1,5,10).


