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
| [deepmind\narrativeQA](https://github.com/deepmind/narrativeqa)      | NarrativeQA 是一个包含故事(影视剧剧本)和相应问题的英语数据集，旨在测试阅读理解能力，尤其是长文档的阅读理解能力。回答问题依靠summary（人类标注）或者story（原文）<br>一个文本对应一个问题       |A typical data point consists of a question and answer pair along with a summary/story which can be used to answer the question. Additional information such as the url, word count, wikipedia page, are also provided.|<br>training(32747,saved in 24 parquet files),<br>valiudation(3461,saved in 3 parquet files),<br>test(10557,saved in 8 parquet files)  <br>based on story (i.e. the same story cannot appear in more than one split)|
|[UltraDomain](https://github.com/qhjqhj00/MemoRAG)      |包含多个领域的数据集，如finance,cs,legal,cooking(all:20 classes)。每个数据集存储在一个jsonl文件中.<br>存在一个文本(context)对应多个不同问题，即一篇文章可以出现在多个example中  |  'input'(question);'context';'dataset';'label';'answers';'_id';'length'  | All train set(total:3933). Example:<br>agriculture(100),art(200).(All information can be seen in READ_UltraDomain.ipynb).<br>Max size:438(legal),<br>Min size:100(cs)  |
|[qasper](https://hf-mirror.com/datasets/allenai/qasper)|  QASPER 是一个用于科学研究论文问答的数据集。它由 1,585 篇自然语言处理论文中的 5,049 个问题组成。每个问题均由 NLP 从业者撰写，他仅阅读相应论文的标题和摘要，并且该问题寻求全文中存在的信息。然后由一组单独的 NLP 从业者回答这些问题，他们还提供答案的支持证据  |
