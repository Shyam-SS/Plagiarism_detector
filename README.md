#  Plagiarism Detector using Sentence-BERT

A machine learning project that detects **semantic similarity** between sentence pairs using a pre-trained **Sentence-BERT** model. The goal is to build a basic **plagiarism detector** capable of identifying paraphrased or meaning-equivalent sentences.

---

##  Features

- Semantic similarity detection using Sentence-BERT
- Cosine similarity scoring between sentence embeddings
- Supports both script (`.py`) and interactive notebook (`.ipynb`) execution
- Evaluation using Accuracy, Precision, Recall, and F1 Score
- Custom sentence input support for real-time testing

---

##  Model Used

- **Model**: `all-MiniLM-L6-v2` (from [Sentence-Transformers](https://www.sbert.net/))
- **Task**: Sentence Embedding & Semantic Similarity
- **Metric**: Cosine Similarity
- **Threshold**: 0.5 (for binary classification: similar(1) / not similar(0)

---

## 📂 Project Structure

```

Plagiarism-Detector/
├── data/                      # Dataset (e.g., SNLI) zip file
│   └── train\_snli.txt
├── notebook/
│   └── Plagiarism\_detector.ipynb   # Jupyter notebook for step-by-step explanation
├── src/
│  └── plagiarism\_detector.py      # Python script version for execution
├── Pretrained Model/Output         # Given below
├── requirements.txt                # Dependency list
├── .gitignore                      # Files/folders excluded from Git
└── README.md                       # This file

## 📥 Download Pretrained Model

Due to GitHub file size limits, the trained model is hosted externally.

### 🔗 [Download the model from Google Drive](https://drive.google.com/file/d/1g7-mpVDm4g7FKSRp4Jz-uHfnqNLI1eTS/view?usp=sharing)

After downloading, extract the zip file and place the folder like this:
output/
└── plagiarism-checker-model/
├── config.json
├── modules.json
└── ...

---

## 📊 Dataset

- **Name**: [SNLI Dataset (Stanford Natural Language Inference)](https://nlp.stanford.edu/projects/snli/)
- **Format**: TSV with three columns: `sentence1`, `sentence2`, `label`
- **Label Mapping**:
  - `entailment` → 1 (Similar)
  - `contradiction`, `neutral` → 0 (Not Similar)

---

## 🛠️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Shyam-SS/Plagiarism-Detector.git
cd Plagiarism-Detector
````

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🚀 How to Use

### ▶️ Run via Python Script

```bash
cd src
python plagiarism_detector.py
```

### 📓 Or Use the Jupyter Notebook

```bash
jupyter notebook notebook/Plagiarism_detector.ipynb
```

---

## 🧪 Sample Output

```
📊 Evaluation Results on Test Set:
Accuracy  : 0.81
Precision : 0.78
Recall    : 0.87
F1 Score  : 0.82

📝 Test the model with your own input sentences.
Enter the first sentence: A man is a player in a basketball game.
Enter the second sentence:A basketball game is being played.

🔍 Cosine Similarity Score:0.7984
✅ Prediction: Similar (1)
Enter the first sentence : Children smiling and waving at camera
Enter the second sentence: The kids are frowning

🔍 Cosine Similarity Score: 0.2373
✅ Prediction =  not similar (0)
Enter the first sentence : Children smiling and waving at camera	
Enter the second sentence: There are children present

🔍 Cosine Similarity Score: 0.5892
 Prediction = Similar (1)
```

---

## 📆 Requirements

```
torch
sentence-transformers
transformers
pandas
scikit-learn
```

> All dependencies are listed in `requirements.txt`.

---

## 📀 Exported Model

After running the script, the Sentence-BERT model is saved to:

```
output/plagiarism-checker-model/
```

You can reload it later for prediction without retraining.

---

## 👨‍💼 About Me

**Shyam Sunder Singh**
Frontend & AI-ML Intern
[LinkedIn](https://www.linkedin.com/in/shyam-sunder-singh)
[GitHub](https://github.com/Shyam-SS)

```
```


