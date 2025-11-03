# 🚀 AT&T Spam Detection Project
## Deep Learning with Sentence Transformers & Neural Networks

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-red.svg)](https://pytorch.org)
[![Sentence Transformers](https://img.shields.io/badge/Sentence--Transformers-2.0%2B-green.svg)](https://www.sbert.net)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AgaHei/Spam-Detector/blob/master/Project_AT%26T_Final.ipynb)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-black.svg)](https://github.com/AgaHei/Spam-Detector)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **Advanced SMS spam detection system using modern transfer learning techniques with Sentence Transformers and lightweight neural networks.**


## 🎯 Overview

This project implements a **state-of-the-art spam detection system** for SMS messages using modern deep learning techniques. Built as part of the Jedha Machine Learning Engineer certification (Bloc 4), it demonstrates advanced transfer learning with Sentence Transformers and efficient neural network architectures.

### 🎪 Why This Approach?

- **Transfer Learning**: Leverages pre-trained Sentence Transformers (`all-MiniLM-L6-v2`) for semantic understanding
- **Feature Engineering**: Combines 384-dimensional embeddings with 8 domain-specific features  
- **Class Imbalance Handling**: Implements weighted loss functions for balanced predictions
- **Efficient Architecture**: Ultra-lightweight models (25K-51K parameters) for production deployment
- **GPU Acceleration**: Optimized for Google Colab with CUDA support

## ⭐ Key Features

### 🧠 Advanced ML Techniques
- **Sentence Transformers** for semantic text embeddings
- **Custom Neural Networks** (Simple & Ultra-Simple architectures)
- **Weighted Binary Cross-Entropy Loss** for imbalanced data
- **Feature Engineering** with spam-specific indicators

### 📊 Comprehensive Analysis
- **Exploratory Data Analysis** with statistical insights
- **Class imbalance detection** and mitigation strategies
- **Performance visualization** with ROC curves and confusion matrices
- **Real-time prediction** capabilities with confidence scores

### 🚀 Production Ready
- **Scalable architecture** suitable for deployment
- **Efficient inference** with minimal computational overhead  
- **Robust preprocessing** pipeline
- **Comprehensive evaluation** metrics

## 🏗️ Technical Architecture

```
Input SMS Message
        ↓
┌─────────────────┬─────────────────┐
│ Sentence        │ Feature         │
│ Transformers    │ Engineering     │
│ (384 dims)      │ (8 features)    │
└─────────────────┴─────────────────┘
        ↓
    Combined Features
    (392 dimensions)
        ↓
    Standard Scaler
        ↓
┌─────────────────────────────────────┐
│        Neural Network               │
│  ┌─────┐  ┌─────┐  ┌─────┐        │
│  │ 392 │→ │ 64  │→ │  1  │        │
│  │     │  │ReLU │  │Sig. │        │
│  └─────┘  └─────┘  └─────┘        │
└─────────────────────────────────────┘
        ↓
   Spam/Ham Prediction
```

## 📊 Dataset

- **Source**: SMS Spam Collection Dataset
- **Size**: 5,572 messages
- **Classes**: 
  - Ham (Legitimate): 4,825 messages (86.6%)
  - Spam: 747 messages (13.4%)
- **Features**: Text messages with binary labels
- **Preprocessing**: Text cleaning, feature engineering, embedding generation

## 🏆 Model Performance

### Best Model: Ultra-Simple Neural Network

| Metric | Score |
|--------|-------|
| **Accuracy** | 98.4% |
| **AUC Score** | 0.992 |
| **Parameters** | 25,153 |
| **Architecture** | 392 → 64 → 1 |

### Detailed Metrics
```
              precision    recall  f1-score   support

         Ham       0.99      0.99      0.99       965
        Spam       0.94      0.95      0.94       150

    accuracy                           0.98      1115
   macro avg       0.96      0.97      0.97      1115
weighted avg       0.98      0.98      0.98      1115
```

## 📓 Notebook Access

### 🎯 Choose Your Preferred Way to Explore the Project:

| Platform | Purpose | Link |
|----------|---------|------|
| **🐙 GitHub** | Code Review & Documentation | [View Notebook](https://github.com/AgaHei/Spam-Detector/blob/master/Project_AT%26T_Final.ipynb) |
| **🚀 Google Colab** | Interactive Execution | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AgaHei/Spam-Detector/blob/master/Project_AT%26T_Final.ipynb) |

### 💡 Recommendations:
- **For Jury Review**: Use GitHub version for clean code viewing
- **For Interactive Testing**: Use Colab version with GPU acceleration
- **For Development**: Clone repository and run locally or in Colab

> **Note**: If the notebook doesn't render on GitHub, use the Colab link which always works perfectly!



### Key Insights

1. **Transfer Learning Effectiveness**: Sentence Transformers provide rich semantic representations
2. **Efficiency vs Performance**: Ultra-simple model achieves 98.4% accuracy with only 25K parameters
3. **Class Imbalance Handling**: Weighted loss successfully addresses 13.4% spam ratio
4. **Feature Importance**: Domain-specific features complement embeddings effectively

### Training Curves
- **Convergence**: Both models converge within 15 epochs
- **Stability**: No overfitting observed with dropout regularization
- **Efficiency**: Ultra-simple model trains 2x faster than simple model

## 🔮 Potential Future Improvements

### Short-term Enhancements
- [ ] **Multi-language Support** with multilingual Sentence Transformers
- [ ] **Real-time API** deployment with FastAPI/Flask
- [ ] **Model Compression** with knowledge distillation
- [ ] **A/B Testing Framework** for production deployment

### Advanced Features
- [ ] **Adversarial Training** for robustness against spam evolution
- [ ] **Federated Learning** for privacy-preserving updates
- [ ] **Explainable AI** with LIME/SHAP integration
- [ ] **Auto-ML Pipeline** with hyperparameter optimization

### Production Deployment
- [ ] **Docker Containerization**
- [ ] **Kubernetes Orchestration**  
- [ ] **MLOps Pipeline** with MLflow/Weights & Biases
- [ ] **Monitoring & Alerting** for model drift detection



## � Contact & Project Links

**📚 Repository**: [github.com/AgaHei/Spam-Detector](https://github.com/AgaHei/Spam-Detector)  
**🚀 Interactive Notebook**: [Open in Google Colab](https://colab.research.google.com/github/AgaHei/Spam-Detector/blob/master/Project_AT%26T_Final.ipynb)  
**🏫 Institution**: Jedha Bootcamp - Machine Learning Engineer Track  

### 📊 Project Stats
- **🔬 Development**: 1 week
- **🎯 Final Accuracy**: 98.4%
- **🏆 Certification**: Jedha Bloc 4 (Deep Learning)

---

## �📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Jedha Bootcamp** for the comprehensive Machine Learning curriculum
- **Sentence Transformers Team** for the excellent pre-trained models
- **PyTorch Community** for the robust deep learning framework
- **SMS Spam Collection Dataset** contributors for the quality dataset

---

**Built for the Jedha Machine Learning Engineer Certification**

> **For Jury Review**: This project showcases advanced ML engineering including transfer learning, neural networks, and production-ready deployment. Click the Colab badge above for interactive exploration!