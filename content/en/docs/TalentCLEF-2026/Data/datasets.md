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
    <a href="https://doi.org/10.5281/zenodo.17625261" class="download-button" target="_blank">Access the Zenodo download page</a>
    <br> 
</body>

<br>  
 
The dataset structure on Zenodo is organized into two `*.zip` files, TaskA.zip and TaskB.zip, each containing folders to support different stages of model development. So far, only the development set of Task A and the training set of Task A have been released, but in future releases, as the tasks progress, additional data will be added to the different subfolders for each task.

**TaskA** includes language-specific subfolders within the directories, covering English and Spanish data. Development folders include two essential folders (queries, corpus), and a qrels file for evaluating model relevance to search queries.

<body>
    <ul>
    <li class="line">
<li class="line">
            <span class="compressed-folder">🗜️️</span> TaskA
            <ul class="subfolder">
                <!-- Task A folder -->
                <li class="line">
                    <ul class="subfolder">
                        <!-- Task A / Development -->
                        <li class="line">
                            <span class="folder">📁</span> development
                            <ul class="subfolder">
                                <li class="line"><span class="folder">📁</span> english
                                    <ul class="subfolder">
                                        <li class="line"><span class="folder">📁</span> queries
                                            <ul class="subfolder">
                                                <li><span class="file">📄</span> 1234</li>
                                                <li>...</li>
                                            </ul>
                                        </li>
                                        <li class="line"><span class="folder">📁</span> corpus
                                            <ul class="subfolder">
                                                <li><span class="file">📄</span> 1</li>
                                                <li>...</li>
                                            </ul>
                                        </li>
                                        <li><span class="file">📄</span> qrels.tsv</li>
                                    </ul>
                                </li>
                                <li class="line"><span class="folder">📁</span> spanish
                                    <ul class="subfolder">
                                        <li class="line"><span class="folder">📁</span> queries
                                            <ul class="subfolder">
                                                <li><span class="file">📄</span> 9865</li>
                                                <li>...</li>
                                            </ul>
                                        </li>
                                        <li class="line"><span class="folder">📁</span> corpus
                                            <ul class="subfolder">
                                                <li><span class="file">📄</span> 2</li>
                                                <li>...</li>
                                            </ul>
                                        </li>
                                        <li><span class="file">📄</span> qrels.tsv</li>
                                    </ul>
                                </li>
                            </ul>
                        </li>
                        <!-- Task A / Test -->
                        <li class="line">
                            <span class="folder">📁</span> test
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
                                <li><span class="file">📄</span> job2skill.tsv</li>
                                <li><span class="file">📄</span> jobid2terms.json</li>
                                <li><span class="file">📄</span> skillid2terms.json</li>
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
                        </li>
                    </ul>
                </li>
            </ul>
        </li>
    </ul>
</body>