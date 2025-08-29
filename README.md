# **MBA 6560 - Intrusion Detection (Capstone Project)**  
  
## ***Project Overview***
*This project involves classifying network activity as either normal (0) or intrusive (1) using supervised machine learning models. Models uses various different activity attributes (Source_IP, Destination_IP, Port, Request_Type, Protocol, Payload_Size, User_Agent, Status, and Scan_Type) to detect benign or malicious activity. The dataset simulates network activity for a ficticious financial institution ("Northwood Bank"). The primary goal was to develop and evaluate models capable of detecting intrusion attempts with high accuracy, recall, and interpretability.*
  
The final deliverables include: a JupyterNotebook, executive presentation slide deck, and reproducable code via Kaggle.
  
## ***Project Workflow***
1. **Data Collection** - The Intrusion Detection Logs (Normal, Bot, Scan) was sourced online via Kaggle and contains 8,846 unique networking records.
2. **Data Cleaning & Preprocessing** - Leveraged pandas to clean data, detect missing values, and matplotlib to perform EDA. Used SMOTE to oversample the minority class prior to model implementation.
3. **Model Development** - Built Logistic Regression (full and reduced), Discriminant Analysis, Multilayer Perceptron, and Classification Tree models using Python's scikit-learn library to classify network activity as benign or malicious.
4. **Model Evaluation** - Evaluated our model's performance using metrics such as kappa score, ROC Curve/AUC score, and using a Confusion Matrix to calculate accuracy, and recall.
5. **Visualization** - Visualized our model's performance by graphing ROC Curves, Confusion Matrices, and Feature Importance.

## ***Model Insights***  
- Performance Metrics: Our best-performing models were the Logistic Regression (Full and Reduced) and Discriminant Analysis models. Both consistently achieved ≥ 95% accuracy and demonstrated strong generalization across different data splits, making them highly reliable for this classification task.
- Neural Network Performance: The Multilayer Perceptron (MLP) Neural Network also performed well, often matching or slightly trailing the accuracy of the linear models. While its performance fluctuated due to random seed partitioning and weight initialization, the model remained overall reliable and competitive.
- Tree-Based Results: The Classification Tree, despite achieving 100% training accuracy, displayed clear signs of overfitting. It relied almost exclusively on a single feature (Scan_Type_Normal) for prediction, indicating poor generalization and limited real-world applicability.

## Overall Conclusion: These findings suggest that linear classification models are particularly well-suited to this dataset, likely because of the inherent structure and separability of the feature set. While we exceeded our original goal of ≥ 85% classification accuracy, further improvement could be achieved through additional feature engineering, hyperparameter tuning, model regularization, and cross-validation to ensure robustness in broader applications.

## ***Completed Code/Project Link (Kaggle)*** 
**Kaggle Code/Project Link:** *https://www.kaggle.com/code/jackmnob/noble-capstone-6560*

## ***Original Dataset Link (Kaggle)***  
**Kaggle Link:** *https://www.kaggle.com/datasets/developerghost/intrusion-detection-logs-normal-bot-scan*
