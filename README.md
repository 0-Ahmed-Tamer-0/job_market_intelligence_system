# Job Market Intelligence System

An end-to-end AI system that predicts job salary ranges and provides intelligent career insights using machine learning, deep learning, and LLM integration.

## Overview

This project builds a comprehensive intelligent system that leverages the Stack Overflow 2023 Developer Survey data to predict developer salaries and provide AI-powered career advice. The system combines predictive modeling with a retrieval-augmented generation (RAG) pipeline for knowledge-based Q&A.

**Real-World Application:** Job seekers and HR teams can use this system to understand salary expectations, identify required skills, and explore market trends through both predictions and natural language interaction.

## Key Features

### 🎯 Salary Prediction System
- **Multi-Model Approach**: XGBoost, Random Forest, and Logistic Regression classifiers
- **Target Variable**: Annual compensation across 89,184+ developer surveys
- **Predictive Features**: 
  - Geographic location (Country - 185 unique countries)
  - Experience level (Years of coding, professional experience)
  - Education level (8 education categories)
  - Technical expertise (programming languages, databases, tools)
  - Employment type and organization size
  - Remote work arrangement

### 🧠 Deep Learning Pipeline
- **Neural Network Architecture**: Multi-layer perceptron (MLP) for pattern recognition
- **Input Features**: 15 carefully selected predictors with minimal missing data
- **Optimization**: Early stopping, learning rate reduction, model checkpointing
- **Framework**: TensorFlow/Keras with regularization techniques

### 🤖 LLM Integration & RAG Pipeline
- **LLM Service**: Groq API for fast inference
- **Vector Embeddings**: Sentence Transformers for semantic understanding
- **Vector Database**: FAISS for efficient similarity search
- **Capability**: Answer career-related questions based on survey data insights

### 📊 Interactive User Interface
- **Framework**: Gradio for easy-to-use web interface
- **Features**: Salary prediction input form, career Q&A interface
- **Real-time**: Live predictions and instant career advice generation

## Technical Stack

### Data Processing & Analysis
- **NumPy & Pandas**: Data manipulation and preprocessing
- **Scikit-learn**: ML preprocessing (LabelEncoder, StandardScaler)

### Machine Learning
- **XGBoost**: Gradient boosting classifier
- **Scikit-learn**: Random Forest, Logistic Regression
- **Evaluation Metrics**: Accuracy, Classification reports, ROC-AUC, Confusion matrices

### Deep Learning
- **TensorFlow/Keras**: Sequential neural networks with advanced callbacks
- **Regularization**: L1/L2 regularization, dropout support

### LLM & NLP
- **Groq**: Fast LLM API for inference
- **Sentence Transformers**: Semantic embeddings
- **FAISS**: Vector similarity search

### Visualization & UI
- **Matplotlib & Seaborn**: Statistical plots
- **Gradio**: Interactive web interface

## Dataset

**Source**: Stack Overflow 2023 Developer Survey (Kaggle)
- **Total Records**: 89,184 developers
- **Salary Data**: ~54,019 records with valid salary information (46.2% coverage)
- **Geographic Coverage**: 185 countries
- **Features**: 84 original features, refined to 15 key predictors

### Selected Predictors

| Feature | Missing % | Salary Variance | Importance |
|---------|-----------|-----------------|-----------|
| Country | 1.4% | 702K | Highest regional variation |
| Age | 0.0% | 88K | Experience proxy |
| Education Level | 1.4% | 92K | Qualification impact |
| Years Coding | 2.0% | 69K | Experience metric |
| Languages Known | 2.3% | 611K | Skill diversity |
| Collaboration Tools | 3.7% | 731K | Modern tech adoption |
| Dev Tools & Tech | 12.7% | 534K | Technical breadth |
| Developer Type | 13.8% | 45K | Role specialization |
| Remote Work | 17.2% | 21K | Work arrangement |
| Databases | 17.7% | 490K | Backend expertise |
| Professional Years | 25.8% | 77K | Seniority |
| Organization Size | 27.1% | 27K | Company scale |


## Installation & Setup

### 1. Clone Repository
```bash
git clone https://github.com/0-Ahmed-Tamer-0/job_market_intelligence_system.git
cd job_market_intelligence_system
```

### 2. Install Dependencies
```bash
pip install numpy pandas scikit-learn xgboost tensorflow keras
pip install groq sentence-transformers faiss-cpu
pip install gradio matplotlib seaborn
pip install kaggle  # For dataset download
```

### 3. Configure Kaggle API (Optional)
```bash
# Download Stack Overflow survey data automatically
# Set your Kaggle credentials in the notebook
```

### 4. Run the Notebook
```bash
jupyter notebook Job_Market_Intelligence_System.ipynb
```

## Usage Example

### Salary Prediction
The system predicts developer salary ranges based on:
- Country of residence
- Years of experience
- Education level
- Programming languages known
- Development tools expertise
- Remote work status

### Career Intelligence Q&A
Ask questions like:
- "What skills should I learn to increase my salary?"
- "How does remote work affect developer compensation?"
- "What's the salary expectation for [specific role] in [country]?"

## Model Performance Metrics

- **Classification Accuracy**: Evaluated across multiple salary brackets
- **Feature Importance**: Country, languages, and collaboration tools are top predictors
- **Cross-validation**: Train-test split (80/20) with stratified sampling
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-Score, ROC-AUC

## Key Insights from Analysis

1. **Geographic Impact**: Country is the strongest salary predictor (702K salary std)
2. **Tech Diversity**: Knowledge of multiple languages/tools correlates with higher compensation
3. **Experience Matters**: Both years coding and professional years significantly impact salary
4. **Education Influence**: Bachelor's degree holders dominate the dataset
5. **Remote Work Adoption**: Hybrid and remote work arrangements are prevalent

## Future Enhancements

- [ ] Real-time job market data integration
- [ ] Skill gap analysis module
- [ ] Career path recommendation engine
- [ ] Multi-language support
- [ ] API endpoint for external integrations
- [ ] Historical trend analysis
- [ ] Predictive market forecasting

## Author

**Ahmed Tamer Mohamed Ezzat**

## Acknowledgments

- Stack Overflow for the 2023 Developer Survey dataset
- Kaggle for hosting the dataset
- Groq for fast LLM inference
- Open-source community for ML frameworks and tools

---

**Note:** This project demonstrates end-to-end AI system development combining classical ML, deep learning, and modern LLM capabilities for real-world career intelligence applications.
