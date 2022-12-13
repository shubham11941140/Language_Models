# Language_Models
Creation of n-gram language models for spelling correction, next word prediction with evaluation

Contains 4 components:

1. Spelling correction using n-gram language models

2. Sequence Extraction using n-gram language models

3. Evaluation of language models

4. Latin Language models

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

### 5. Results

Non-Word Error:

![image](https://user-images.githubusercontent.com/63910248/205891792-9c1394ff-2d91-4d01-b310-fa9fd7060d63.png)

Real-Word Error:

![image](https://user-images.githubusercontent.com/63910248/205891880-1e15ceff-ccc5-42e1-ad2e-062a428b533d.png)

## Sequence Extraction using n-gram language models

### Sequence Extraction using tri-gram language models
    Given a sequence of characters with no spaces in between, recover the correct sequence of words. For example, given a text “itdoesnotmattertotheboard”, the extracted sequence should be: - “It”, “does”, “not”, “matter”, “to”, “the”, “board”.

### 2. Dataset Used for training the language model
    (i) Brown Corpus: 1 million words

### 3. Methodology
    (i) Preprocessing: Tokenization, removal of punctuations, removal of stop words, removal of numbers, removal of words with length less than 3
    (ii) Split into train and test set (80:20)
    (iii) For every statement in the test set, combine it and check if your model can split it correctly
    (iv) one-grams.txt attached to train the model
    (v) Evaluation: Accuracy, Precision, Recall, F1 Score

### 4. Sample Examples

```
a) “Myunscientificfrienddoesnotbelievethathumanstatureismeasurablein
termsofspeed”
b) “Myhostwentoverandstaredoutthewindowathispeacocks”
c) “wheninthecourseofhumaneventsitbecomesnecessaryforonepeople”
d) “Ihavetobesomewhatcarefulinmychoiceofwords”
```

### 5. Results

![image](https://user-images.githubusercontent.com/63910248/205895867-d6dcccd9-96cc-482f-b3b5-605af57d8822.png)

## Evaluation of language models (Bigram, Trigram and Quadgram)

### 1. Dataset Used for training the language model
    (i) Webtext Corpus: 1 million words The webtext corpus includes content from a Firefox discussion forum, conversations overheard in New York, Pirates of the  Caribbean movie scripts, personal advertisements, and wine reviews.

### 2. Methodology
    (i) Preprocessing: Tokenization, removal of punctuations, removal of stop words, removal of numbers, removal of words with length less than 3
    (ii) Split into train and test set (70:30)
    (iii) Evaluation: Perplexity

### 3. Results

Bigram:

![image](https://user-images.githubusercontent.com/63910248/205903853-a0025aca-6058-4d8d-872b-38a6aca8d272.png)


Trigram:

![image](https://user-images.githubusercontent.com/63910248/205903892-36f22ed9-5ab1-43ab-b128-18aa7dfc945b.png)

Quadgram:

![image](https://user-images.githubusercontent.com/63910248/205903924-4391ade6-b203-4238-90b6-72b9904edb02.png)

