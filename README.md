# Language_Models
Creation of n-gram language models for spelling correction, next word prediction with evaluation

Contains 3 components:

1. Spelling correction using n-gram language models

2. Next word prediction using n-gram language models

3. Evaluation of language models

## Spelling correction using n-gram language models

### 1. Spelling Corrrection using bi-gram language models
    (i) Non-Words: Words that are not present in the corpus
    (ii) Real Words: Words that are present in the corpus

### 2. Dataset Used for training the language model
    (i) Gutenberg Corpus: 1 million words

### 3. Methodology
    (i) Preprocessing: Tokenization, removal of punctuations, removal of stop words, removal of numbers, removal of words with length less than 3
    (ii) Split into train and test set (80:20)
    (iii) Error Generation: A word is replaced with a random word from the corpus within edit distance 2
    (iv) Evaluation: Accuracy, Precision, Recall, F1 Score

### 4. Sample Examples

Non-Word Error:

```
a) They had determined that thirr marriage ought to be concluded.
b) He began to thenk.
c) I think there is a litlle likeness between us.
d) Her fathar fondly replied.
e) He kaw his son every year.
```

Real-Word Error:
```
a) They had determined that there marriage ought to be concluded.
b) He began to pink.
c) I think there is a brittle likeness between us.
d) Her gather fondly replied.
e) He raw his son every year.
```
