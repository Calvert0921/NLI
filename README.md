# Method A: SVM
Method a employs the traditional architecture--SVM

We compared three embedding methods--GloVe, DeBERTa and sBERT

## Instructions
**Install dependencies**

You can find all necessary dependencies in SVM_glove.ipynb

**Train and test SVM**

To train the different models, you can run SVM_glove.ipynb, SVM_DeBERTa.ipynb and SVM_sBERT.ipynb under method_a folder

The trained models are available at https://github.com/Calvert0921/NLI/tree/main/method_a/models

The demo.ipynb only includes SVM with sBERT, which achieved the best performance


# Method B: HBMP Model
This is a HBMP model that employs hierarchical layers of Bi-directional Long Short-Term Memory (BiLSTM) networks combined with max pooling.

## Instructions
To train the model, follow the steps below:

**Install dependencies**

The following dependencies are required (versions used in brackets):
Python 
Pytorch (2.2.2+cu118)
Numpy (1.14.3)
Torchtext (for preprocessing) (0.6.0)
SpaCy (for tokenization) (3.7.4)

This will download the needed word embeddings, including:
[GloVe 840B 300D](https://nlp.stanford.edu/projects/glove/)

**Train and test HBMP**
Run the [train.ipynb](https://github.com/Calvert0921/NLI/blob/02f87f8cca2269abede3551dfb5032c8ecdf91b4/method_b/train.ipynb) to train and evaluate the model.

Run the [test.ipynb](https://github.com/Calvert0921/NLI/blob/02f87f8cca2269abede3551dfb5032c8ecdf91b4/method_b/demo.ipynb) to test the [trained model](https://github.com/Calvert0921/NLI/blob/main/method_b/best_HBMP_600D_devacc_72.17_epoch_3.pt).


## References
[1] Aarne Talman, Anssi Yli-Jyrä and Jörg Tiedemann. 2019. [Sentence Embeddings in NLI with Iterative Refinement Encoders](https://www.cambridge.org/core/journals/natural-language-engineering/article/sentence-embeddings-in-nli-with-iterative-refinement-encoders/AC811644D52446E414333B20FEACE00F). Natural Language Engineering. 25 (4), 467-482.
