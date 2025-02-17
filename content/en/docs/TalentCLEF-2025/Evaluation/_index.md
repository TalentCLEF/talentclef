---
title: "Evaluation"
weight: 5
type: docs  
resources:
  - src: "codalab.png"  
---

<style>
.full-width-image {
            width: 80%;
            height: auto; /* Maintains the aspect ratio */
        }
</style>

The evaluation will be done at CodaBench. TalentCLEF-2025 submissions will be ranked by Mean Average Precision.

### Evaluation dates
21st April - 5th May 2025

### Submission format
Submissions must adhere to the TREC Run File Format, including column names, with exactly six space-separated columns per line, structured as follows:

```
<q_id> Q0 <doc_id> <rank> <score> <run_tag>
```

**Column Descriptions**

- `<q_id>`: The identifier for the query corresponding to the job title being searched.
- `Q0`: A constant placeholder (always set to "Q0").
- `<doc_id>`: The identifier for the retrieved corpus element.
- `<rank>`: The ranking position of the retrieved document for the query (starting at 1).
- `<score>`: The retrieval score assigned to the document (higher scores indicate greater relevance).
- `<run_tag>`: A label identifying the submitted run (e.g., `teamA_systemA`).

^
**Example** 
The submissions must contains the column headers:

```
q_id Q0 doc_id rank score tag
query1 Q0 ce1 1 0.6910377144813538 teamA_systemA
query1 Q0 ce4 2 0.6690284013748169 teamA_systemA
query1 Q0 ce5 3 0.662328839302063 teamA_systemA
```

## Codabench

For Task A, predictions for each language pair must be generated in separate .trec files. These files should be compressed into a ZIP file, ensuring that the files are placed directly inside the archive (without any folders), and then uploaded to Codabench.

During the **development phase**, participants can submit as many files as they wish. However, in the **test phase**, submission limits apply:
  - **Task A**: A maximum of 6 submissions per queries-corpus combination (i.e., up to 6 prediction files per evaluation scenario).
  - **Task B**: A maximum of 3 submissions

The Codabench competition links will be shared soon, and participants will be notified both here and through online communication channels.

For local testing, an evaluation script is available in our GitHub repository. You can access it here: [Evaluation Script](https://github.com/TalentCLEF/talentclef25_evaluation_script). You can find a tutorial on the process of generating submission files and evaluating them in the Tutorials section of the [*Additional resources page*](https://talentclef.github.io/talentclef/docs/talentclef-2025/data/additional_resources/#3-tutorials)


