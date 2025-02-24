---
title: Codabench
date: 2017-01-05
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

The evaluation will take place on [Codabench](https://www.codabench.org/), where participants must upload their predictions according to the [submission format](/docs/talentclef-2025/evaluation/submission_format/). The official competition links will be shared soon through this platform and online communication channels.

<img src="https://miro.medium.com/v2/resize:fit:1400/1*cIZRfXOzzSobTkTV4i6gVA.png" alt="Codabench" class="full-width-image">

#### Task A - Codabench rules 

- For Task A, predictions for each language pair must be generated in separate .trec files. These files should be compressed into a ZIP file, ensuring that the files are placed directly inside the archive (without any folders), and then uploaded to Codabench.
- During the development phase, participants can submit as many files as they wish in the platform. 
- During the **test phase**, a maximum of **6 submissions** can be uploaded. Each submission is required to contain at least the results for `en-en`, `es-es` and `de-de`; otherwise, an evaluation error will appear. We also suggest including cross-lingual predictions (`en-es`, `en-de`), as well as the Chinese results (`zh-zh`, `en-zh`).

**Uploading rules**:

- **File Naming Rules**: TREC files must follow the naming convention `run_xx-xx_teamname.trec`, where xx-xx represents the directionality of the queries and corpus elements.
- **ZIP Compression**: The `.trec` files should be compressed into a flat ZIP file (i.e., the .trec files must be placed directly inside the ZIP, without folders).


#### Task B - Codabench rules

- During the development phase, participants can submit as many files as they wish in the platform. 
- During the **test phase**, a maximum of **3 submissions** can be uploaded. 


For local testing, an evaluation script is available in our GitHub repository. You can access it here: [Evaluation Script](https://github.com/TalentCLEF/talentclef25_evaluation_script). You can find a tutorial on the process of generating submission files and evaluating them in the Tutorials section of the [*Additional resources page*](https://talentclef.github.io/talentclef/docs/talentclef-2025/data/additional_resources/#3-tutorials)



### Codabench Tutorial
To Be Published