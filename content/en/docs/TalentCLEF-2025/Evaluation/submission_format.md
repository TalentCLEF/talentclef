---
title: Submission format
date: 2017-01-05
categories: [Examples]
weight: 3
tags: [test, sample, docs]
---


{{< alert color="warning" >}}<i class="fas fa-exclamation-triangle"></i> You can find a tutorial on the process of generating submission files and evaluating them in the Tutorials section of the [*Additional resources page*](https://talentclef.github.io/talentclef/docs/talentclef-2025/data/additional_resources/#3-tutorials)
{{< /alert >}}


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


**Example** 
The submissions must contains the column headers:

```
q_id Q0 doc_id rank score tag
query1 Q0 ce1 1 0.6910377144813538 teamA_systemA
query1 Q0 ce4 2 0.6690284013748169 teamA_systemA
query1 Q0 ce5 3 0.662328839302063 teamA_systemA
```
