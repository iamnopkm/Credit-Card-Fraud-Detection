# Credit-Card-Fraud-Detection

## Introdduction

<h1 align='center'>Abtraction</h1>
<p>
Credit card fraud poses a significant challenge for financial institutions, with
detrimental effects on both customers and businesses. Fraudulent transactions can occur due to
various factors, including unauthorized access, compromised card information, or sophisticated
cyber-attacks. Detecting fraudulent activity is crucial to safeguarding financial systems and
maintaining customer trust. Establishing robust methods to classify credit card transactions as
either legitimate or fraudulent is imperative. Utilizing Machine Learning algorithms, this
research aims to identify key features within a credit card transaction dataset that impact fraud
classification. By developing a fraud prediction framework, this study seeks to enhance the
effectiveness of fraud detection in the financial sector, ultimately contributing to the security
and integrity of electronic payment systems.
</p>

<h1 align='center'>About Dataset</h1>
<p>The dataset at hand encapsulates a simulated chronicle of credit card transactions, spanning the duration from January 1, 2019, to December 31, 2020.</p>
<p>It has 21 features and over 1.2 million rows of transaction data.</p>
<p>The transactions involve 1000 simulated customers and 800 merchants.</p>
<p>The dataset includes both legitimate transactions and simulated fraudulent activities.</p>
<hr>
<p>You can download the dataset at <a href='https://www.kaggle.com/code/islamashraaf/credit-card-fraud-detection/input'>HERE</a></p>

## Objective
<p>Note: The code origin was from <a href='https://www.kaggle.com/code/islamashraaf/credit-card-fraud-detection/input'>kaggle</a> but we had implement and modify it.</p>
<ul>
  <li>
    Implement advanced anomaly detection techniques to identify subtle patterns
indicative of potential credit card fraud, contributing to the continuous
improvement of fraud detection capabilities.
  </li>
  <li>
    Investigate and incorporate innovative features or data sources that can provide
additional insights into the evolving tactics of fraudsters, thereby staying ahead
of emerging fraud patterns in credit card transactions.
  </li>
  <li>
    Optimize model interpretability and explainability to provide actionable insights
for fraud analysts and investigators, facilitating a more transparent and
understandable fraud detection process in credit card transactions.
  </li>
</ul>

## Model Building and Evaluation
<hr>
<p>Experimental protocols</p>

![image](https://github.com/iamnopkm/Credit-Card-Fraud-Detection/blob/main/PaperResources/protocol.png)

<hr>
<p>A conceptual model for the prediction of potential fraud transactions</p>

![image](https://github.com/iamnopkm/Credit-Card-Fraud-Detection/blob/main/PaperResources/conceptual_model_for_prediction.png)

<hr>
<table>
    <tr>
        <th>Algorithm</th>
        <th>Description</th>
        <th>Reason for choosing</th>
    </tr>
    <tr>
        <th>Logistic Regression</th>
        <td style="text-align: center;">Logistic regression is used for
classification and predictive analytics.
Logistic regression predicts a dependent
data variable by analyzing the
relationship between one or more
existing given dataset of independent
variables. And the outcome is predicted
as binary outcome</td>
        <td style="text-align: center;">Logistic Regression provides
probabilistic outputs, enabling a
nuanced understanding of
prediction confidence, and is
particularly effective when dealing
with linearly separable data. It
serves as an efficient baseline
model, offering insights into feature
importance and being easily
interpretable, making it an excellent
option for scenarios where a clear
understanding of predictive factors
is crucial.
</td>
    </tr>
    <tr>
        <th>P-values</th>
        <td style="text-align: center;">P - value is calculated to validate a
hypothesis on a dataset.In this study,
p-value is used to determine whether a
dataset feature has a significant impact
on the output value. The lower p-value is,
the more significant the features could be
(Gelman, 2013)
<br>● p > 0.10 → “not significant”
<br>● p ≤ 0.10 → “marginally
significant”
<br>● p ≤ 0.05 → “significant”
<br>● p ≤ 0.01 → “highly significant”
</td>
        <td style="text-align: center;">P - values play a pivotal role in
statistical hypothesis testing,
quantifying evidence against a null
hypothesis and aiding
decision-making. They indicate
whether observed results are likely
due to chance, ensuring statistical
significance in research findings.
P-values contribute to the
replicability of studies, offer a standardized communication
method for evidence strength, and
help control Type I error rates.
Caution in interpretation and
consideration alongside effect sizes
enhance the reliability of research
conclusions.
</td>
    </tr>
  <tr>
    <th>SMOTE</th>
    <td style="text-align: center;">SMOTE is used for synthetic minority
oversampling in machine learning. It
generates synthetic samples to balance
imbalanced datasets, specifically
targeting the minority class.
SMOTE should be used when dealing
with imbalanced datasets to improve the
performance of machine learning models
on minority class predictions.
</td>
    <td style="text-align: center;">SMOTE prevents biases towards
the majority class, enhances model
performance on the minority class,
and is applicable across various
machine learning algorithms. It is
particularly valuable in domains
with imbalanced classes, such as
fraud detection or rare event
prediction, ensuring robust model
performance and effective handling
of critical instances.</td>
  </tr>
  <tr>
    <th>Decision Tree</th>
    <td style="text-align: center;">A decision tree is a machine learning
algorithm that uses a tree-like model for
decision-making. It recursively splits data
based on optimal conditions, leading to
simple and interpretable outcomes.
Despite their interpretability, decision
trees can be prone to overfitting
mitigated through techniques like
pruning.
</td>
    <td style="text-align: center;">Decision trees are prized for their
simplicity, interpretability, and
adaptability. They efficiently handle
diverse datasets, both numerical and
categorical, without intricate
preprocessing. Their visual clarity
aids in easy comprehension and
explanation, making them ideal for
transparent decision-making.
Notably versatile, decision trees
excel in capturing complex patterns
and are foundational in ensemble
methods like Random Forests,
ensuring robust performance across various tasks.</td>
  </tr>
  <tr>
    <th>Random Forest</th>
    <td style="text-align: center;">Random forest is the use of multiple
classifier models for classifying the same
data set, all the outcomes are combined
to generate a single result. By following
the large number principle, a random
forest classifier is considered to reduce
the error and give better performance,
compared to a single classifier.</td>
    <td style="text-align: center;">Random Forests stand out for their
accuracy and adaptability in
machine learning. By combining
multiple decision trees, they deliver
robust predictions, handling outliers
and diverse data effortlessly.
Versatile across classification and
regression tasks, Random Forests
provide reliable results with
automatic feature importance
assessment. Their reduced
overfitting, efficient handling of
missing data, and ease of use make
them a powerful and accessible
ensemble learning technique for a
wide range of applications.</td>
  </tr>
  <tr>
    <th>Area Under The Curve (AUC)</th>
    <td style="text-align: center;">Area under the curve or area under the
receiver operating characteristics is an
evaluation metric used for measuring a
classification model performance. The
curve is plotted by the true positive rate
as y-axis and the false positive rate as x
axis. The higher AUC, the better the
model.
</td>
    <td style="text-align: center;">AUC is a key metric in machine learning, offering a holistic assessment of a model's discriminative performance across various thresholds. Its threshold independence, insensitivity to class imbalance, and applicability to diverse scenarios make it invaluable. A higher AUC signifies superior performance, aiding in straightforward model comparison. With resilience to noise and suitability for both binary and multiclass scenarios, AUC provides a concise and effective measure for evaluating model performance.</td>
  </tr>
  <tr>
    <th>Confusion Matrix</th>
    <td style="text-align: center;">A confusion matrix represents the
prediction summary in matrix form. It
shows how many predictions are correct
and incorrect per class. It helps in
understanding the classes that are being
confused by models as other classes.
</td>
    <td style="text-align: center;">Confusion matrices are crucial in
machine learning for a detailed
performance breakdown,
facilitating the calculation of key
metrics like precision and recall.
They aid in threshold adjustment,
making informed decisions about
model tuning, and are essential for
handling class imbalances. With a
clear visual representation,
confusion matrices serve as a
fundamental tool for evaluating and
optimizing machine learning
models.
</td>
</table>

## Final Result
<p align='center'>Evaluation metrics before applying SMOTE</p>

|                    | Logistic Regression | Random Forest | Decision Tree |
|--------------------|---------------------|---------------|---------------|
| Recall Score       | 0.1916              | 0.6988        | 0.77948       |
| Precision          | 0.8253              | 0.972         | 0.72632       |
| F1-Score           | 0.311               | 0.813         | 0.75196       |
| Accuracy Score     | 0.9967              | 0.998         | 0.99801       |
| AUC Score          | 0.8631              | 0.978         | 0.89917       |
| Running Time (mins)| 0.19                | 5.5           | 0.23          |
                  
<hr>
<p align='center'>Evaluation metrics after applying SMOTE</p>

|                    | Logistic Regression | Random Forest | Decision Tree |
|--------------------|---------------------|---------------|---------------|
| Recall Score       | 0.7557              | 0.7678        | 0.80986       |
| Precision          | 0.0259              | 0.8912        | 0.61275       |
| F1-Score           | 0.0501              | 0.8249        | 0.69466       |
| Accuracy Score     | 0.8094              | 0.9987        | 0.99727       |
| AUC Score          | 0.8749              | 0.9901        | 0.89995       |
| Running Time (mins)| 0.92                | 22.05         | 1.15          |

## Authors
I'm Hồ Quang Anh aka iamnopkm this brief introduc abou this project was make by me but the process of getting this result is made buy us the contributors:

Name                 |    School ID    |       
-------------------- |-----------------|
Hồ Quang Anh         | BI12-017 | 
Trần Đức Anh         | BI12-018 | 
Lê Ngọc Phan Anh     | BI12-010 | 
Trần Ngọc Ánh        | BI12-040 | 
Hoàng Minh Đức       | BI12-093 |
Lê Nhật Minh         | BI12-289 |
Nguyễn Hoàng Nam     | BI12-308 |







