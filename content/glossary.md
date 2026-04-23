---
title: Glossary
layout: default
nav_order: 10
has_toc: T
---
# Glossary 
<p>This page is a quick reference for terms used in these workshops: LLMs, Cursor, and Python for data analysis.</p> 

| Term | Definition |
|------|------------|
|Bias|A systematic error in the LLM. This is brought into the LLM during the training phase.|
|Comma-separated values (CSV)|A plain-text table format (often <code>.csv</code>). The Palmer Penguins dataset in this series is a CSV you load with pandas.|
|Context window|The amount of text (tokens) an LLM can consider at once, including your current prompt and previous messages.|
|Dataframe|Data structure constructed with rows and columns that can contain many different types of data (numbers and characters).|
|Data type|The kind of data in your dataset. For example, numbers are numeric data and letters are character data.|
|Data structures|Shapes/formats the entire dataset is saved as. These could be a dataframe, a matrix, a list, a vector to name a few. Statistical analyses and graph generation require data in a specific format.|
|Drop missing values (<code>dropna</code>)|A pandas method that removes rows (or columns) containing missing values.|
|Dummy data|A fake dataset that has the same data types and structure as your real data. These datasets are used to make sure code works and work around data privacy and ownership concerns of using real data.|
|Exploratory Data Analysis (EDA)|Early-stage analysis used to understand data shape, quality, patterns, and possible relationships before formal modeling.|
|Hallucinations|Mistakes made by the LLM. Factually incorrect answers.|
|Histogram|A chart showing the distribution of a numeric variable by binning values into ranges.|
|Integrated development environment (IDE)|Software for writing and running code in one place (e.g. Cursor).|
|Jupyter notebook (<code>.ipynb</code>)|An interactive document that combines code, output, plots, and notes in one file.|
|Kernel|The Python runtime used by a notebook to execute code cells. Choosing the right kernel ensures your packages are available.|
|Large Language Model (LLM)|A large computer model that outputs text (language) based on past experiences (training data).|
|Prompt|Text input you give the LLM.|
|Prompt engineering|The practice of designing and refining prompts so the model returns useful, accurate results.|
|Summary statistics|Numeric summaries such as count, mean, min, and max used to quickly describe a dataset.|
|Token|The small units of text an LLM reads and writes. Longer chats use more tokens; models also have a context limit.|
|Training Data|Data used to make the LLM. This is what ChatGPT crawls the web for.|
|Testing Data|Data that is used to test the accuracy of the LLM.|
|Virtual environment (venv)|An isolated Python environment for a project so dependencies do not conflict with other projects.|

<p>There is also a <a href="https://www.vectara.com/glossary-of-llm-terms" target="_blank">list of terms here</a>. This page goes a bit more in detail for each term than the glossary in this workshop.</p>
