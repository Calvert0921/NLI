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

This is a SVM model paired with sBERT embedding.

- **Developed by:** Jia Tong See and Zhizhou Fang
- **Language(s):** English
- **Model type:** Supervised
- **Model architecture:** SVM
- **Finetuned from model [optional]:** NA

### Model Resources

<!-- Provide links where applicable. -->

- **Repository:** NA
- **Paper or documentation:** https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=708428

## Training Details

### Training Data

<!-- This is a short stub of information on the training data that was used, and documentation related to data pre-processing or additional filtering (if applicable). -->

26K premise-hypothesis pairs

### Training Procedure

<!-- This relates heavily to the Technical Specifications. Content here should link to that section when it is relevant to the training procedure. -->

#### Training Hyperparameters

<!-- This is a summary of the values of hyperparameters used in training the model. -->


      - C: 2
      - kernel: rbf

#### Speeds, Sizes, Times

<!-- This section provides information about how roughly how long it takes to train the model and the size of the resulting model. -->


      - overall training time: 1 hour
      - model size: 495MB

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

The model obtained an F1-score of 71.83% and an accuracy of 71.98%.

## Technical Specifications

### Hardware


      - RAM: at least 16 GB
      - Storage: at least 2GB,
      - GPU: RTX3060

### Software


      - scikit-learn
      - Pytorch 2.2.2+cu118

## Bias, Risks, and Limitations

<!-- This section is meant to convey both technical and sociotechnical limitations. -->

NA

## Additional Information

<!-- Any other information that would be useful for other people to know. -->

The hyperparameters were determined by experimentation
      with different values.
