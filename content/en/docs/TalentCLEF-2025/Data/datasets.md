---
title: Datasets
date: 2017-01-05
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
        .excel-file {
            margin-right: 5px;
            color: #1f73b7;
        }
        .subfolder {
            margin-left: 20px;
        }
        .button-container {
            display: flex;
            justify-content: center;
            margin-top: 20px;
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

{{< alert color="warning" >}}We take the legal and ethical implications of using AI in Human Resources very seriously. It is important to note that the data we utilize inherently excludes any personal information, focusing solely on job titles and skills without involving personal/company information or geographic location.{{< /alert >}}

The data will be hosted on the Zenodo platform under the [*NLP in HR*](https://zenodo.org/communities/nlp_hr/records?q=&l=list&p=1&s=10) community, following the file structure outlined below. Each time new data is added, an updated version of the dataset will be published on the platform. 
 <br> 
<body>
    <a href="https://doi.org/10.5281/zenodo.14002665" class="download-button" target="_blank">Access the Zenodo download page</a>
    <br> 
</body>

<br>  
 
The dataset structure on Zenodo is organized into two `*.zip` files, TaskA and TaskB, each containing training, validation and test folders to suuport different stages of model development. Until the official release of the full training set, users can access a sample version of the data through the `sampleset_TaskA.zip` and `sampleset_TaskB.zip` files.

**TaskA** includes language-specific subfolders within the training and validation directories, covering English, Spanish, German, and Chinese job title data. The tr*aining folders for TaskA contain language-specific .tsv files for each respective language. Validation folders include three essential files—queries, corpus_elements, and q_rels—for evaluating model relevance to search queries. TaskA’s test folder has queries and corpus_elements files for testing retrieval. 

<body>
    <ul>
    <li class="line">
<li class="line">
            <span class="compressed-folder">🗜️️</span> TaskA
            <ul class="subfolder">
                <!-- Task A folder -->
                <li class="line">
                    <ul class="subfolder">
                        <!-- Task A / Training -->
                        <li class="line">
                            <span class="folder">📁</span> training
                            <ul class="subfolder">
                                <li class="line"><span class="folder">📁</span> english
                                    <ul class="subfolder">
                                        <li><span class="file">📄</span> taskA_training_en.tsv</li>
                                    </ul>
                                </li>
                                <li class="line"><span class="folder">📁</span> spanish
                                    <ul class="subfolder">
                                        <li><span class="file">📄</span> taskA_training_es.tsv</li>
                                    </ul>
                                </li>
                                <li class="line"><span class="folder">📁</span> german
                                    <ul class="subfolder">
                                        <li><span class="file">📄</span> taskA_training_de.tsv</li>
                                    </ul>
                                </li>
                            </ul>
                        </li>
                        <!-- Task A / Validation -->
                        <li class="line">
                            <span class="folder">📁</span> validation
                            <ul class="subfolder">
                                <li class="line"><span class="folder">📁</span> english
                                    <ul class="subfolder">
                                        <li><span class="file">📄</span> queries</li>
                                        <li><span class="file">📄</span> corpus_elements</li>
                                        <li><span class="file">📄</span> q_rels</li>
                                    </ul>
                                </li>
                                <li class="line"><span class="folder">📁</span> spanish
                                </li>
                                <li class="line"><span class="folder">📁</span> german
                                </li>
                                <li class="line"><span class="folder">📁</span> chinese
                                </li>
                            </ul>
                        </li>
                        <!-- Task A / Test -->
                        <li class="line">
                            <span class="folder">📁</span> test
                            <ul class="subfolder">
                                <li><span class="file">📄</span> queries</li>
                                <li><span class="file">📄</span> corpus_elements</li>
                            </ul>
                        </li>
                    </ul>
                </li>
    </li>
</body>

 <br> 

**TaskB** follows a similar structure but without language-specific subfolders, providing general .tsv files for training, validation, and testing. This consistent file organization enables efficient data access and structured updates as new data versions are published.




<body>
    <ul>
        <!-- Root folder -->
                <!-- Task B folder -->
                <li class="line">
                <span class="compressed-folder">🗜️️</span> TaskB
                    <ul class="subfolder">
                        <!-- Task B / Training -->
                        <li class="line">
                            <span class="folder">📁</span> training
                            <ul class="subfolder">
                                <li><span class="file">📄</span> taskB_training.tsv</li>
                            </ul>
                        </li>
                        <!-- Task B / Validation -->
                        <li class="line">
                            <span class="folder">📁</span> validation
                            <ul class="subfolder">
                                <li><span class="file">📄</span> queries</li>
                                <li><span class="file">📄</span> corpus_elements</li>
                                <li><span class="file">📄</span> q_rels</li>
                            </ul>
                        </li>
                        <!-- Task B / Test -->
                        <li class="line">
                            <span class="folder">📁</span> test
                            <ul class="subfolder">
                                <li><span class="file">📄</span> queries</li>
                                <li><span class="file">📄</span> corpus_elements</li>
                            </ul>
                        </li>
                    </ul>
                </li>
            </ul>
        </li>
    </ul>
</body>
