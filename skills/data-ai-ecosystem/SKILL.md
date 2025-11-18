---
name: data-ai-ecosystem
description: Master data science, machine learning, and AI/ML engineering including deep learning, data pipelines, and prompt engineering. Use when building ML models, processing large datasets, implementing AI applications, or optimizing ML systems.
---

# Data Science & AI/ML Ecosystem Skill

## Quick Start

Build end-to-end machine learning systems from data processing through deployment and monitoring.

### Essential ML Stack

```python
# Python scikit-learn and TensorFlow example
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, precision_score, recall_score
import tensorflow as tf

# Load and prepare data
df = pd.read_csv('data.csv')
X = df.drop('target', axis=1)
y = df['target']

# Train-test split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Scale features
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)

# Train model
model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train_scaled, y_train)

# Evaluate
y_pred = model.predict(X_test_scaled)
print(f"Accuracy: {accuracy_score(y_test, y_pred)}")
print(f"Precision: {precision_score(y_test, y_pred)}")
print(f"Recall: {recall_score(y_test, y_pred)}")
```

## Learning Domains

### 📊 **Data Science Fundamentals**

**Statistics & Probability**
- Descriptive statistics
- Probability distributions
- Hypothesis testing
- Bayesian inference

**Exploratory Data Analysis (EDA)**
- Data visualization (Matplotlib, Seaborn, Plotly)
- Statistical summaries
- Correlation and distribution analysis
- Outlier detection

**Data Preprocessing**
- Missing value handling
- Data cleaning and validation
- Feature scaling and normalization
- Encoding categorical variables

### 🤖 **Machine Learning**

**Supervised Learning**
- Linear and logistic regression
- Decision trees and random forests
- Support vector machines (SVM)
- Ensemble methods (boosting, bagging)
- Hyperparameter tuning

**Unsupervised Learning**
- Clustering (K-means, DBSCAN, hierarchical)
- Dimensionality reduction (PCA, t-SNE)
- Association rules
- Anomaly detection

**Reinforcement Learning**
- Q-learning and SARSA
- Policy gradient methods
- Deep Q-networks (DQN)
- Multi-armed bandits

### 🧠 **Deep Learning**

**Neural Networks**
- Feedforward networks
- Convolutional neural networks (CNN)
- Recurrent neural networks (RNN, LSTM, GRU)
- Transformer architectures

**Transfer Learning**
- Pre-trained models (ResNet, BERT, GPT)
- Fine-tuning strategies
- Domain adaptation
- Few-shot learning

**Generative Models**
- Autoencoders
- Generative Adversarial Networks (GANs)
- Variational autoencoders (VAE)
- Diffusion models

### 📈 **Data Engineering**

**Data Pipelines**
- ETL/ELT architecture
- Batch processing (Spark, Hadoop)
- Stream processing (Kafka, Flink)
- Workflow orchestration (Airflow, Dagster)

**Data Storage**
- Data warehouses (Snowflake, Redshift)
- Data lakes (S3, HDFS)
- Distributed databases
- Time-series databases

**Data Quality**
- Data validation
- Data profiling
- Anomaly detection
- Data lineage and governance

### 🚀 **MLOps & Deployment**

**Model Development**
- Scikit-learn workflows
- TensorFlow and PyTorch
- Model selection and evaluation
- Cross-validation strategies

**Model Serving**
- REST APIs for model inference
- Batch prediction
- Real-time serving (TensorFlow Serving, TorchServe)
- Edge deployment

**Monitoring & Maintenance**
- Model performance monitoring
- Data drift detection
- Model retraining triggers
- A/B testing for models

**CI/CD for ML**
- Automated testing pipelines
- Model versioning (DVC, MLflow)
- Continuous training
- Automated deployment

### 💬 **Prompt Engineering & LLMs**

**Prompt Design**
- Few-shot learning
- Chain-of-thought prompting
- Structured prompts
- Prompt templates and examples

**LLM Fine-tuning**
- Transfer learning for language
- Domain-specific adaptation
- Low-rank adaptation (LoRA)
- Instruction tuning

**RAG Systems**
- Retrieval-augmented generation
- Vector databases (Pinecone, Weaviate)
- Semantic search
- Context management

**Prompt Safety**
- Adversarial prompts
- Jailbreak prevention
- Bias detection and mitigation
- Output validation

### 🔬 **Specialized Domains**

**Natural Language Processing**
- Text preprocessing (tokenization, stemming)
- Word embeddings (Word2Vec, GloVe)
- Transformers (BERT, GPT)
- Named entity recognition (NER)

**Computer Vision**
- Image classification
- Object detection
- Semantic segmentation
- Image generation

**Time Series Analysis**
- Forecasting methods (ARIMA, exponential smoothing)
- Deep learning for time series (LSTM, Transformer)
- Anomaly detection
- Seasonal decomposition

## Skill Development Checklist

- [ ] Build complete ML pipeline (data → model → deployment)
- [ ] Preprocess and clean real-world datasets
- [ ] Train multiple models and compare performance
- [ ] Implement feature engineering (10+ new features)
- [ ] Achieve 90%+ accuracy on classification task
- [ ] Deploy model as REST API
- [ ] Setup model monitoring and retraining
- [ ] Implement RAG system with LLMs
- [ ] Create data pipeline with Airflow/Prefect

## Real-World Scenarios

**Customer Churn Prediction**
```python
# End-to-end ML workflow
import pandas as pd
from sklearn.preprocessing import StandardScaler, LabelEncoder
from sklearn.model_selection import train_test_split
from xgboost import XGBClassifier
from sklearn.metrics import roc_auc_score, confusion_matrix

# Load data
df = pd.read_csv('customer_churn.csv')

# Feature engineering
df['tenure_years'] = df['tenure'] / 12
df['total_charges_log'] = np.log1p(df['total_charges'])

# Encode categorical
le = LabelEncoder()
df['gender'] = le.fit_transform(df['gender'])

# Prepare
X = df.drop('churn', axis=1)
y = df['churn']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Scale
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)

# Train
model = XGBClassifier(n_estimators=100, max_depth=6)
model.fit(X_train_scaled, y_train, eval_metric='logloss')

# Evaluate
y_pred_proba = model.predict_proba(X_test_scaled)[:, 1]
auc = roc_auc_score(y_test, y_pred_proba)
print(f"ROC-AUC: {auc:.4f}")
```

## Practice Projects

1. **Predictive Analytics**
   - House price prediction
   - Customer churn prediction
   - Stock price forecasting

2. **NLP Applications**
   - Sentiment analysis
   - Text classification
   - Chatbot with RAG

3. **Computer Vision**
   - Image classification
   - Object detection
   - Facial recognition

4. **Data Warehouse**
   - ETL pipeline
   - Data quality monitoring
   - BI dashboards

## Resources

- **11+ Data & AI Roadmaps** - ML, Data Engineering, AI Engineering, etc.
- **180+ Content Modules** - Theory and practical implementation
- **Python Ecosystem** - NumPy, Pandas, Scikit-learn, TensorFlow, PyTorch
- **Data Pipelines** - Airflow, Spark, Kafka guides
- **LLM Resources** - Prompt engineering, fine-tuning, RAG systems
- **Competition Datasets** - Kaggle competitions and solutions

## Assessment Criteria

You've mastered this skill when you can:

✓ Build complete ML pipelines from data to deployment
✓ Perform advanced feature engineering
✓ Tune hyperparameters systematically
✓ Implement deep learning models
✓ Design and build data pipelines
✓ Deploy and monitor models in production
✓ Apply prompt engineering for LLMs
✓ Handle data at scale
✓ Optimize model performance and resource usage
