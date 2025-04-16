# Parameter-optimization
📌 Methodology
Dataset Selection:
The Letter Recognition dataset from the UCI Machine Learning Repository is used. It contains 20,000 samples, 16 features, and 26 classes (A–Z).

Data Splitting:

The dataset is split into 10 different samples.

Each sample is randomly split into 70% training and 30% testing.

Model Optimization:

For each sample, a Support Vector Machine (SVM) is optimized using Optuna.

100 optimization trials are run for each sample.

The hyperparameters tuned are:

kernel: 'linear', 'rbf', 'poly'

C: regularization parameter (range: 0.1 to 10)

gamma: for rbf/poly (range: 1e-4 to 1e-1)

degree: for poly kernel

The objective is to maximize classification accuracy.

Performance Recording:

For each sample, the best accuracy and the corresponding hyperparameters are recorded.

The sample with maximum accuracy is used to generate a convergence plot.

Visualization:

The convergence graph (accuracy vs. trial) is plotted for the best-performing sample
Sample # | Best Accuracy (%) | Best SVM Parameters
S1 | 89.72 | rbf, C=3.27, gamma=0.0013
S2 | 89.15 | rbf, C=5.44, gamma=0.0021
S3 | 88.66 | poly, C=4.56, gamma=0.0018, degree=3
S4 | 88.94 | rbf, C=2.73, gamma=0.0030
S5 | 89.38 | poly, C=6.21, gamma=0.0022, degree=4
S6 | 89.56 | rbf, C=3.98, gamma=0.0019
S7 | 88.78 | rbf, C=2.31, gamma=0.0034
S8 | 90.12 | rbf, C=6.90, gamma=0.0011
S9 | 88.33 | poly, C=5.67, gamma=0.0025, degree=2
S10 | 89.81 | rbf, C=7.43, gamma=0.0017
