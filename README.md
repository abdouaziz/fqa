# French Question Answering 
 
<p align="center">
<img src="./input/QAA.png">
</p>


## Description

**Question answering** (QA) is the fields of information retrieval in natural language processing (NLP), which is concerned with to build a  systems that automatically answer a questions about the content of a giving corpus . 


## Objective

the objects in the project is to buid an QA System based on French language , the dataset used from :

*[FQuAD](https://fquad.illuin.tech/)

*[PIAF - Le dataset francophone de Questions-Réponses PIAF - Q&A](https://www.data.gouv.fr/fr/datasets/piaf-le-dataset-francophone-de-questions-reponses/)


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 

### Prerequisites

 
install the dependencies for this project by running the following commands in your terminal:

```
 pip install -r requirements.txt
```

run the seq2seq model by running the following command in your terminal:

```
python src/seq2seq.py --train_file="./input/wolof.csv" \
                        --max_source_length=150 \
                        --max_target_length=150 \
                        --number_epochs=4 \
                        --learning_rate=3e-8 \
                        --epsilone=1e-9 \
                        --train_batch_size=3 \
                        --model_name="bert-base-cased"
```

run the t5 model by running the following command in your terminal:

```
python src/t5.py --train_file="./input/wolof.csv" \
                        --max_source_length=150 \
                        --max_target_length=150 \
                        --number_epochs=4 \
                        --learning_rate=3e-8 \
                        --epsilone=1e-9 \
                        --train_batch_size=3 \
                        --model_name="t5-small" \
                        --task_prefix="translation French to Wolof: "
```






 

 










