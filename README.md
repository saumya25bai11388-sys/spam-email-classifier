# 📧 Spam Email Classifier

A machine learning project that classifies SMS/email messages as **Spam** or **Ham (Not Spam)** using Natural Language Processing and supervised learning techniques.

Built as part of the **Fundamentals of AI and ML** course capstone (BYOP project).

---

## 🧠 Problem Statement

Spam messages are a widespread issue affecting communication systems worldwide. Every day, millions of unwanted, deceptive, or malicious messages are sent to users. The goal of this project is to build a model that can automatically detect and filter spam messages using machine learning — specifically, text classification.

---

## 📊 Dataset

- **Source:** [SMS Spam Collection Dataset — UCI ML Repository](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)
- **Size:** ~5,574 SMS messages
- **Labels:** `spam` (747 messages) | `ham` (4,827 messages)
- Loaded directly from a public URL — no manual download required.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3 | Core programming language |
| pandas | Data loading and manipulation |
| NLTK | Text preprocessing (stopwords, stemming) |
| scikit-learn | TF-IDF vectorization, model training, evaluation |
| matplotlib / seaborn | Data visualizations |
| WordCloud | Word frequency visualization |

---

## ⚙️ How It Works

```
Raw Text → Preprocessing → TF-IDF Vectorization → ML Model → Spam / Ham
```

1. **Preprocessing:** Lowercase, remove URLs/special characters, remove stopwords, apply Porter Stemming
2. **Feature Extraction:** TF-IDF with unigrams and bigrams (`max_features=5000`)
3. **Models Trained:**
   - Multinomial Naive Bayes (primary)
   - Logistic Regression (comparison)
4. **Evaluation:** Accuracy, Precision, Recall, F1-Score, Confusion Matrix

---

## 🚀 How to Run

### Option 1: Google Colab (Recommended)

1. Open the notebook file `spam_email_classifier.ipynb` in [Google Colab](https://colab.research.google.com/)
2. Click **Runtime → Run All**
3. All dependencies install automatically — no setup needed!

### Option 2: Local (Jupyter Notebook)

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/spam-email-classifier.git
cd spam-email-classifier

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook spam_email_classifier.ipynb
```

---

## 📦 Requirements

```
pandas
numpy
matplotlib
seaborn
wordcloud
nltk
scikit-learn
```

Install all at once:
```bash
pip install pandas numpy matplotlib seaborn wordcloud nltk scikit-learn
```

---

## 📈 Results

| Model | Accuracy | Precision (Spam) | Recall (Spam) | F1-Score |
|-------|----------|-----------------|--------------|----------|
| Multinomial Naive Bayes | ~98% | ~97% | ~95% | ~96% |
| Logistic Regression | ~98% | ~98% | ~96% | ~97% |

Both models achieve strong performance. Naive Bayes is particularly well-suited for text classification due to its probabilistic nature and speed.

---

## 🔍 Key Findings

- Spam messages are **significantly longer** than ham messages on average
- Strong spam indicators: `free`, `win`, `prize`, `urgent`, `claim`, `call now`
- TF-IDF with **bigrams** improves detection of common spam phrases like "free entry" or "win prize"
- The model correctly classifies unseen messages with high confidence

---

## 🧪 Try It Yourself

At the end of the notebook, there's an interactive cell where you can type any message and get an instant prediction:

```
Enter a message to test: Congratulations! You've won a FREE iPhone!
Prediction: 🚨 SPAM
Confidence: 99.2%
```

---

## 📁 Project Structure

```
spam-email-classifier/
│
├── spam_email_classifier.ipynb   # Main notebook (all code)
├── README.md                     # This file
└── requirements.txt              # Python dependencies
```

---

## 👤 Author

Name:Saumya Sinha  
Course: Fundamentals of AI and ML  
Institution: VIT  
Academic Year: Winter Sem 2025–26

---
https://colab.research.google.com/github/saumya25bai11388-sys/spam-email-classifier/blob/main/spam_email_classifier.ipynb

## 📄 License

This project is for academic purposes only.

