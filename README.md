💳 Credit Card Fraud Detection

![alt text](https://img.shields.io/badge/Python-3.8%2B-blue)


![alt text](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)


![alt text](https://img.shields.io/badge/Dataset-Kaggle-blue)

📌 Project Overview

This project applies Machine Learning techniques to detect fraudulent credit card transactions. Credit card fraud costs consumers and banks billions of dollars annually. The goal of this project is to build a predictive model that can accurately identify fraudulent transactions while managing the challenges of a highly imbalanced dataset.
📊 Dataset

The dataset used for this project is the famous Credit Card Fraud Detection dataset from Kaggle.

Dataset Characteristics:

    Total Transactions: 284,807

    Fraudulent Transactions: 492

    Imbalance Ratio: Highly imbalanced (Frauds account for only 0.172% of all transactions).

    Features: 30 numeric features.

        V1 to V28 are the result of a PCA (Principal Component Analysis) transformation due to confidentiality issues.

        Time: Seconds elapsed between each transaction and the first transaction.

        Amount: Transaction amount.

        Class: Target variable (1 for Fraud, 0 for Legitimate).

🛠️ Technologies Used

    Language: Python

    Data Manipulation: Pandas, NumPy

    Data Visualization: Matplotlib, Seaborn

    Machine Learning: Scikit-Learn

⚙️ Installation & Setup

    Clone the repository:
    code Bash

    git clone https://github.com/[YourUsername]/Credit-Card-Fraud-Detection.git
    cd Credit-Card-Fraud-Detection

    Create a virtual environment (optional but recommended):
    code Bash

    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`

    Install the required dependencies:
    code Bash

    pip install -r requirements.txt

    Download the dataset:
    Download creditcard.csv from Kaggle and place it in the data/ directory.

🧠 Methodology
1. Exploratory Data Analysis (EDA)

    Analyzed the distribution of the Time and Amount features.

    Visualized the extreme class imbalance (99.8% Legitimate vs. 0.2% Fraud).

2. Handling Imbalanced Data

Because standard models will overfit to the majority class in a 99.8% / 0.2% split, the data needed to be balanced prior to training.

    Under-sampling: I created a balanced dataset by randomly under-sampling the majority class (Legitimate transactions) to match the exact number of the minority class (Fraudulent transactions). This resulted in an evenly distributed 50/50 dataset for the model to learn from.

3. Modeling

    Logistic Regression: Chosen as the primary model for its efficiency and interpretability in binary classification tasks. The model was trained exclusively on the newly created undersampled dataset.

📈 Results

A Logistic Regression model was successfully trained using the undersampled dataset. The model achieved the following accuracies:

    Training Data Accuracy: 93.90%

    Test Data Accuracy: 93.91%

Conclusion:
The nearly identical training and test accuracies indicate that the model is performing exceptionally well on both seen and unseen data. There are no signs of overfitting or underfitting, suggesting a strong and reliable generalization capability for detecting credit card fraud within the balanced dataset.
📁 Project Structure
code Text

├── data/                   # Folder containing the dataset (creditcard.csv)
├── notebooks/              # Jupyter notebooks for EDA and model training
├── src/                    # Python scripts for data processing and modeling
├── README.md               # Project documentation
├── requirements.txt        # Required Python libraries

🚀 Future Improvements

    Evaluate on the Original Imbalanced Data: While the model performs beautifully on the balanced test set, a great next step is evaluating its Precision, Recall, and F1-Score on the original imbalanced data to simulate real-world transaction ratios.

    Test Additional Algorithms: Experiment with tree-based models like Random Forest or XGBoost.

    Over-sampling Techniques: Compare the current undersampling results against over-sampling methods like SMOTE.

🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.
📝 License

This project is MIT licensed.
👤 Author

Marryam Aqeel

    GitHub: https://github.com/marryamaqeel

    LinkedIn: www.linkedin.com/in/marryam-aqeel
