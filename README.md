# 🌐 Multilingual Translator & ML Model Evaluation

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Streamlit-Interactive%20App-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit">
  <img src="https://img.shields.io/badge/NLP-Multilingual%20Translation-4B8BBE?style=for-the-badge" alt="NLP">
  <img src="https://img.shields.io/badge/Machine%20Learning-Model%20Evaluation-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Machine Learning">
  <img src="https://img.shields.io/badge/Audio-Voice%20Processing-8A2BE2?style=for-the-badge" alt="Audio">
</p>

<p align="center">
  <b>A multilingual Streamlit application combining text translation, transliteration, text-to-speech, voice-to-text, and interactive machine-learning model evaluation.</b>
</p>

<p align="center">
  <a href="#-overview">Overview</a> •
  <a href="#-features">Features</a> •
  <a href="#-translation-workflow">Translation</a> •
  <a href="#-ml-evaluation">ML Evaluation</a> •
  <a href="#-tech-stack">Tech Stack</a> •
  <a href="#-getting-started">Getting Started</a>
</p>

---

## ✨ Overview

**Multilingual Translator & ML Model Evaluation** is a Streamlit-based Python application that brings together two major capabilities in one interface:

### 🌍 Multilingual Language Tools

- Translate text into a selected target language
- Romanize / transliterate translated text
- Convert translated text into speech
- Capture speech and convert it into text

### 🤖 Machine Learning Evaluation

- Clustering with K-Means
- Regression with Linear Regression
- Classification with multiple supervised learning algorithms
- Data preprocessing and feature scaling
- Imbalanced-data handling with SMOTE
- Visual evaluation using plots, heatmaps, and confusion matrices

The result is a practical application combining **NLP, speech processing, data preprocessing, machine learning, and interactive visualization**.

---

# 🚀 Features

| Feature | Description |
|---|---|
| 🌐 **Multilingual Translation** | Translate text into multiple target languages |
| 🔤 **Romanization** | Convert translated text into a more readable Romanized form |
| 🔊 **Text-to-Speech** | Generate audio from translated text |
| 🎙️ **Voice-to-Text** | Capture audio input and convert speech into text |
| 🧩 **Clustering** | Explore K-Means clustering |
| 📈 **Regression** | Train and evaluate Linear Regression models |
| 🧠 **Classification** | Compare Logistic Regression, Naive Bayes, SVM, and KNN |
| ⚖️ **SMOTE** | Handle imbalanced classification datasets |
| 📏 **Feature Scaling** | Scale numerical features with StandardScaler |
| 📊 **Visualization** | Generate correlation heatmaps, interactive plots, and confusion matrices |

---

# 🌍 Translation Workflow

```text
                 ┌────────────────────┐
                 │   User Text / Voice│
                 └─────────┬──────────┘
                           │
               ┌───────────┴───────────┐
               ▼                       ▼
       ┌───────────────┐       ┌───────────────┐
       │    Text Input │       │  Voice Input  │
       └───────┬───────┘       └───────┬───────┘
               │                       │
               │                       ▼
               │              Speech-to-Text
               │                       │
               └───────────┬───────────┘
                           ▼
                  GoogleTranslator
                           │
                           ▼
                 Translated Text
                           │
                  ┌────────┴────────┐
                  ▼                 ▼
            Transliteration    Text-to-Speech
                  │                 │
                  ▼                 ▼
          Romanized Output      Audio Output
```

---

# 🔤 Translation Capabilities

The translation workflow supports:

- 🌐 Source-language text input
- 🎯 Target-language selection
- 🔤 Romanization / transliteration
- 🔊 Audio generation through `gTTS`
- 🎙️ Voice-to-text input through `speech_recognition`

The translation component uses **GoogleTranslator** for language conversion and `gTTS` for text-to-speech generation.

---

# 🤖 Machine Learning Evaluation

The application also provides an interactive environment for evaluating several machine-learning approaches.

## 🧩 Clustering

### K-Means

Used to group data points based on similarity.

```text
Dataset
   │
   ▼
Feature Preparation
   │
   ▼
K-Means Clustering
   │
   ▼
Cluster Assignments
   │
   ▼
Interactive Visualization
```

---

## 📈 Regression

### Linear Regression

Used for predicting continuous target variables.

The workflow includes:

- Data preparation
- Feature/target separation
- Model training
- Prediction
- Evaluation
- Visualization

---

## 🧠 Classification

The application supports several classification algorithms:

| Model | Type |
|---|---|
| Logistic Regression | Linear classifier |
| Naive Bayes | Probabilistic classifier |
| Support Vector Machine | Margin-based classifier |
| KNeighborsClassifier | Instance-based classifier |

The interface allows models to be trained and evaluated on prepared datasets.

---

# 🧹 Data Preprocessing

Before model evaluation, the application supports several preprocessing steps.

### Missing Values

Missing values can be handled during dataset preparation.

### Categorical Encoding

Categorical variables are encoded using:

```python
LabelEncoder
```

### Feature Scaling

Numerical features are scaled using:

```python
StandardScaler
```

### Class Balancing

For imbalanced classification datasets, the project applies:

```python
SMOTE
```

This provides a more balanced training distribution before model evaluation.

---

# 📊 Visualization & Evaluation

The application includes visualization tools for understanding datasets and model performance.

### Available Visualizations

- 🔥 Correlation heatmaps
- 📊 Interactive Plotly visualizations
- 🔲 Confusion matrices
- 📈 Model evaluation outputs
- 🧩 Clustering visualizations
- 📉 Regression evaluation views

---

# 🧠 Application Architecture

```text
                 ┌─────────────────────┐
                 │     Streamlit UI    │
                 └──────────┬──────────┘
                            │
           ┌────────────────┼────────────────┐
           │                │                │
           ▼                ▼                ▼
     Language Tools     ML Workflow      Visualization
           │                │                │
     ┌─────┼─────┐      ┌───┼────┐           │
     │     │     │      │   │    │           │
     ▼     ▼     ▼      ▼   ▼    ▼           ▼
 Translate TTS  STT   Cluster Regr Class   Charts
     │                      │     │     │
     └──────────────────────┴─────┴─────┘
                    │
                    ▼
              Streamlit Output
```

---

# 🛠️ Tech Stack

<p align="center">

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" alt="Streamlit">
<img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" alt="NumPy">
<img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" alt="Pandas">
<img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white" alt="Scikit-learn">
<img src="https://img.shields.io/badge/Imbalanced--learn-SMOTE-6A1B9A?style=flat-square" alt="imbalanced-learn">
<img src="https://img.shields.io/badge/GoogleTranslator-Translation-4285F4?style=flat-square" alt="GoogleTranslator">
<img src="https://img.shields.io/badge/gTTS-Text%20to%20Speech-34A853?style=flat-square" alt="gTTS">
<img src="https://img.shields.io/badge/SpeechRecognition-Voice%20to%20Text-EA4335?style=flat-square" alt="Speech Recognition">
<img src="https://img.shields.io/badge/Plotly-Interactive%20Charts-3F4F75?style=flat-square&logo=plotly&logoColor=white" alt="Plotly">
<img src="https://img.shields.io/badge/Matplotlib-Visualization-11557C?style=flat-square" alt="Matplotlib">
<img src="https://img.shields.io/badge/Seaborn-Statistical%20Visualization-4C72B0?style=flat-square" alt="Seaborn">
<img src="https://img.shields.io/badge/Transliterate-Romanization-FFB000?style=flat-square" alt="Transliterate">

</p>

---

# 📁 Repository Structure

```text
Multiligual_translator/
│
├── 📂 images/
├── 🐍 Translator.py
├── 📦 requirements.txt
└── 📘 README.md
```

---

# ⚙️ Getting Started

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/Divakar1326/Multiligual_translator.git
cd Multiligual_translator
```

## 2️⃣ Create a Virtual Environment

### Windows

```bash
python -m venv .venv
.venv\Scriptsctivate
```

### macOS / Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

## 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

## 4️⃣ Run the Streamlit Application

```bash
streamlit run Translator.py
```

---

# 🧪 Typical Usage

### 🌍 Translation

1. Enter text or provide voice input.
2. Select a target language.
3. Translate the input.
4. View the translated output.
5. Romanize the translation when available.
6. Generate audio from the translated result.

### 🤖 Model Evaluation

1. Provide or load a dataset.
2. Prepare the features.
3. Apply preprocessing.
4. Select clustering, regression, or classification.
5. Train and evaluate the selected model.
6. Inspect metrics and visualizations.

---

# 📦 Core Python Libraries

```text
streamlit
numpy
pandas
matplotlib
seaborn
scikit-learn
imbalanced-learn
gTTS
speech-recognition
transliterate
plotly
```

> The repository's `requirements.txt` should remain the final source of truth for the exact dependency versions.

---

# 🧠 What This Project Demonstrates

- 🌐 Multilingual NLP application development
- 🎙️ Speech-to-text integration
- 🔊 Text-to-speech generation
- 🔤 Transliteration / Romanization
- 🧹 Data preprocessing
- 📏 Feature scaling
- ⚖️ Imbalanced-data handling
- 🤖 Classification
- 📈 Regression
- 🧩 Clustering
- 📊 Interactive visualization
- 🖥️ Streamlit application development

---

# 🔮 Future Improvements

Potential extensions include:

- 🌐 Add more translation providers or offline translation models
- 💬 Add translation history
- 🎙️ Improve real-time voice interaction
- 🧠 Add transformer-based NLP models
- 📊 Add richer model-comparison dashboards
- 📈 Add cross-validation and additional evaluation metrics
- 🚀 Deploy the application publicly
- 🧪 Add automated tests and validation

---

# ⚠️ Notes

- Internet connectivity may be required for external translation and text-to-speech services.
- Model results depend on the dataset and preprocessing configuration.
- Voice recognition quality can vary depending on audio quality and environment.
- This project is intended for educational and demonstration purposes.

---

# 👨‍💻 Author

## Divakar M  |  Brian Benton Nelson 

**B.Tech CSE — Artificial Intelligence & Data Science**

AI/ML • Generative AI • Python • NLP • Machine Learning

<p align="center">
  <a href="https://github.com/Divakar1326">
    <img src="https://img.shields.io/badge/GitHub-Divakar1326-181717?style=for-the-badge&logo=github" alt="GitHub">
  </a>
</p>
<p align="center">
  <a href="https://github.com/Briandeveloper007">
    <img src="https://img.shields.io/badge/GitHub-Briandeveloper007-181717?style=for-the-badge&logo=github" alt="GitHub">
  </a>
</p>
---

<p align="center">
  ⭐ If you find this project useful, consider starring the repository.
</p>

<p align="center">
  <b>Translate 🌍 • Analyze 🤖 • Visualize 📊</b>
</p>
