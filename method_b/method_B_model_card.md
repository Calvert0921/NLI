---
{}
---
language: en
license: cc-by-4.0
tags:
- text-classification
repo: https://github.com/Calvert0921/NLI

---

# Model Card for m42677js-j95271zf-track_NLI

<!-- Provide a quick summary of what the model is/does. -->

This is a classification model that was trained to
      determine if the hypothesis is true based on the premise.


## Model Details

### Model Description

<!-- Provide a longer summary of what this model is. -->

This is a HBMP model that employs hierarchical layers of Bi-directional Long Short-Term Memory (BiLSTM) networks combined with max pooling.

- **Developed by:** Jia Tong See and Zhizhou Fang
- **Language(s):** English
- **Model type:** Supervised
- **Model architecture:** BiLSTM
- **Finetuned from model [optional]:** N/A

### Model Resources

<!-- Provide links where applicable. -->

- **Repository:** https://github.com/Helsinki-NLP/HBMP
- **Paper or documentation:** https://www.cambridge.org/core/journals/natural-language-engineering/article/sentence-embeddings-in-nli-with-iterative-refinement-encoders/AC811644D52446E414333B20FEACE00F

## Training Details

### Training Data

<!-- This is a short stub of information on the training data that was used, and documentation related to data pre-processing or additional filtering (if applicable). -->

26K premise-hypothesis pairs

### Training Procedure

<!-- This relates heavily to the Technical Specifications. Content here should link to that section when it is relevant to the training procedure. -->

#### Training Hyperparameters

<!-- This is a summary of the values of hyperparameters used in training the model. -->


      - dropout: 0.5
      - optimizer: 'adam'
      - lr_reduction_factor: 0.2
      - learning_rate: 5e-04
      - train_batch_size: 32
      - eval_batch_size: 32
      - num_epochs: 20

#### Speeds, Sizes, Times

<!-- This section provides information about how roughly how long it takes to train the model and the size of the resulting model. -->


      - overall training time: 4m54s
      - duration per training epoch: 1m
      - model size: 125MB

## Evaluation

<!-- This section describes the evaluation protocols and provides the results. -->

### Testing Data & Metrics

#### Testing Data

<!-- This should describe any evaluation data used (e.g., the development/validation set provided). -->

A subset of the development set provided, amounting to 6K pairs.

#### Metrics

<!-- These are the evaluation metrics being used. -->


      - Precision
      - Recall
      - F1-score
      - Accuracy

### Results

The model obtained an F1-score of 72.02% and an accuracy of 72.17%.

## Technical Specifications

### Hardware


      - RAM: at least 16 GB
      - Storage: at least 2GB,
      - GPU: RTX3060

### Software


      - spacy
      - torchtext 0.6.0
      - Pytorch 2.2.2+cu118

## Bias, Risks, and Limitations

<!-- This section is meant to convey both technical and sociotechnical limitations. -->

N/A

## Additional Information

<!-- Any other information that would be useful for other people to know. -->

The hyperparameters were determined by experimentation
      with different values.
