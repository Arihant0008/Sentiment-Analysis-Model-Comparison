# 📊 Sentiment Analysis Model Comparison

This project compares **three Hugging Face Transformer models** on the **Amazon Fine Food Reviews dataset** to evaluate their sentiment classification performance efficiently.

---

## 🚀 **Project Overview**

✅ **Objective:**  
To analyse and compare the accuracy of **different pre-trained sentiment analysis models** on product reviews for practical NLP applications.

✅ **Dataset Used:**  
- **Amazon Fine Food Reviews**  
- Source: [Kaggle](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews?resource=download&select=Reviews.csv)
- Subset: First 100 samples used for quick evaluation.

---

## 🔬 **Models Evaluated**

1. **DistilBERT (SST-2)**
   - `distilbert-base-uncased-finetuned-sst-2-english`
   - Lightweight and fast for binary sentiment analysis.

2. **nlptown Multilingual BERT**
   - `nlptown/bert-base-multilingual-uncased-sentiment`
   - Outputs 1-5 star ratings, mapped to Positive, Neutral, Negative.

3. **CardiffNLP Twitter RoBERTa**
   - `cardiffnlp/twitter-roberta-base-sentiment`
   - Fine-tuned on Twitter data, generalises well to short reviews.

---

## 📈 **Final Model Accuracies**

| **Model** | **Accuracy** |
|---|---|
| distilbert-base-uncased-finetuned-sst-2-english | 0.75 |
| nlptown/bert-base-multilingual-uncased-sentiment | 0.86 |
| cardiffnlp/twitter-roberta-base-sentiment | 0.81 |

✅ **Conclusion:**  
The **nlptown multilingual BERT model achieved the highest accuracy (86%)**, demonstrating strong generalisation to Amazon reviews.

---

## 🛠️ **Project Workflow**

1. **Data Loading & Preprocessing**
   - Loaded reviews and mapped scores to sentiment labels.

2. **Model Loading & Inference**
   - Used Hugging Face `pipeline()` with GPU acceleration for fast evaluation.
   - Applied **safe input truncation** to avoid token length errors.

3. **Accuracy Evaluation**
   - Compared predicted sentiments with ground truth labels.

4. **Visualisation**
   - Plotted a **bar graph** to compare model accuracies visually.

---

## 💻 **Instructions to Run**

1. Clone the repository:

```bash
git clone https://github.com/yourusername/Sentiment-Analysis-Model-Comparison.git
cd Sentiment-Analysis-Model-Comparison
```
