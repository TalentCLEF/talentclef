---
title: Additional resources
date: 2026-09-18
categories: [Examples]
weight: 3
tags: [test, sample, docs]
---


To support your participation in this shared task, we have compiled a list of additional resources that may be useful for understanding the task better, exploring related work, and utilizing domain-specific models.

## 1. Related papers:

- Gasco, L., Fabregat, H., García-Sardiña, L., Estrella, P., Deniz, D., Rodrigo, A., & Zbib, R. (2025, September). Overview of the TalentCLEF 2025: Skill and Job Title Intelligence for Human Capital Management. In International Conference of the Cross-Language Evaluation Forum for European Languages (pp. 464-485). Cham: Springer Nature Switzerland.
- Gasco, L., Fabregat, H., García-Sardiña, L., Estrella, P., Veys, W., Carrino, C. P., De Lange, M., Deniz, D., Rodrigo, A., Decorte, J. J., & Zbib, R. (2026, September). Overview of the TalentCLEF 2026: Skill and Job Title Intelligence for Human Capital Management. In Experimental IR Meets Multilinguality, Multimodality, and Interaction. Lecture Notes in Computer Science, vol. 17087. Cham: Springer Nature Switzerland. Preprint: [arXiv:2606.31692](https://arxiv.org/abs/2606.31692)
- Fabregat, H., García-Sardiña, L., Estrella, P., Gasco, L., Carrino, C. P., Deniz, D., Rodrigo, A., & Zbib, R. (2026). Overview of TalentCLEF 2026: Task A – Contextualized Job–Person Matching. In Working Notes of CLEF 2026 – Conference and Labs of the Evaluation Forum.
- Veys, W., Gasco, L., De Lange, M., & Decorte, J. J. (2026). Overview of TalentCLEF 2026: Task B – Job-Skill Matching with Skill Type Classification. In Working Notes of CLEF 2026 – Conference and Labs of the Evaluation Forum.
- Gasco, L., Fabregat, H., García-Sardiña, L., Deniz, D., Rodrigo, A., Estrella, P., & Zbib, R. (2025, April). TalentCLEF at CLEF2025: Skill and Job Title Intelligence for Human Capital Management. In European Conference on Information Retrieval (pp. 479-486). [Link](https://doi.org/10.1007/978-3-031-88720-8_69)
- Zbib, R., Lacasa, L. A., Retyk, F., Poves, R., Aizpuru, J., Fabregat, H., ... & García-Casademont, E. (2022). Learning Job Titles Similarity from Noisy Skill Labels. arXiv preprint [arXiv:2207.00494](https://arxiv.org/abs/2207.00494)
- Deniz, D., Retyk, F., García-Sardiña, L., Fabregat, H., Gasco, L., & Zbib, R. (2024). Combined Unsupervised and Contrastive Learning for Multilingual Job Recommendation. [Link CEUR](https://ceur-ws.org/Vol-3788/RecSysHR2024-paper_3.pdf)
- Decorte, J. J., Van Hautte, J., Demeester, T., & Develder, C. (2021). Jobbert: Understanding job titles through skills. arXiv preprint [arXiv:2109.09605](https://arxiv.org/abs/2109.09605) 
- Anand, S., Decorte, J. J., & Lowie, N. (2022). Is it required? ranking the skills required for a job-title. arXiv preprint [arXiv:2212.08553](https://arxiv.org/abs/2212.08553)
- Zhang, M., Van Der Goot, R., & Plank, B. (2023). ESCOXLM-R: Multilingual taxonomy-driven pre-training for the job market domain. arXiv preprint [arXiv:2305.12092](https://arxiv.org/abs/2305.12092)
- Bhola, A., Halder, K., Prasad, A., & Kan, M. Y. (2020, December). Retrieving skills from job descriptions: A language model based extreme multi-label classification framework. In Proceedings of the 28th international conference on computational linguistics (pp. 5832-5842). [Link](https://aclanthology.org/2020.coling-main.513/)
- Retyk, F., Gasco, L., Carrino, C. P., Deniz, D., & Zbib, R. (2024). MELO: An Evaluation Benchmark for Multilingual Entity Linking of Occupations. arXiv preprint [arXiv:2410.08319](https://arxiv.org/abs/2410.08319).
- Laosaengpha, N., Tativannarat, T., Rutherford, A., & Chuangsuwanich, E. (2025). Mitigating Language Bias in Cross-Lingual Job Retrieval: A Recruitment Platform Perspective. arXiv preprint [arXiv:2502.03220](https://arxiv.org/abs/2502.03220)
- Laosaengpha, N., Tativannarat, T., Piansaddhayanon, C., Rutherford, A., & Chuangsuwanich, E. (2024). Learning Job Title Representation from Job Description Aggregation Network. arXiv preprint [arXiv:2406.08055](https://arxiv.org/abs/2406.08055)


The per-task overview papers of the 2026 edition and the working notes of the participating teams are listed on the <a href='{{< relref "docs/talentclef-2026/results/" >}}'>TalentCLEF 2026 Results</a> pages.

Task 1.2 (explainability) and Task 2 (skill ranking under negation) draw on lines of work that are new to TalentCLEF. We will complete this list with the relevant references on **LLM-as-a-judge evaluation and explanation faithfulness**, on **negation cue and scope detection** (e.g. NegBERT), and on the **JobSkape** data-generation framework ahead of the start of each task.

## 2. External Resources: 

- [ESCOXLM-R Model](https://huggingface.co/jjzha/esco-xlm-roberta-large) in Huggingface 
- [NESTA Taxonomy](https://github.com/nestauk/skills-taxonomy-v2)
- [ESCO Taxonomy](https://esco.ec.europa.eu/en/use-esco/download)
- **WorkRB** — TechWolf's community-driven evaluation framework for AI in the work domain, to which Task 2 contributes. *(Link to be added.)*
- Datasets from previous TalentCLEF editions, in the [*NLP in HR*](https://zenodo.org/communities/nlp_hr/records?q=&l=list&p=1&s=10) Zenodo community

## 3. Tutorials:

We will publish a series of notebooks covering the fundamentals, including how to work with the data and upload predictions to Codabench. They will be made available in the [talentclef_tutorials](https://github.com/TalentCLEF/talentclef_tutorials) repository once the sample set is released.
