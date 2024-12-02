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
