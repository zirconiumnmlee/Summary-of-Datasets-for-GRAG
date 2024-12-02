<center><h2>📢Summary of Datasets for GRAG</h2></center>
This is a repository to summarize the datasets used in several papers,which may include how to install the datasets,how to read them with python and something else. It will help us become familiar with the structure of relevant data sets for further scientific research.

## How to install datasets from Huggingface

- Install the dependencies and devDependencies and start the server.

```
pip install -U huggingface_hub
```

- Download dataset you need

```
huggingface-cli download --repo-type dataset <name>
```

You may need to open [huggingface](https://huggingface.co/) to get the full name of your dataset
(If cannot enter,try [huggingface mirror](https://hf-mirror.com/))

## Summary of Datasets
| Name      | Description | Structure | Data Splits |
| ----------- | ----------- | ----------|---|
| [deepmind\narrativeQA](https://github.com/deepmind/narrativeqa)      | NarrativeQA 是一个包含故事(影视剧剧本)和相应问题的英语数据集，旨在测试阅读理解能力，尤其是长文档的阅读理解能力。回答问题依靠summary（人类标注）或者story（原文）       |A typical data point consists of a question and answer pair along with a summary/story which can be used to answer the question. Additional information such as the url, word count, wikipedia page, are also provided.|training(32747,saved in 24 parquet files), valiudation(3461,saved in 3 parquet files),  test(10557,saved in 8 parquet files)  based on story (i.e. the same story cannot appear in more than one split)|
