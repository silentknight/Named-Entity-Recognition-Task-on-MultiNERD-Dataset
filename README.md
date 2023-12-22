# Assignment: Research Engineer in Natural Language Processing
## RISE Research Institutes of Sweden

Fine-tune a Transformer-based Large Language Model (LLM) found on HuggingFace Model Hub on the English subset of the training set of the MultiNERD Named Entity Recognition dataset.

### Installing Dependencies
You can use the command below to install the packages according to the configuration file requirements.txt.
```
$ pip install -r requirements.txt
```

### Fine-tuning the Model
Using the script, utilize this command to execute experiments A (with the complete tagset) and B (with a reduced tagset).
```
$ ./run_script
```
Execute the experiment individually by running the following command and replacing the command line argument with either "A" or "B".
```
$ python main --exp A
```

### Pre-trained Models
In this specific scenario, three pre-trained cased Language Models (LLMs) were employed - BERT, DistilBERT, and XLNet. The choice of cased models for an NER task was obvious as NER tokens are influenced by the case of the text.

| # | Pre-Trained Model  | Model Description |
| - | ------------- | ------------- |
| 1. | bert-base-cased | 12-layer, 768-hidden, 12-heads, 110M parameters. Trained on cased English text. |
| 2. | xlnet-base-cased | 12-layer, 768-hidden, 12-heads, 110M parameters. XLNet English model. |
| 3. | distilbert-base-cased | 6-layer, 768-hidden, 12-heads, 65M parameters. Distilled from the bert-base-cased model. |

### Model Hyper-parameters
```
batch_size = 8
learning_rate = 1e-4
num_train_epochs = 5
weight_decay = 0.00001
```

### Results
The results are listed in '.jsonl' files.

### Report of the Task
Please find the report in the repository at: https://github.com/silentknight/RISE-MultiNERD-Task/blob/master/Report.pdf

## Resources:
- HuggingFace Model Hub: https://huggingface.co/models
- MultiNERD Named Entity Recognition dataset: https://huggingface.co/datasets/Babelscape/multinerd?row=17
- MultiNERD: A Multilingual, Multi-Genre and Fine-Grained Dataset for Named Entity Recognition (and Disambiguation): https://aclanthology.org/2022.findings-naacl.60.pdf
