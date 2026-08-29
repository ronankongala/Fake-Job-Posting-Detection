# Fake Job Posting Detection

## 📄 IEEE Publication
**Published at IEEE ICAISS 2025** - 3rd International Conference on Augmented Intelligence and Sustainable Systems
- 📖 [Read the Full Paper](IEEE%20paper%20pdf.pdf)
- 🏆 [Conference Certificate](IEEE%20certificate.pdf)
- 📍 Presented at CARE College of Engineering, Trichy, India (May 21-23, 2025)

## 🎯 Project Overview
Detection of fraudulent job postings using Machine Learning and Natural Language Processing. This research addresses the critical challenge of identifying fake job advertisements in online recruitment platforms, achieving **85% accuracy** through ensemble methods and advanced data balancing techniques.

## 📊 Key Results

### Model Performance Comparison
| Algorithm | Accuracy | Recall (Fake) | F1-Score (Fake) |
|-----------|----------|---------------|-----------------|
| Random Forest + SMOTE | 98% | 68% | 0.80 |
| Gradient Boosting | 97% | 97% | 0.73 |
| XGBoost | 97% | 77% | 0.70 |
| AdaBoost | 96% | 80% | 0.68 |

### Key Achievements
- ✅ Successfully handled class imbalance using SMOTE and ADASYN
- ✅ Compared 4 ensemble learning algorithms
- ✅ Processed 9,000+ job postings
- ✅ Published peer-reviewed research paper

## 🛠️ Technologies & Methods

### Machine Learning Algorithms
- Random Forest
- AdaBoost
- Gradient Boosting
- XGBoost

### Data Balancing Techniques
- SMOTE (Synthetic Minority Over-sampling Technique)
- ADASYN (Adaptive Synthetic Sampling)

### Natural Language Processing
- TF-IDF (Term Frequency-Inverse Document Frequency)
- Text preprocessing and feature extraction

### Tools & Libraries
- Python 3.x
- Scikit-learn
- Pandas & NumPy
- Matplotlib & Seaborn
- Imbalanced-learn

## 📁 Repository Structure
├── IEEE paper pdf.pdf          # Published research paper
├── IEEE certificate.pdf        # Conference presentation certificate
├── fake_job_postings.csv.zip  # Dataset (EMSCAD)
├── presntation.ipynb          # Implementation notebook
├── outputs compared.docx      # Performance comparison document
└── README.md                  # Project documentation

## 🚀 Getting Started

## Prerequisites
```bash
pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn
Running the Project

Clone the repository

bashgit clone https://github.com/ronankongala/Fake-Job-Posting-Detection.git

Extract the dataset

bashunzip fake_job_postings.csv.zip

Run the Jupyter notebook

bashjupyter notebook presntation.ipynb
📈 Methodology

Data Preprocessing: Cleaned and prepared EMSCAD dataset with 9,000+ job postings
Feature Engineering: Applied TF-IDF for text feature extraction from job descriptions
Class Balancing: Implemented SMOTE and ADASYN to address dataset imbalance
Model Training: Trained and optimized multiple ensemble classifiers
Evaluation: Assessed using accuracy, precision, recall, and F1-score metrics


🔮 Future Enhancements

Real-time API for job posting verification
Integration with LinkedIn, Indeed, and other platforms
Deep learning implementation using BERT
Browser extension for automatic fake job detection

📫 Contact
For questions or collaboration: kongalaronan@gmail.com

Supported by Vardhaman College of Engineering & Northeastern University
