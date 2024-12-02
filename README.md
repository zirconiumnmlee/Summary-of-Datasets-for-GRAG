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
| Name      | Description | Structure | Data Splits |Data Instance |
| ----------- | ----------- | ----------|---|---|
| [deepmind\narrativeQA](https://github.com/deepmind/narrativeqa)      | NarrativeQA 是一个包含故事和相应问题的英语数据集，旨在测试阅读理解能力，尤其是长文档的阅读理解能力。       |A typical data point consists of a question and answer pair along with a summary/story which can be used to answer the question. Additional information such as the url, word count, wikipedia page, are also provided.|training(32747), valiudation(3461),  test(10557)  based on story (i.e. the same story cannot appear in more than one split)|{
    "document": {
        "id": "23jncj2n3534563110",
        "kind": "movie",
        "url": "https://www.imsdb.com/Movie%20Scripts/Name%20of%20Movie.html",
        "file_size": 80473,
        "word_count": 41000,
        "start": "MOVIE screenplay by",
        "end": ". THE END",
        "summary": {
            "text": "Joe Bloggs begins his journey exploring...",
            "tokens": ["Joe", "Bloggs", "begins", "his", "journey", "exploring",...],
            "url": "http://en.wikipedia.org/wiki/Name_of_Movie",
            "title": "Name of Movie (film)"
        },
        "text": "MOVIE screenplay by John Doe\nSCENE 1..."
    },
    "question": {
        "text": "Where does Joe Bloggs live?",
        "tokens": ["Where", "does", "Joe", "Bloggs", "live", "?"],
    },
    "answers": [
        {"text": "At home", "tokens": ["At", "home"]},
        {"text": "His house", "tokens": ["His", "house"]}
    ]
}|
