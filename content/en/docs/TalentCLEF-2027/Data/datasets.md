---
title: Datasets
date: 2026-09-18
categories: [Examples]
weight: 2
tags: [test, sample, docs]
---
<head>
    <style>
        /* Basic styling for better presentation */
        ul {
            list-style-type: none;
            padding: 0;
            margin: 0;
        }
        li {
            margin-bottom: 5px;
        }
        /* Style folder and file icons */
        .folder {
            margin-right: 5px;
            color: #007BFF;
        }
        .file {
            margin-right: 5px;
            color: #6C757D;
        }
        .compressed-folder {
            margin-right: 5px;
            color: #28a745;
        }
        .subfolder {
            margin-left: 20px;
        }
        .download-button {
            background-color: #007BFF;
            color: white;
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            text-decoration: none;
        }
        .download-button:hover {
            background-color: #0056b3;
        }
    </style>
</head>

{{< alert color="warning" >}}We take the legal and ethical implications of using AI in Human Resources very seriously. The data we use inherently excludes any personal information. When context is provided, it is generated using generative Large Language Models, so all the information is produced without involving personal/company information or geographic location.{{< /alert >}}

The data will be hosted on the Zenodo platform under the [*NLP in HR*](https://zenodo.org/communities/nlp_hr/records?q=&l=list&p=1&s=10) community, created as a central hub for resources in this domain. Each time new data is added, an updated version of the dataset will be published on the platform.
 <br> 
<body>
    <a href="https://doi.org/10.5281/zenodo.24461181" class="download-button" target="_blank">Access the Zenodo download page</a>
    <br> 
</body>

<br>  

Once the tasks are finished, the datasets will also be made available on HuggingFace, facilitating access for ML practitioners worldwide.

To ensure transparency and reproducibility, the competitions will again be launched on [Codabench](https://www.codabench.org/), with access restricted to participants officially registered in CLEF during the campaign, and reopened as a public benchmark afterwards. Evaluation scripts, tutorials and support materials will be provided through both this website and the project's [GitHub repository](https://github.com/TalentCLEF).

## File structure

The data on Zenodo is organized into two `*.zip` files, one per task. As new data is released, according to the <a  href='{{< relref "docs/talentclef-2027/schedule/" >}}'>official schedule</a>, a new version of the record will be published with the corresponding folders. Until the official release of the training and development data, users can access a sample version of the data through the `sample_Task1.zip` and `sample_Task2.zip` files.

This sample dataset provides an example of the data format and structure that will be used in the tasks, serving as a preview of the full dataset to be released. A detailed description of each file is available in the <a  href='{{< relref "docs/talentclef-2027/data/description_corpus" >}}'>Description of the Corpus</a> page.

**Task 1** includes a language-specific subfolder for English (`en`), Spanish (`es`) and French (`fr`). Each language subfolder contains two folders, `queries` (job offers) and `corpus_elements` (candidate résumés), and a `qrels.tsv` file that links queries to corpus elements and is used to evaluate model relevance.

<body>
    <ul>
        <li class="line">
            <span class="compressed-folder">🗜️️</span> Task 1
            <ul class="subfolder">
                <li class="line"><span class="folder">📁</span> en
                    <ul class="subfolder">
                        <li class="line"><span class="folder">📁</span> queries
                            <ul class="subfolder">
                                <li><span class="file">📄</span> sample_qa_1.txt</li>
                            </ul>
                        </li>
                        <li class="line"><span class="folder">📁</span> corpus_elements
                            <ul class="subfolder">
                                <li><span class="file">📄</span> sample_ca_1.txt</li>
                            </ul>
                        </li>
                        <li><span class="file">📄</span> qrels.tsv</li>
                    </ul>
                </li>
                <li class="line"><span class="folder">📁</span> es
                    <ul class="subfolder">
                        <li>...</li>
                    </ul>
                </li>
                <li class="line"><span class="folder">📁</span> fr
                    <ul class="subfolder">
                        <li>...</li>
                    </ul>
                </li>
            </ul>
        </li>
    </ul>
</body>

 <br> 

**Task 2** provides one JSON file per set: the training, development and test sets will each be released as their own JSON file. In the sample set, `task2_sample.json` contains 5 synthetic job postings in English, each one with the list of ESCO skills annotated with their polarity in the text.

<body>
    <ul>
        <li class="line">
            <span class="compressed-folder">🗜️️</span> Task 2
            <ul class="subfolder">
                <li><span class="file">📄</span> task2_sample.json</li>
            </ul>
        </li>
    </ul>
</body>

 <br> 

{{< alert color="info" >}}The sample set is intended only to illustrate the data. The format of the training, development and test sets may differ slightly. Any change will be documented on this website.{{< /alert >}}
