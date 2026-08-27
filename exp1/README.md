# Deep Learning Lab – Experiment 1
## Single Layer Perceptron for Binary Classification

### 📌 Experiment Overview

This experiment implements a **Single Layer Perceptron from scratch** for binary classification.

The experiment demonstrates:
- Artificial neuron fundamentals
- Perceptron learning algorithm
- Step activation function
- Weight and bias updates
- Data preprocessing and normalization
- Model training and evaluation
- Visualization of the learning process

The implementation is done using Python and does not rely on Scikit-learn's Perceptron model for training.

---

## 🎯 Objective

The objective of this experiment is to understand the working of an artificial neuron and implement a Single Layer Perceptron from scratch for binary classification.

The experiment also analyzes the learning process using different visualizations and evaluates the model using standard classification metrics.

---

## 📊 Dataset

### Banknote Authentication Dataset

The **Banknote Authentication Dataset** from the UCI Machine Learning Repository is used.

- **Total Samples:** 1372
- **Features:** 4 numerical features
- **Classes:** 2
- **Missing Values:** None
- **Task:** Binary Classification

### Features

1. Variance
2. Skewness
3. Curtosis
4. Entropy

### Target Classes

- `0` – Authentic Banknote
- `1` – Forged Banknote

Dataset Source:

https://archive.ics.uci.edu/dataset/267/banknote+authentication

---

## ⚙️ Methodology

The experiment follows these steps:

### 1. Dataset Exploration
- Load the dataset
- Display the first five samples
- Check dataset dimensions
- Check for missing values
- Generate descriptive statistics

### 2. Exploratory Data Analysis

The following visualizations are generated:

- Feature Histograms
- Correlation Heatmap
- Variance vs Skewness Scatter Plot
- Feature Boxplots

### 3. Data Preprocessing

- Separate input features and target labels
- Normalize numerical features using `StandardScaler`
- Split the dataset into:
  - 80% Training Data
  - 20% Testing Data

### 4. Perceptron Implementation

The Perceptron is implemented from scratch with:

- Weight initialization
- Bias initialization
- Step activation function
- Forward prediction
- Perceptron learning rule
- Weight updates
- Bias updates

### 5. Model Training

The model is trained using:

- **Learning Rate:** `0.01`
- **Epochs:** `20`

During training, the following are recorded:

- Epoch number
- Number of misclassified samples
- Updated weights
- Updated bias

### 6. Model Evaluation

The trained model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

---

## 🧠 Perceptron Equation

The weighted sum is calculated as:


- z = wᵀx + b


The Step Activation Function is:

- f(z) = 1, if z >= 0
-       0, if z < 0

The weight update rule is:

- w_new = w_old + η(y - ŷ)x


The bias update rule is:

- b_new = b_old + η(y - ŷ)

## where:
- x = input vector
- w = weight vector
- b = bias
- η = learning rate
- y = actual target
- ŷ = predicted output


## 📈 Results
The model achieved the following performance on the test dataset:
| Metric    |  Score |
| --------- | -----: |
| Accuracy  | 0.9636 |
| Precision | 1.0000 |
| Recall    | 0.9213 |
| F1-Score  | 0.9590 |


## Final Model Parameters
Final Weights:
- [-0.15641765, -0.17466330, -0.15518554, -0.02596029]

Final Bias:
- -0.09

## Confusion Matrix
- [[146   2]
   [  3 124]]

## 📉 Visualizations

The experiment generates the following plots:

- Feature Histograms
- Correlation Heatmap
- Variance vs Skewness Scatter Plot
- Feature Boxplots
- Confusion Matrix
- Training Error vs Epoch
- Learning Rate Comparison
- Weight Evolution
- Bias Evolution

The training error decreases significantly during the initial epochs and then becomes relatively stable. The learning-rate comparison also shows that a learning rate of 0.01 provides a good balance between convergence speed and stability.


## 🔍 Observations
- The dataset contains four numerical features useful for distinguishing authentic and forged banknotes.
- Variance shows a strong negative correlation with the target class.
- Variance and Skewness provide noticeable separation between the two classes.
- The Perceptron performs well because the dataset is largely linearly separable.
- The model achieved an accuracy of 96.36%.
- A learning rate of 0.01 provided a good balance between convergence speed and training stability.
- The weights and bias gradually change during training as the decision boundary is learned.


## ⚠️ Limitation

- A Single Layer Perceptron can only learn linearly separable decision boundaries.
- Therefore, it cannot correctly solve non-linear problems such as the XOR problem.
- For more complex non-linear classification problems, Multilayer Perceptrons (MLPs) and deeper neural networks are required.


## 🛠️ Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google ColaB

## 📚 References
- F. Rosenblatt, The Perceptron, Psychological Review, 1958.
- Ian Goodfellow, Yoshua Bengio and Aaron Courville, Deep Learning, MIT Press, 2016.
- Christopher M. Bishop, Pattern Recognition and Machine Learning, Springer, 2006.
- Simon Haykin, Neural Networks and Learning Machines, Pearson, 2009.
- UCI Machine Learning Repository – Banknote Authentication Dataset.
- Scikit-learn Documentation – Perceptron.

## ✅ Conclusion

The Single Layer Perceptron was successfully implemented from scratch and used to classify the Banknote Authentication Dataset.
The experiment demonstrated the Perceptron Learning Rule, weight and bias updates, model convergence, and binary classification. The model achieved 96.36% accuracy, showing that the Perceptron is effective for this largely linearly separable dataset.










