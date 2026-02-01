# Code-Mixed Language Detection (Hindi–English)

## 📌 Overview
Code-mixed text, especially Hindi–English (Hinglish), is very common in social media, chat applications, and informal communication in multilingual societies like India. Traditional language identification systems fail on such data because they operate at the sentence level.

This project implements **token-level language identification** for **Hindi–English code-mixed text** using a **multilingual Transformer model (XLM-RoBERTa)**. Each word in a sentence is classified as either **Hindi (HI)** or **English (EN)**.

---

## 🎯 Objectives
- Perform **word-level language detection** on code-mixed sentences
- Handle both **Devanagari Hindi** and **English**
- Demonstrate Transformer-based token classification
- Provide an interactive **Streamlit web application**

---

## 🧠 Approach
- Treat language identification as a **token classification** problem
- Use **XLM-RoBERTa**, a pretrained multilingual Transformer
- Align word-level labels with subword tokenization
- Perform inference without fine-tuning (baseline experiment)

---

## 🏗️ Project Architecture

Input Sentence
↓
Word Tokenization
↓
XLM-RoBERTa Tokenizer
↓
Subword Embeddings
↓
Token Classification Head
↓
Word-level Language Labels (HI / EN)



---

## 📂 Project Structure

code-mixed-language-detection/
│
├── app.py # Streamlit web app
├── notebook.ipynb # Experiments and evaluation
├── requirements.txt # Python dependencies
├── README.md # Project documentation
└── .gitignore


---

## 🧪 Dataset
A small manually annotated Sentence: आज meeting थी boss के साथ
Tokens: आज | meeting | थी | boss | के | साथ
Labels: HI | EN | HI | EN | HI | HI


> ⚠️ Note: The dataset is intentionally small and used only for baseline evaluation.

आज meeting थी boss के साथ
आज → HI
meeting → EN
थी → HI
boss → EN
के → HI
साथ → HI


📊 Evaluation

Evaluation is performed using precision, recall, and F1-score.

precision    recall  f1-score
EN    0.30      1.00     0.46
HI    0.00      0.00     0.00

⚠️ Limitations

Model is not fine-tuned on Hinglish data
Romanized Hindi (e.g., kal, tum, kaha) is often misclassified
Very small dataset
Script bias toward English

🔮 Future Work

Fine-tune XLM-RoBERTa on large Hinglish datasets
Add CRF layer for better sequence consistency
Extend to multi-language code-mixing
Support Romanized Hindi
Integrate sentence-level aggregation

🧪 Technologies Used

Python
PyTorch
HuggingFace Transformers
XLM-RoBERTa
Scikit-learn
Streamlit
