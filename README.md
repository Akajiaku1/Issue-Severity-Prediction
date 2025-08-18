# 🧠 Issue Severity Prediction using Machine Learning and BERT

This project demonstrates how to predict the severity of software issues (bugs, incidents, feature requests) using synthetic data. It includes two approaches:
- A **traditional ML approach** using TF-IDF and Random Forest.
- A **deep learning approach** using BERT from Hugging Face Transformers.

---

## 📁 Project Structure

├── issue_severity_synthetic_data.xlsx # Synthetic dataset (generated) ├── traditional_model.py # Random Forest model using TF-IDF ├── bert_model.py # Fine-tuned BERT model ├── issue_severity_model/ # Saved Hugging Face BERT model ├── issue_severity_model.pt # PyTorch format saved model └── README.md # Project documentation


---

## 🧪 Dataset

The dataset is synthetically generated and includes:
- `Title`: Short description of the issue
- `Description`: Longer explanation of the issue
- `Severity`: Labeled as one of `Low`, `Medium`, `High`, or `Critical`

To generate it, run:

```python
python generate_data.py

Or load from Excel:

import pandas as pd
df = pd.read_excel("issue_severity_synthetic_data.xlsx")

🔍 Model 1: Traditional ML

    Preprocessing: TF-IDF vectorization

    Model: RandomForestClassifier

    Evaluation: Classification Report + Confusion Matrix

python traditional_model.py

🤖 Model 2: Deep Learning with BERT

    Pretrained model: bert-base-uncased

    Fine-tuned for multi-class classification

    Hugging Face Trainer API for training & evaluation

python bert_model.py

Model saved to:

    Hugging Face format: issue_severity_model/

    PyTorch .pt format: issue_severity_model.pt

📊 Evaluation

Includes metrics:

    Accuracy

    F1-Score (macro)

    Confusion Matrix

    Classification Report

🚀 Requirements

Install dependencies:

pip install pandas scikit-learn transformers datasets torch

📦 Export

    Download Excel file: issue_severity_synthetic_data.xlsx

    Exported models in Hugging Face and PyTorch formats

📌 Future Improvements

    Add REST API using FastAPI

    Integrate with Jira/GitHub Issues for real data

    Deploy model using Docker & Hugging Face Spaces
Author
  Name: Otutu Anslem
  Github: https://github.com/Otutu11
  LinkedIn: https://www.linkedin.com/in/otutu-anslem-53a687359/

📜 License

MIT License – feel free to use, modify, and distribute.
