# NLP
# 🧠 Natural Language Processing (NLP) Roadmap


---

<img src="Images/roadmap.png" alt="NLP Roadmap" width="600"/>

---

## 📌 Part 1: Text Preprocessing using NLTK

### 🔹 Techniques Covered
- Tokenization
- Stemming (Porter, Regexp, Snowball)
- Lemmatization (WordNet)
- Stop Words Removal

---

### 1. 🔸 Tokenization
> Breaking down sentences into individual tokens (words or phrases).

<img src="Images/tokenization.png" alt="Tokenization" width="500"/>

---

### 2. 🔸 Stemming
> Reducing words to their root form.

| Stemmer Type       | Description                                         |
|--------------------|-----------------------------------------------------|
| **Porter Stemmer** | Automatic, fast, but lower accuracy                |
| **Regexp Stemmer** | Manual suffix removal, not automatic               |
| **Snowball Stemmer** | Improved accuracy over Porter                    |

---

### 3. 🔸 Lemmatization
> Converts words to their base dictionary form (lemma).

- Uses WordNetLemmatizer
- More accurate than stemming but slightly slower

---

### 4. 🔸 Stop Words Removal
> Removes common, insignificant words (like “is”, “the”, “and”) to focus on meaningful text.

---

## 📌 Part 2: Vectorization Techniques

### 🔹 Techniques Covered
- One Hot Encoding
- Bag of Words
- TF-IDF (Term Frequency - Inverse Document Frequency)

---

### 1. 🔸 One Hot Encoding
> Represents words as binary vectors based on vocabulary index.

<img src="Images/ohe.png" alt="One Hot Encoding" width="400"/>
<img src="Images/unique.png" alt="Vocabulary" width="300"/>

**Limitations:**
- Prone to **OOV (Out Of Vocabulary)** errors
- Does **not capture semantic meaning**

---

### 2. 🔸 Bag of Words
> Represents text by the frequency of words in a document.

*🖼️ Add Bag of Words diagram here*

---

### 3. 🔸 TF-IDF (Term Frequency-Inverse Document Frequency)
> Weights the word frequency by how unique a word is across documents.

*🖼️ Add TF-IDF illustration here*

---

## 🚀 Part 3: Deep Learning for NLP *(Coming Soon)*

- 🔄 **RNN (Recurrent Neural Networks)**
- 🔁 **LSTM (Long Short-Term Memory)**
- 🔃 **Bidirectional LSTM**
- 🔤 **Word Embeddings (Word2Vec, GloVe)**
- 🧠 **Transformer models (optional)**

---

### 🔄 1. Recurrent Neural Networks (RNN)

> RNNs are designed for sequential data. They maintain a hidden state that captures information from previous time steps, making them suitable for tasks like sentiment analysis and text generation.

<img src="Images/rnn.png" alt="RNN Architecture" width="500"/>

**Limitations:**
- Struggles with long sequences due to vanishing gradients
- Hard to capture long-term dependencies

---

### 🔁 2. Long Short-Term Memory Networks (LSTM)

> LSTM is a type of RNN that solves the vanishing gradient problem using memory cells and gates (input, forget, and output gates).

<img src="Images/lstm.png" alt="LSTM Cell Architecture" width="500"/>

**Advantages:**
- Retains long-term dependencies
- Widely used in text classification, machine translation, and time-series prediction

---

### 🔃 3. Bidirectional LSTM

> Bidirectional LSTMs process the sequence in both forward and backward directions, providing context from past and future at each time step.

<img src="Images/bilstm.png" alt="Bidirectional LSTM" width="500"/>

**Use Cases:**
- Named Entity Recognition (NER)
- Question Answering
- Text Summarization

---

### 🔤 4. Word Embeddings – Word2Vec

> Word2Vec is a technique to represent words as dense vectors that capture their semantic meaning. Words with similar context have similar vectors.

#### Two architectures:
- **CBOW (Continuous Bag of Words):** Predicts the current word from surrounding context.
- **Skip-Gram:** Predicts surrounding context given the current word.

<img src="Images/word2vec.png" alt="Word2Vec" width="500"/>

**Advantages:**
- Captures semantic similarity  
  (e.g., `"king" - "man" + "woman" ≈ "queen"`)
- Reduces dimensionality and sparsity compared to one-hot or TF-IDF

---

## ✅ Summary

| Technique          | Handles Sequence | Retains Context         | Semantic Understanding |
|--------------------|------------------|--------------------------|-------------------------|
| RNN                | ✅               | ✅ (short-term)          | ❌                      |
| LSTM               | ✅               | ✅ (long-term)           | ❌                      |
| BiLSTM             | ✅               | ✅ (bi-directional)      | ❌                      |
| Word2Vec           | ❌               | ❌                       | ✅                      |











<img src="Images/roadmap.png">



### Text PreProcessing using NLTK PART 1 
- Tokenization
- Stemming (Porter,RegexpStemmer, Snowball Stemmer)
- Lemmatizer
- Stop Words

#### 1. Tokenization 


<img src = "Images/tokenization.png">


#### 2. Stemming
Taking a word and Reducing it to its Word Stem
[eating,eaten,ate] ---> eat
[going,goes,gone] ----> go

##### Porter Stemmer : Automatic, Fast but low accuracy
##### Regexp Stemmer : Initliaze the suffix we need to clean/remove from the word. Not Automatic
##### SnowBall stemmer : Better than Porter Stemmer. 


#### 2. Word Net Lemmatizer (Lemmatization)
- Great Accuracy compared to stem but slower.

#### 3. Stop Words :
- StopWords are use to minimize the paragraph, it removes word that doesn't add any potential meaning to the paragraph



  <--------------------------------------------------------------------------------------------------------------------->

### Text Preprocessing using NLTK PART 2 
- One Hot Encoding
- Bag Of Words
- TDIDF ( Term Frequency- Inverse Document Frequency )

#### 1. One Hot Encoding:
- The Data is divided into unique Vocabulary.

<img src="Images/ohe.png" > <img src="Images/unique.png" >


- Only Problem is that if the data is small, such as `Pizza is Amazing`. It will cause OOV(OUT OF VOCABULARY)
- Also, Semantic Meaning is not captured

#### 2. Bag Of Words:

