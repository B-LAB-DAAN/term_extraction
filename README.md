# Equation Term Extraction Using NLP and Machine Learning

## Overview
This project applies Natural Language Processing (NLP) and Machine Learning (ML) techniques to extract mathematical equation terms from scientific abstracts.

**Implemented Models:**
- **Logistic Regression:** Classifies equation-related terms using TF-IDF.
- **Conditional Random Fields (CRF):** Recognizes term sequences based on contextual relationships.
- **Latent Dirichlet Allocation (LDA):** Groups terms into topic-based clusters for better interpretability.

The dataset consists of 100 filtered mathematical research abstracts from the ArXiv Metadata Dataset.

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/equation-term-extraction.git
cd equation-term-extraction
```
### 2. Install Dependencies
Ensure you have Python 3.8+ installed. Then, install the required libraries:

```bash
# Копировать
pip install -r requirements.txt
```
## Notebook Structure

| Section                        | Description                                                                            |
| ------------------------------ | -------------------------------------------------------------------------------------- |
| **Importing Libraries**        | Loads necessary packages (NumPy, scikit-learn, sklearn-crfsuite, etc.)                 |
| **Data Preprocessing**         | Loads mathematical abstracts and extracts relevant terms                               |
| **Feature Engineering**        | Applies TF-IDF vectorization for Logistic Regression                                   |
| **Logistic Regression Model**  | Trains and evaluates Logistic Regression                                               |
| **CRF Model**                  | Implements sequence-based extraction using CRF                                         |
| **Topic Modeling (LDA)**       | Groups extracted terms into research topics                                            |
| **Visualization**              | Generates accuracy plots and training loss curves                                        |
| **Results & Conclusion**       | Summarizes model performance and key findings                                            |

### Check Model Performance

The output will display accuracy, precision, recall, and F1-score for each model.

### Model Performance Table

| Model                   | Accuracy | Precision | Recall  | F1-score |
| ----------------------- | -------- | --------- | ------- | -------- |
| Logistic Regression     | 98.00%   | 0.9800    | 1.0000  | 0.9897   |
| CRF Model               | 97.10%   | 0.9735    | 0.9727  | 0.9593   |

- **Logistic Regression** performed best in classification-based term extraction.
- **CRF Model** was effective in context-based sequence recognition.
- **LDA** provided interpretability but lacked precision for direct term extraction.
## Visualization Samples

**Training vs Validation Loss (Logistic Regression):**

![Training vs Validation Loss]![image](https://github.com/user-attachments/assets/7b533c40-394d-4c54-aeaa-b5a63e47e064)


**Actual vs Predicted Accuracy (CRF Model):**

![Actual vs Predicted Accuracy]![image](https://github.com/user-attachments/assets/e3240c70-2c12-4219-9515-4cb64ecb9a13)


**Top Words from LDA Topic Modeling:**

- **Topic 1:** ['triangular', 'velocity', 'subsets', 'projection', 'dimensional']
- **Topic 2:** ['parameters', 'polytope', 'convex', 'curvature', 'cubes']
- **Topic 3:** ['symbols', 'parameters', 'eigenforms', 'eigenvalues', 'spectra']
- **Topic 4:** ['classification', 'surface', 'integer', 'automorphisms', 'complexity']
- **Topic 5:** ['correspondence', 'inverse', 'vertex', 'symmetric', 'gradient']
- **Topic 6:** ['coordinates', 'polytope', 'quasisymmetric', 'coordinatizations', 'grassmannian']
- **Topic 7:** ['symbols', 'integrator', 'quantum', 'algebra', 'exponential']
- **Topic 8:** ['algorithms', 'euclidean', 'frobenius', 'quantization', 'distribution']
- **Topic 9:** ['planar', 'accuracy', 'consensus', 'cohomology', 'polynomial']
- **Topic 10:** ['metric', 'area', 'digraph', 'interval', 'sphere']

