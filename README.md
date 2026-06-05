# AI Contract Intelligence System 📑

A high-performance, interactive, and visually stunning AI-powered dashboard for Legal Natural Language Inference (NLI). Built with **TensorFlow / Keras**, **Streamlit**, and **Plotly**, this platform classifies contract clauses and explains the decision boundary by extracting and highlighting real-time Multi-Head Self-Attention weights.

---

## 🚀 Key Features

* **Intelligent Clause Classification:** Identifies whether legal texts **entail**, **contradict**, or are **neutral** with respect to key legal covenants.
* **Explainable AI (XAI) Word Highlight Visualizer:** Uses eager evaluation hooks to extract Multi-Head Attention scores from the neural network and highlights tokens driving the predictions.
* **Multi-Head Attention Mappings:** Lets you inspect specific attention heads (Heads 1-4) or head averages via interactive Plotly heatmaps.
* **Sinusoidal Positional Encoding Visualizer:** Plots the positional sinusoidal vectors (sine/cosine curves) that the model uses to understand word ordering in a clause.
* **Dataset Insights:** Displays binned distribution patterns and donut charts summarizing the ContractNLI training corpus.
* **Exportable Reports:** Download compiled contract reports including prediction breakdowns, top vocabulary frequencies, and highly-attended tokens.

---

## 🛠️ Technology Stack

* **Frontend Framework:** Streamlit (injected with custom glassmorphic Dark Theme styling)
* **Model Engine:** TensorFlow / Keras (Multi-Head Self-Attention classification model)
* **Interactive Visualizations:** Plotly Express & Plotly Graph Objects
* **Data Processing:** NumPy, Pandas, Scikit-Learn
* **Utility Libraries:** WordCloud, Matplotlib

---

## 📦 Setup & Installation

### Prerequities
Make sure Python 3.9+ is installed on your local machine.

### 1. Clone the Repository
```bash
git clone <your-repository-url>
cd AI_Contract_Intelligence_System
```

### 2. Install Dependencies
Install all package requirements via pip:
```bash
pip install -r requirements.txt
```

### 3. Run the Dashboard locally
Launch the Streamlit app:
```bash
python -m streamlit run app.py
```
Open `http://localhost:8501` in your browser.

---

## 🌐 Deploying to Streamlit Community Cloud

Streamlit Community Cloud is the easiest way to deploy and share this project. Follow these steps:

### Step 1: Upload to GitHub
1. Create a public GitHub repository.
2. Initialize Git in this directory:
   ```bash
   git init
   git add .
   git commit -m "Initial commit - modern dashboard"
   ```
3. Push your code to your remote GitHub repository.

### Step 2: Set up Streamlit Community Cloud
1. Log in to [Streamlit Community Cloud](https://share.streamlit.io/).
2. Click **New App** and sign in with your GitHub account.
3. Select your repository, the correct branch (e.g. `main` or `master`), and specify the main file path as `app.py`.
4. Click **Deploy**. Streamlit will automatically read `requirements.txt`, install dependencies, load the neural network (`attention_model.h5`), and host your app on a public URL!

*Note: Since the model weights file (`attention_model.h5`) is around 16 MB, it is small enough to commit directly to Git without Git LFS.*
