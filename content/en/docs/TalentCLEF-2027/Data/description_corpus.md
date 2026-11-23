---
title: Description of the Corpus
date: 2026-09-18
categories: [Examples]
weight: 1
tags: [test, sample, docs]
---
{{< alert color="warning" >}}We take the legal and ethical implications of using AI in Human Resources very seriously. The data we use inherently excludes any personal information. When context is provided, it is generated using generative Large Language Models, so all the information is produced without involving personal/company information or geographic location.{{< /alert >}}

{{< alert color="info" >}}The sample set has been released. Dataset files and detailed format specifications for the training, development and test sets will be added here as they are released according to the <a  href='{{< relref "docs/talentclef-2027/schedule/" >}}'>official schedule</a>.{{< /alert >}}

This page contains the corpus information for TalentCLEF 2027 tasks. You can access the link to download in [datasets](/docs/talentclef-2027/data/datasets/) page.

Both datasets are annotated by expert annotators with professional experience in Human Resources.

<details>
<summary><strong>Task 1: Contextualized Job-Person Matching</strong></summary>

<strong>Summary:</strong>

The dataset reuses and extends the 2026 data-generation pipeline: synthetic, multilingual job vacancies and résumés containing no personal information, covering **English, Spanish and, new for this edition, French**. Subtask 1.2 additionally provides evidence-unit annotations for a subset of job offer–candidate pairs.

<strong>Sample set:</strong>

The sample set (`sample_Task1.zip`) contains one language-specific subfolder for each of English (`en`), Spanish (`es`) and French (`fr`). Each language subfolder is structured into three components: *queries*, *corpus_elements* and *qrels.tsv*.

- **queries**: A folder containing the job description files (e.g., `sample_qa_1.txt`, referred to as `qa_1` in `qrels.tsv`).

- **corpus_elements**: A folder containing the résumé files (e.g., `sample_ca_1.txt`, referred to as `ca_1` in `qrels.tsv`).

- **qrels.tsv**: This file defines the relationship between the queries and the corpus elements, in TREC format. It does not include a column header, but one is shown here for illustrative purposes:
    - *q_id*: The identifier of the query.
    - *iter*: A reserved field (always 0).
    - *c_id*: The identifier of the corresponding corpus element.
    - *relevance*: The relevance of the corpus element to the query.

    Content of the sample `qrels.tsv`:

    | q_id | iter | c_id | relevance |
    |------|------|------|-----------|
    | qa_1 | 0    | ca_1 | 0         |

Example of a query (`en/queries/sample_qa_1.txt`, truncated):

```text
Senior Financial Analyst

We are seeking a dedicated Senior Financial Analyst to join our team and contribute to financial planning and analysis, data-driven decision-making, and regulatory compliance support.

About the Role
The Senior Financial Analyst will perform financial analysis, develop management reports, and support compliance initiatives, including anti-money laundering and sanctions monitoring. ...

Required Skills
- Anti-Money Laundering (AML)
- Sanctions and screening
- Investigation
- Data Analysis
...
```

</details>

<details>
<summary><strong>Task 2: Paragraph-to-Skill Ranking under Negation</strong></summary>

<strong>Summary:</strong>

The dataset consists of short paragraphs of job-market text paired with ESCO skills annotated for polarity (required, negated, or neither). The training set is deliberately kept small, as the negation/polarity signal is scarce; participants may freely enrich it with other skill-extraction datasets.

<strong>Sample set:</strong>

The sample set (`sample_Task2.zip`) contains a single JSON file, `task2_sample.json`, with 5 synthetic job postings in English. Each entry has an identifier (`id`), the text of the posting (`text`) and a list of `annotations`. Each annotation has:

- `skill`: the preferred label of the ESCO skill.
- `label`: the polarity of the skill in the text (`1` or `-1`, see below).
- `evidence`: the sentence of the text that motivates the annotation.
- `start`, `end`: the character offsets of the evidence in `text`, so that `text[start:end] == evidence`.

The sample uses two types of annotated skills:

- **Required skills (+1)**: The posting asks the candidate to perform the skill. Required skills are usually described in everyday language rather than with the wording of the ESCO label. For example, *"Pull apart the balance sheet of each client before the first client meeting"* is annotated with *interpret financial statements*.
- **Decoy skills (−1)**: The posting evokes the skill, but the role does not require it. Decoys usually come from parts of the posting other than the duties, such as benefits, perks, facilities, tools offered by the company or the hiring process. For example:
    - *"Quarterly team-building lunch and an annual company retreat, paid by us"* evokes *encourage teambuilding*.
    - *"Interviews are a call with our editor, then a paid test post"* evokes *recruit employees*.
    - *"Access to our Schoology platform for online training courses"* evokes *Schoology*.

  A system that ranks decoy skills highly is penalised.

All ESCO skills that are not listed for a posting are considered neutral (0). The sample is a simplified version of the task: it uses a single grade for required skills instead of graded relevance levels.

Example of an entry (text truncated):

```json
{
  "id": 1,
  "text": "Business Analyst, Calgary\n\n... Pull apart the balance sheet of each client before the first client meeting. ...",
  "annotations": [
    {
      "skill": "interpret financial statements",
      "label": 1,
      "evidence": "Pull apart the balance sheet of each client before the first client meeting.",
      "start": 194,
      "end": 270
    },
    {
      "skill": "encourage teambuilding",
      "label": -1,
      "evidence": "Quarterly team-building lunch and an annual company retreat, paid by us.",
      "start": 420,
      "end": 492
    }
  ]
}
```

</details>

{{< alert color="info" >}}The sample set is intended only to illustrate the data. The format of the training, development and test sets may differ slightly. Any change will be documented on this website.{{< /alert >}}
