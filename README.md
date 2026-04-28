# Diploma Thesis: Sentiment Analysis using Machine Learning and Deep Learning

**Title:** Use of Machine Learning and Language Technology Tools for Knowledge Extraction from Text (Text Mining)  
**Author:** Roman Pantsenko  
**University:** Ionian University, Department of Computer Science  
**Year:** 2024

## 📖 Abstract

This thesis explores sentiment analysis, a subfield of Natural Language Processing (NLP), by applying both classical machine learning and deep learning models on a Twitter dataset. Four models were implemented and compared: a Convolutional Neural Network (CNN), a Long Short-Term Memory network (LSTM), a simple Recurrent Neural Network (RNN), and a Support Vector Machine (SVM). The goal was to classify tweets as positive or negative sentiment. The LSTM model achieved the best overall performance with an average F1-score of 0.76.

## 🧰 Technologies & Tools

- **Language:** Python 3.12
- **Libraries:** pandas, numpy, scikit-learn, TensorFlow / Keras, matplotlib, seaborn
- **Environment:** Jupyter Notebook, Anaconda
- **Word Embeddings:** Word2Vec (via Keras Tokenizer)

## 📊 Dataset

- **Source:** Twitter (sampled from a public sentiment dataset)
- **Size:** 40,000 tweets (after sampling)
- **Classes:** 0 = negative, 4 = positive (balanced)
- **Preprocessing:** Removal of unnecessary columns, text tokenization, padding to fixed length (36 tokens)

## 🤖 Models Implemented

| Model | Architecture Summary |
|-------|----------------------|
| CNN   | Embedding → Conv1D → MaxPooling → Conv1D → GlobalMaxPooling → Dense(5) |
| LSTM  | Embedding → LSTM(32) → LSTM(64) → LSTM(128) → Dense(5) |
| RNN   | Embedding → SimpleRNN(64) → Dense(5) |
| SVM   | StandardScaler → SVC(gamma='auto') |

All neural models were trained for **2 epochs** with **batch size 100**.

## 📈 Results (average metrics)

| Model | Precision | Recall | F1-Score |
|-------|-----------|--------|-----------|
| CNN   | 0.74      | 0.73   | 0.73      |
| LSTM  | 0.77      | 0.76   | **0.76**  |
| RNN   | 0.74      | 0.74   | 0.74      |
| SVM   | 0.52      | 0.52   | 0.49      |

- The **LSTM** model outperformed the others, especially in correctly identifying negative sentiment (recall 0.86 for class 0).
- The **SVM** performed poorly due to the high-dimensional, sequential nature of text data.

## 🚀 How to Run the Code

1. **Clone the repository**  
   ```bash
   git clone https://github.com/romanp217/diploma-thesis.git
   cd diploma-thesis
   ```

2. **Install dependencies** (recommend using a virtual environment)  
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Jupyter notebook**  
   ```bash
   jupyter notebook code.ipynb
   ```

   Execute cells sequentially. The notebook loads the dataset (`data.csv`), preprocesses it, builds and trains the four models, and prints evaluation metrics and confusion matrices.

## 📁 Repository Contents

- `code.ipynb` – Full Jupyter notebook with all experiments.
- `ΤΕΛΙΚΟ_ΚΕΙΜΕΝΟ.docx` – Full thesis text (in Greek).
- `README.md` – This file.

## 📄 License

Academic use only. For any other use, please contact the author.

---

**Author:** Roman Pantsenko – [GitHub](https://github.com/romanp217)
[LinkedIn](https://www.linkedin.com/in/roman-pantsenko-95a648294/)
email - [romanpn17@outlook.com](mailto:romanpn17@outlook.com)
