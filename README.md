# Developing and assessing named entity recognition models using the MultiNERD dataset

**Author**: [Mahbub Ul Alam](https://www.linkedin.com/in/anondo),
 Email: mahbub.ul.alam.anondo@gmail.com

## Overview
This repository documents the training and evaluation of named entity recognition (NER) models using the English subset of the MultiNERD dataset. The dataset includes 10 languages and 15 NER categories, with a focus on Wikipedia and WikiNews texts. The project centers around fine-tuning the "bert-base-multilingual-cased" BERT-based language model with the English portion of the MultiNERD dataset.

## System Implementation
### System A
- **Dataset**: Uses the English subset of the MultiNERD dataset.
- **Framework**: Training conducted with the SpanMarker Python framework, which processes sentences through a pretrained encoder (such as BERT or RoBERTa) and fine-tunes it using cross-entropy loss. The model employs special tokens to indicate the start and end of a span in the input sentence.

### System B
- **Dataset**: Mirrors System A, focusing on five entity types: PERSON, ORGANIZATION, LOCATION, DISEASES, ANIMAL.
- **Framework**: Adopts the same SpanMarker Python framework as System A.
- **Adjustments**: Excludes other entity types and alters label IDs for consistency.

## Evaluation and Analysis
- **Tools**: Utilizes seqeval and nervaluate frameworks for evaluation.
- **Approach**: Conducts a thorough evaluation using various metrics, including F1, Recall, Precision, and detailed error categorization.
- **Findings**: The results demonstrate satisfactory performance, with insights into the impact of entity type quantity and the comparison between cased and uncased models.

## Limitations and Future Work
- **Current Limitations**: Restricted computational resources limited in-depth hyper-parameter tuning and exploration of diverse transformer models.
- **Future Directions**: Aims to overcome these challenges and focus on the real-world applicability and efficacy of models. Future evaluations will employ methodologies from "Interpretable Multi-dataset Evaluation for Named Entity Recognition" ([Read the paper](https://aclanthology.org/2020.emnlp-main.489.pdf)) and its [GitHub Repository](https://github.com/neulab/InterpretEval).

## Additional Experiments
- **Uncased Model Trials**: Conducted experiments with 'bert-base-multilingual-uncased' model, yielding results that highlight the need for more extensive hyperparameter tuning.

## Repository Contents
- **Models and Results**: All trained models and their results are accessible at [GitHub Repository - neulab/InterpretEval](https://github.com/neulab/InterpretEval).
- **IPython Notebook**: Includes a well-commented and descriptive IPython notebook for detailed understanding and replication of the experiments.

## User Guide
- **Setup**: Refer to `requirements.txt` for environment setup.
- **Dataset Preparation**: Assumes the MultiNERD dataset has been pre-downloaded. Instructions for downloading and using git-lfs are included in the IPython Notebook.
- **Google Colab Information**: For users on Google Colab with an A100 GPU, Google Drive access is required to save information.

This repository is open for contributions, suggestions, and discussions to enhance the models and evaluation methods. For a comprehensive understanding of the methodologies, results, and future plans, please explore the IPython Notebook.
