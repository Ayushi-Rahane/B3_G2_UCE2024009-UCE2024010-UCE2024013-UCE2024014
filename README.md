# 🎭 **Emotion Detection Chatbot**
A conversational AI system that understands emotions, tracks mood changes, and generates empathetic responses.

---

## 👩‍💻 **Contributors**
- **Shrawani Deshmukh (UCE2024009)**  
- **Dhammavi Pilewan (UCE2024010)**  
- **Vrunani Muley (UCE2024013)**  
- **Ayushi Rahane (UCE2024014)**  

---

## 🏷️ **Badges**

![Python](https://img.shields.io/badge/Python-3.9+-blue?logo=python)  
![Flask](https://img.shields.io/badge/Framework-Flask-green)  
![Transformer](https://img.shields.io/badge/Model-DistilRoBERTa-orange?logo=huggingface)  
![License](https://img.shields.io/badge/License-MIT-purple)  

---

## 🎯 **Project Objective**

Traditional chatbots respond *generically*, without understanding how the user feels.  
This project aims to create an **emotionally intelligent chatbot** that:

✔ Detects emotions from user text using a transformer model  
✔ Refines predictions using sentiment polarity and rules  
✔ Tracks mood transitions across the conversation  
✔ Generates empathetic and context-aware replies  
✔ Visualizes emotional behaviour patterns (clusters, heatmaps, stats)

---

## 🧩 **Problem Statement**

Most chatbots treat every message the same, ignoring emotional context.  
This limits their effectiveness in:

- Support and helpdesk systems  
- Mental health assistance  
- Personalized AI companions  
- Interactive learning platforms  

**We solve this by building a chatbot that understands emotion and responds empathetically—not mechanically.**

---

## 📂 **Dataset**

**Dataset Name:** *Emotions Dataset for NLP (Kaggle)*  
**Total Samples:** ~2000  

**Emotion Labels:**  
- anger  
- fear  
- joy  
- love  
- sadness  
- surprise  

**Format:**  


**Used for:**  
- Training the baseline model  
- Evaluating both models  
- Generating confusion matrices  

---

## 🏗️ **System Architecture**
User Input  
&nbsp; &nbsp; ↓  
Text Preprocessing  
&nbsp; &nbsp; ↓  
Transformer-Based Emotion Prediction  
&nbsp; &nbsp; ↓  
Sentiment Polarity Refinement  
&nbsp; &nbsp; ↓  
Transition Matrix Update  
&nbsp; &nbsp; ↓  
Empathetic Response Generation  
&nbsp; &nbsp; ↓  
Visualization (Stats, PCA Clusters, History)


---

## 🧠 **Models & Methods**

### 🔹 **1. Primary Model – DistilRoBERTa**
- Model: **j-hartmann/emotion-english-distilroberta-base**  
- Handles context, sarcasm, multi-word meaning  
- Predicts 7 emotions  
- **Accuracy:** ~84.1%  
- **Macro F1:** 0.838  

---

### 🔹 **2. Supporting Modules**
- **Sentiment Analysis:** TextBlob  
- **Rule-based Tuning:** Keyword-based refinement  
- **Mood Tracking:** 7×7 **Transition Matrix**  
- **Embedding Clustering:** K-Means  
- **Dimensionality Reduction:** PCA  

---

### 🔹 **3. Baseline Model**
- **TF-IDF + Logistic Regression**  
- **Accuracy:** 86.9%  
- Strong on surface-level patterns  
- Weak in understanding context or subtle emotions  

---

## 🧪 **Results**

### **Model Comparison Table**

| **Metric** | **Baseline (TF-IDF LR)** | **DistilRoBERTa** |
|------------|---------------------------|--------------------|
| Accuracy | **86.9%** | 84.1% |
| Weighted F1 | 0.865 | **0.876** |
| Handles subtle emotions | ❌ | ✔ |
| Understands context | ❌ | ✔ |
| Works with long sentences | ❌ | ✔ |

---

### **Confusion Matrix Insights**
- **Baseline:** clear confusion between *love ↔ joy*, *surprise ↔ fear*  
- **Transformer:** stronger separation, especially for *joy, sadness, fear*

---

### **Qualitative Outputs**
- Real-time emotion tagging  
- Color-coded message bubbles  
- Live emotion statistics  
- PCA emotion clustering  
- Transition heatmap  
- Exportable conversation history  

---

## 🏁 **Conclusion**

This project shows that combining **transformers + sentiment refinement + mood tracking** creates a chatbot that is far more emotionally aware than traditional approaches.

The system provides:

- Accurate emotion predictions  
- Consistent mood tracking  
- Human-like empathetic responses  
- Visual analytics of emotional patterns  

It forms a strong foundation for future affective computing applications.

---

## 🚀 **Future Scope**

- Speech-based emotion detection  
- Multimodal emotion analysis (Text + Audio + Facial cues)  
- Dynamic LLM-based response generation  
- Long-term user mood analytics  
- Cloud & mobile deployment  
- Emotion intensity scoring (0–100 scale)

---

## 📚 **References**

1. A. Pophale, S. Gite, A. Thombre, *Emotion recognition using chatbot system*, 2021.  
2. J. Antony, S. G. Sudha, R. Prabha, *Emotion recognition-based mental healthcare chatbots: A survey*, 2021.  
3. P. Zhong, D. Wang, C. Miao, *Knowledge-enriched transformer for emotion detection*, 2019.  
4. C. Cortiz, *Exploring transformers in emotion recognition*, 2021.  
5. L. Bulla et al., *Distribution-shift robust emotion classification*, ACL 2023.

---

## ⚙️ **Installation**

```bash
git clone https://github.com/your-repo/emotion-detection-chatbot.git
cd emotion-detection-chatbot
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python backend/app.py

## ▶️ **Run the App**

```bash
python backend/app.py

## ▶️ **Run the App**: 👉 http://127.0.0.1:5000/


