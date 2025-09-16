# Shopping: Customer Purchase Prediction 🛍️

This project uses a k-Nearest Neighbors (k-NN) machine learning model to predict whether an online shopper will complete a purchase based on data from their session. The goal is to analyze user behavior patterns to identify sessions that are likely to result in revenue.

**Course:** [CS50's Introduction to Artificial Intelligence with Python](https://cs50.harvard.edu/ai/2020/) - Harvard University

---

## 📝 Project Overview

The `shopping.py` script performs the following key steps:

1. **Data Loading and Preprocessing**
   - Loads a dataset of online shopping sessions from a CSV file using **pandas**
   - Converts categorical data (like months) and boolean values into numerical format suitable for machine learning

2. **Data Splitting**
   - Divides the dataset into training and testing sets using **scikit-learn**
   - Ensures unbiased assessment by training on one set and evaluating on another

3. **Model Training**
   - Trains a k-Nearest Neighbors (k-NN) classifier with `k=1`
   - Model learns to associate user session attributes with purchase likelihood

4. **Model Evaluation**
   - Makes predictions on the unseen test set
   - Measures performance using key metrics:
     - **Sensitivity (True Positive Rate):** Proportion of actual buyers correctly identified
     - **Specificity (True Negative Rate):** Proportion of non-buyers correctly identified

5. **Results**
   - Outputs total correct and incorrect predictions
   - Displays calculated sensitivity and specificity rates

---

## 🛠️ Technologies Used

- **Language:** Python 3
- **Core Libraries:**
  - [**scikit-learn**](https://scikit-learn.org/): k-Nearest Neighbors algorithm implementation and data splitting
  - [**pandas**](https://pandas.pydata.org/): Dataset loading, manipulation, and preprocessing

---

## 📊 Dataset

The project uses the `shopping.csv` dataset where each row represents one user session.

**Features include:**
- Number and duration of pages visited (`Administrative`, `Informational`, `ProductRelated`)
- `BounceRates` and `ExitRates`
- Visitor characteristics (`VisitorType`, `Region`, etc.)

**Target Variable:**
- `Revenue`: Boolean value (`TRUE`/`FALSE`) indicating if the session ended in a purchase

---

## 🚀 How to Run the Project

### Prerequisites
- Python 3
- Required libraries (pandas, scikit-learn)

### Installation & Execution

1. **Clone the repository** (if applicable)
   ```bash
   git clone <your-repository-url>
   cd <your-repository-directory>
   ```

2. **Install dependencies**
   ```bash
   pip install pandas scikit-learn
   ```

3. **Run the script**
   ```bash
   python shopping.py
   ```

### Example Output
```bash
Correct: 4354
Incorrect: 578
True Positive Rate: 41.05%
True Negative Rate: 95.34%
```

*Note: Results may vary slightly due to the random nature of the train-test split.*

---

## 🙏 Acknowledgments

This project is an assignment from **CS50's Introduction to Artificial Intelligence with Python**. The problem specification and dataset were provided by the course staff at Harvard University.
