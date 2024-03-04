# State-of-health-estimation-for-fast-charging-Dataset

**<u>Raw Dataset</u>**
Dataset Source: https://data.matr.io/1/projects/5d80e633f405260001c0b60a

The dataset involves lithium-ion phosphate/graphite cells cycled under
extreme fast-charging conditions for a study on closed-loop
optimization. It includes 224 fast-charging protocols for A123 Systems'
APR18650M1A cells. The data is divided into five batches, with the first
four used for testing and the fifth for validation. Temperature data is
available for the validation batch, and internal resistance measurements
were taken during charging. The dataset is structured in MATLAB structs,
accessible in both MATLAB and Python, with CSV files containing raw data
for each cell. Some variations and challenges in temperature
measurements are acknowledged in the dataset.

**<u>After Processing, Used Features of Machine learning
prediction</u>**

The provided battery dataset consists of various parameters related to
battery performance and cycling. Each entry in the dataset corresponds
to a specific measurement or feature. Here is a summary of the dataset
along with metadata:

IR (Internal Resistance):

QC (Charge Capacity):

QD (Discharge Capacity):

Tavg (Average Temperature):

Tmin (Minimum Temperature):

Tmax (Maximum Temperature):

chargetime (Charge Time):

cycle (Cycle Number):

SOH (State of Health):

**<u>Machine Learning Data Preparation</u>**

The dataset includes features such as Internal Resistance (IR), Charge
Capacity (QC), Discharge Capacity (QD), Average Temperature (Tavg),
Minimum Temperature (Tmin), Maximum Temperature (Tmax), Charge Time
(chargetime), and Cycle Number (cycle). The target variable for
prediction is the SOH.

Here's a summary of the results and key observations:

**Linear Regression:**

Mean Squared Error: 0.1039

R-squared: 0.9945

**Decision Tree Regressor:**

Mean Squared Error: 0.0177

R-squared: 0.9991

**Random Forest Regressor:**

Mean Squared Error: 0.0023

R-squared: 0.9999

**Support Vector Regressor (SVR):**

Mean Squared Error: 10.8014

R-squared: 0.4322

**Gradient Boosting Regressor:**

Mean Squared Error: 0.0310

R-squared: 0.9984

**Bagging with Random Forest:**

Mean Squared Error: 0.0053

R-squared: 0.9997

**Boosting with AdaBoost:**

Mean Squared Error: 1.0612

R-squared: 0.9442

**8. Deep Learning (Neural Network):**

Mean Squared Error: 0.0038

R-squared: 0.9998

Linear Regression, Decision Tree, Random Forest, Gradient Boosting, and
Bagging with Random Forest exhibit high accuracy, with R-squared values
close to 1.

Support Vector Regressor (SVR) shows comparatively lower accuracy.

The ensemble methods (Random Forest, Bagging, and AdaBoost) perform
exceptionally well, with R-squared values approaching 1.

The performance summary is visualized in a bar plot, indicating that
Linear Regression, Decision Tree, Random Forest, Gradient Boosting, and
Bagging with Random Forest are suitable models for predicting battery
SOH based on the given features.
