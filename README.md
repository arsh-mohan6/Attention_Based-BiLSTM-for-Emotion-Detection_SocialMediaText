# Emotion Classification using BiLSTM and Attention

##  Project Title
**Emotion Classification in Social Media Text using BiLSTM and Attention Mechanisms: A Study on Contextual and Negation-based Emotional Expressions**

---

##  Author
**Arsh Mohan Nishant**

---

##  Project Overview
This project focuses on **emotion classification in social media text** using deep learning techniques.  
We implemented and compared two models:

- **BiLSTM (Baseline Model)**
- **BiLSTM + Attention Mechanism (Proposed Model)**

The goal of this project is to analyze how well deep learning models understand **contextual meaning and negation-based emotional expressions** in short text data.

---

##  Objectives
- Perform emotion classification on social media text
- Compare BiLSTM and Attention-based models
- Analyze contextual understanding in NLP models
- Study limitations in handling **negation-based sentences**

---

##  Dataset
- Dataset: **Twitter Emotion Dataset**
- Total Samples: **416,809**
- Features:
  - `text` → social media sentence
  - `label` → emotion class

### Emotion Classes:
| Label | Emotion |
|------|--------|
| 0 | sadness |
| 1 | joy |
| 2 | love |
| 3 | anger |
| 4 | fear |
| 5 | surprise |

---

##  Tech Stack
- **Python**
- **TensorFlow / Keras**
- **NumPy**
- **Pandas**
- **Matplotlib / Seaborn**
- **Scikit-learn**
- **Google Colab**

---

##  Data Preprocessing
- Tokenization using Keras Tokenizer
- Text → Sequence conversion
- Padding sequences to fixed length (50)
- Train-test split (80/20)

---

##  Models Used

### 1️ BiLSTM (Baseline Model)
- Embedding Layer
- Bidirectional LSTM
- Dropout
- Dense Layer
- Softmax Output

---

### 2️ Attention-BiLSTM (Proposed Model)
- Embedding Layer
- BiLSTM
- Attention Layer
- Global Pooling
- Dense Layer
- Softmax Output

---

##  Hyperparameters
- Embedding Dimension: 128  
- Sequence Length: 50  
- Batch Size: 128  
- Epochs: 3  
- Optimizer: Adam  
- Loss Function: Sparse Categorical Crossentropy  

---

##  Results

| Model | Accuracy |
|------|---------|
| BiLSTM | **93.59%** |
| Attention-BiLSTM | **93.29%** |

---

##  Visualizations
The project includes:

- Emotion distribution graph
- Training accuracy curves
- Loss curves
- Confusion matrices
- Model architecture diagram

---

##  Key Observation (Important)
The model struggles with **negation-based expressions**.

### Example:
Input: I am not feeling happy
Prediction: joy

 Reason:
The model focuses on keywords like **"happy"** instead of understanding **negation context ("not")**.

---

##  Features
- Deep learning-based emotion classification
- Comparison of baseline and attention models
- Real-time prediction system
- Analysis of contextual understanding in NLP

---

##  Prediction System
A separate notebook allows real-time emotion prediction:

Input: I feel very happy today
Output: joy


---

##  Limitations
- Poor handling of negation (e.g., "not happy")
- Class imbalance in dataset
- Emotion overlap between categories

---

##  Future Work
- Use Transformer models (BERT, RoBERTa)
- Improve negation handling
- Use larger contextual embeddings
- Apply data balancing techniques

---

##  Project Structure
emotion_project/
│
├── data/
├── models/
├── results/
├── notebooks/
│ ├── bilstm_baseline.ipynb
│ ├── attention_model.ipynb
│ └── predict_emotion.ipynb


---

##  Acknowledgement
This project was developed as part of an **AI/ML Mini Project** at  
**KIIT University, Department of Computer Science and Engineering**

---

##  Conclusion
This project demonstrates that **BiLSTM models are highly effective for emotion classification**, while **Attention mechanisms provide interpretability but do not significantly improve accuracy**.  

It also highlights an important NLP challenge:  
 **Handling negation and contextual emotional shifts remains difficult.**

---

##  License
This project is for academic and educational purposes.
