---
title: Codabench
date: 2026-01-05
categories: [Examples]
weight: 4
type: docs  
---
<style>
.full-width-image {
            width: 80%;
            height: auto; /* Maintains the aspect ratio */
        }
</style>

The evaluation will take place on [Codabench](https://www.codabench.org/), where participants must upload their predictions according to the [submission format](/docs/talentclef-2026/evaluation/submission_format/). The official competition links will be shared soon through this platform and online communication channels.

<img src="https://miro.medium.com/v2/resize:fit:1400/1*cIZRfXOzzSobTkTV4i6gVA.png" alt="Codabench" class="full-width-image">

#### Task A - Codabench rules 

- For Task A, predictions for each language pair must be generated in separate run files. These files should be compressed into a ZIP file, ensuring that the files are placed directly inside the root of the archive (without any folders), and then uploaded to Codabench.
- During the development phase, participants can submit as many files as they wish in the platform. 
- During the **test phase**, a maximum of **5 submissions** can be uploaded. Each submission is required to contain at least the results for `en-en` and `es-es`; otherwise, an evaluation error will appear. We also suggest including cross-lingual predictions (`en-es`).

**Uploading rules**:

- **File Naming Rules**: Run files must follow the naming convention `run_xx-xx_teamname.trec`, where xx-xx represents the directionality of the queries and corpus elements.
- **ZIP Compression**: The Run files should be compressed into a flat ZIP file (i.e., the files must be placed directly inside the ZIP, without folders).


#### Task B - Codabench rules

- During the development phase, participants can submit as many files as they wish in the platform. 
- During the **test phase**, a maximum of **3 submissions** can be uploaded. 


For local testing, an evaluation script is available in our GitHub repository. You can access it here: [Evaluation Script](https://github.com/TalentCLEF/talentclef26_evaluation_script). You can find a tutorial on the process of generating submission files and evaluating them in the Tutorials section of the [*Additional resources page*](/docs/talentclef-2026/data/additional_resources/#3-tutorials)

