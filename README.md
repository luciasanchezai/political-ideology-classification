# 🧠 Political Ideology Classification on Twitter

Multiclass text classification of political ideologies using tweets in Spanish.  
This project applies NLP techniques and various machine learning models to classify users' political orientation based on their tweets.

---

## 📚 Project Description

This project was part of the "Natural Language Processing I" course at URJC.  
It focuses on classifying political ideologies in Spanish tweets using:

- **Classical ML models**: Logistic Regression, Naive Bayes, SVM
- **Neural networks**: CNNs
- **Pretrained models**: BERT (bert-base-cased)

Data comes from the **PoliticEs 2022** shared task at IberLEF, with over 28,000 tweets for training and 4,600 for validation.

---

## 🔧 Technologies Used

- **Languages**: Python  
- **Libraries**: scikit-learn, pandas, NumPy, gensim, spaCy, NLTK, TensorFlow, PyTorch, Transformers  
- **Embeddings**: Word2Vec (SBW vectors), FastText  
- **Preprocessing**: emoji handling, lemmatization, n-gram extraction

---

## 🧪 Vector Representations

- **CountVectorizer (binary)**: n-grams (1–3), max_df = 0.9  
- **TF-IDF**: adjusted with Spanish stopwords  
- **Word2Vec**: pretrained SBW vectors (300-dim)  
- **FastText**: custom-trained, 200-dim, character n-grams  
- **BERT**: fine-tuned on training set (1 epoch, bert-base-cased)

---

## 🤖 Models and Results

| Model                     | Representation    | Macro-F1 |
|--------------------------|-------------------|----------|
| Logistic Regression      | Binary n-grams    | **0.543** |
| Logistic Regression      | TF-IDF            | 0.543    |
| Naive Bayes              | Binary n-grams    | 0.534    |
| Naive Bayes              | TF-IDF            | 0.492    |
| SVM                      | TF-IDF            | 0.529    |
| CNN                      | FastText          | 0.427    |
| CNN                      | Word2Vec          | 0.098    |
| BERT (bert-base-cased)   | Fine-tuned (1 ep) | 0.519†   |

† Approximated from accuracy

---


## 🚀 Future Improvements

- Full fine-tuning using Spanish-specific models like BETO or RoBERTa  
- Improve CNN performance with better architectures (e.g., BiLSTM)  
- Include more metadata: user profile, hashtags, etc.  
- Evaluate generalization with multilingual tweets

---

## 📄 Report

The full project report is available in [`report.pdf`](report.pdf) (in Spanish).

---

## 👩🏻‍💻 Author

Lucía Sánchez  
[LinkedIn](https://www.linkedin.com/in/lucia-sanchez-102978277) · [Email](mailto:lusanchezca.ai@gmail.com)


