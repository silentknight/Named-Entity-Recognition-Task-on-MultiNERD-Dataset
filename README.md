# Assignment: Research Engineer in Natural Language Processing
## RISE Research Institutes of Sweden

Fine-tune a Transformer-based Large Language Model (LLM) found on HuggingFace Model Hub on the English subset of the training set of the MultiNERD Named Entity Recognition dataset.

### Installing Dependencies
Use the command below to install the packages according to the configuration file requirements.txt.
```
$ pip install -r requirements.txt
```

### Running the Task
Utilize this command to execute both experiments A (with the complete tagset) and B (with a reduced tagset) using the script.
```
$ ./run_script
```
Execute the experiment individually by running the following command and replacing the command line argument with either "A" or "B".
```
$ python main --exp A
```

### Training Details
In this specific scenario, three pre-trained Language Models (LLMs) were employed - BERT, DistilBERT, and XLNet.

The model parameters are:
```
batch_size = 8
learning_rate = 1e-4
num_train_epochs = 5
weight_decay = 0.00001
```

### Results
The results are listed in '.jsonl' files.

## Resources:
- HuggingFace Model Hub: https://huggingface.co/models
- MultiNERD Named Entity Recognition dataset: https://huggingface.co/datasets/Babelscape/multinerd?row=17
- MultiNERD: A Multilingual, Multi-Genre and Fine-Grained Dataset for Named Entity Recognition (and Disambiguation): https://aclanthology.org/2022.findings-naacl.60.pdf
