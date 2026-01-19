---
title: Description of the Corpus
date: 2017-01-01
categories: [Examples]
weight: 1
tags: [test, sample, docs]
---
{{< alert color="warning" >}}We take the legal and ethical implications of using AI in Human Resources very seriously. It is important to note that the data we utilize inherently excludes any personal information, focusing solely on job titles and skills without involving personal/company information or geographic location.{{< /alert >}}

This page contains the corpus information for TalentCLEF 2026 tasks. You can access the link to download in [datasets](/docs/talentclef-2026/data/datasets/) page.


<details>
<summary><strong>Task A: Contextualized Job-Person Matching</strong></summary>
<strong>Summary:</strong>

The Task A corpus consists of job descriptions and résumés (CVs) in two languages: English and Spanish. Documents are synthetically generated from structured data derived from real job descriptions and curricula vitae, preserving realism while protecting privacy. The dataset covers multiple professional domains and sectors, selected via clustering over semantic vector representations to ensure diversity and representativeness.

Synthetic documents were generated in English and then manually reviewed to ensure quality and internal coherence. Job–candidate matches were annotated by human experts, who determined whether each résumé is suitable for a given job offer. The Spanish version was created through parallel translation using LLMs and validated by human reviewers to ensure semantic consistency and content equivalence across languages.

> Dataset files and detailed format specifications will be added here as they are released according to the official schedule.

<strong>Data:</strong>

1. **Development Set**: 

2. **Test Set**:

</details>

<details>
<summary><strong>Task B: Job-Skill Matching with Skill Type Classification</strong></summary>

<strong>Summary:</strong>

This dataset supports job title–based skill prediction in English across multiple job domains and professional sectors. It includes job titles and associated skills, curated and processed to facilitate training and evaluation for this task.

Participants must retrieve the skills from a gazetteer that best match each job title and classify each retrieved skill as <em>core</em> or <em>contextual</em>. Core skills are required to perform a job regardless of employer or work setting (i.e., essential for the role). Contextual skills depend on factors such as the organization, industry, or specific project, and can therefore be considered optional.

For example, a <strong>software engineer</strong> may be required to <em>develop mobile applications</em> in some contexts depending on the product and technical stack, but will generally be expected to <em>write code</em>. In this case, <em>write code</em> is a core skill, while <em>mobile application development</em> is a contextual skill.

> Dataset files and detailed format specifications will be added here as they are released according to the official schedule.

<strong>Data:</strong>
1. **Training Set**: 

2. **Validation Set**:

3. **Test Set**:

</details>