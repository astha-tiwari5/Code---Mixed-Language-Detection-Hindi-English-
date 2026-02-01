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
