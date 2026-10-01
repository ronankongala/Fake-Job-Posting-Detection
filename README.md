# Fake Job Posting Detection

## IEEE Publication
Published at **IEEE ICAISS 2025**, the 3rd International Conference on Augmented Intelligence and Sustainable Systems, and presented at CARE College of Engineering, Trichy, India (May 21 to 23, 2025).
- [Read the paper](IEEE%20paper%20pdf.pdf)
- [Conference certificate](IEEE%20certificate.pdf)

## Project Overview
Classifies job postings as real or fake using TF-IDF features and four ensemble models, with SMOTE/ADASYN for the roughly 5% fake class. The dataset is EMSCAD: 17,880 postings, 866 of them fraudulent. The best model, Random Forest trained on SMOTE-balanced data, reaches 98% accuracy on the held-out test set (3,576 postings) and catches 68% of the fake ones.

## Results

| Algorithm | Accuracy | Recall (Fake) | F1-Score (Fake) |
|-----------|----------|---------------|-----------------|
| Random Forest + SMOTE | 98% | 68% | 0.80 |
| Gradient Boosting | 97% | 79% | 0.73 |
| XGBoost | 97% | 77% | 0.70 |
| AdaBoost | 96% | 80% | 0.68 |

Accuracy is high for every model because 95% of postings are real, so recall and F1 on the fake class are the more useful comparison. The boosting models trade precision for recall: AdaBoost finds the most fake postings but flags more real ones by mistake.

## Methods and Tools
Models are Random Forest, AdaBoost, Gradient Boosting and XGBoost, with SMOTE and ADASYN for class balancing and TF-IDF over the cleaned, lemmatized posting text. The code is Python 3 with scikit-learn, imbalanced-learn, XGBoost, Pandas, NumPy, Matplotlib and Seaborn.

## Repository Structure
```
├── IEEE paper pdf.pdf          # Published research paper
├── IEEE certificate.pdf        # Conference presentation certificate
├── fake_job_postings.csv.zip   # Dataset (EMSCAD)
├── presntation.ipynb           # Implementation notebook
├── outputs compared.docx       # Performance comparison document
└── README.md                   # Project documentation
```

## Getting Started

### Prerequisites
```bash
pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn
```

### Running the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/ronankongala/Fake-Job-Posting-Detection.git
   ```
2. Extract the dataset:
   ```bash
   unzip fake_job_postings.csv.zip
   ```
3. Open the [notebook](presntation.ipynb):
   ```bash
   jupyter notebook presntation.ipynb
   ```

## Methodology
1. Preprocessing: location and salary range were split into separate fields, the text columns were joined into one `full_text` field, and that text was lowercased, stripped of stopwords and lemmatized.
2. Feature extraction: TF-IDF over `full_text`.
3. Class balancing: SMOTE and ADASYN applied to the training split only.
4. Training: each ensemble classifier was fit on the balanced training data.
5. Evaluation: accuracy, precision, recall and F1 on the untouched test split.

## Future Enhancements
- A real-time API for checking a posting
- A BERT-based model to compare against the TF-IDF ensembles
- A browser extension that flags postings on job sites

## Contact
For questions or collaboration: kongalaronan@gmail.com

Supported by Vardhaman College of Engineering and Northeastern University.
