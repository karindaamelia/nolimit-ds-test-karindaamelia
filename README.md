# Emotion Classification with Hugging Face Models and Sentence Embeddings

**Nama:** Karinda Amelia  
**Email:** karindaamelia21@gmail.com

## 📌 Project Summary
This project implements an **Emotion Classification** pipeline designed to identify emotions expressed in text messages. It leverages **Hugging Face Sentence-Transformers** (`all-MiniLM-L6-v2`) to generate dense text embeddings and applies a **Logistic Regression** model for classification.  

The workflow covers the entire process: dataset loading, exploratory data analysis (EDA), text preprocessing, embedding generation, model training, evaluation, inference, and deployment. The final solution is delivered through a **Streamlit web app**, enabling users to input text and instantly receive predicted emotions along with intuitive emoji indicators.  

**Objective**: Demonstrate the ability to build an end-to-end NLP solution using Hugging Face models and embeddings, with a clean, reproducible workflow.

Supported emotions:  
- 😢 Sadness  
- 😄 Joy  
- ❤️ Love  
- 😡 Anger  
- 😨 Fear  
- 😲 Surprise  

## 📊 Dataset Source & Annotation
We use the **Emotion Dataset** from Hugging Face: [dair-ai/emotion](https://huggingface.co/datasets/dair-ai/emotion).  

- **Source**: English tweets annotated with six basic emotions.  
- **Annotations**: Each text is labeled with one of the six emotion categories:  
  - `0`: sadness  
  - `1`: joy  
  - `2`: love  
  - `3`: anger  
  - `4`: fear  
  - `5`: surprise  
- **Splits**: 16,000 train / 2,000 validation / 2,000 test. 
- **License**: The dataset is released for **educational and research purposes only**, as specified by the original authors.   

Example:  
```json
{"text": "im feeling quite sad and sorry for myself but ill snap out of it soon", "label": 0}
```

## ⚙️ Setup Instructions

### 1. Clone Repository
```bash
git clone https://github.com/karindaamelia/nolimit-ds-test-karindaamelia.git
cd nolimit-ds-test-karindaamelia
```

### 2. Install Requirements
```bash
pip install -r requirements.txt
```

### 3. Run Streamlit App
```bash
streamlit run app.py
```

## 🤖 Models & Approach

- **Embedding Model**: [Sentence-Transformers/all-MiniLM-L6-v2](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2)  
  - A lightweight Transformer-based model from Hugging Face.  
  - Generates dense vector representations (embeddings) of text suitable for semantic similarity and classification tasks.  
  - Efficient in both speed and memory, making it well-suited for production-grade NLP pipelines.  

- **Classifier**: Logistic Regression (Scikit-learn)  
  - Implemented using `sklearn.linear_model.LogisticRegression`.  
  - Trained on text embeddings extracted from the Emotion dataset.  
  - Offers interpretability, fast training, and robust performance with dense embeddings.  
  - Serves as a solid baseline model for text classification tasks.  

## 🔗 Access Links

- **GitHub Repository**: [nolimit-ds-test-karindaamelia](https://github.com/karindaamelia/nolimit-ds-test-karindaamelia)  
- **Streamlit App**: [nolimit-ds-test-karindaamelia.streamlit.app](https://nolimit-ds-test-karindaamelia.streamlit.app/)  
