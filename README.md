# Detecting anomalous activities of ship engines
This project's objectives were to develop an anomaly detection system to protect a company’s shipping fleet by evaluating engine functionality, ensuring early identification & malfucntion prevention.

## 🔻Data
The dataset used in this project consists of 19535 rows and 6 columns, earch representing different engines and their vital metrics including - 
Engine RPM, Lubricant oil pressure, Lubricant oil temperature, Fuel pressure, Coolant pressure & Coolant temperature. 

The dataset can be found here: [dataset](https://ieee-dataport.org/open-access/predictive-maintenance-ships-main-engine-using-ai)

## 🔻Methodology
* Performed inital data exploration and preprocessing.
* Applied the **interquartile range (IQR)** method to identify outliers for each feature. Extracted the final sample of outlier where only two or more of the features fell under an outlier category.
* Instantiated and ran the **OneClassSVM** pipeline and experimented with parameter values to optimise the model's performance. 
* Applied the **Isolation forest** algorithm and tested different combinations of parameter settings to improve the model's outlier predictions.
* Performed dimensionality reduction on the data using Principle component analysis (PCA) to enable simpler and more intuitive data visualisation.
* Compared the outputs of the two ML methods.

## 🔻Tools
* Python, Numpy, Pandas, SciPy Stats
* MatPlotLib, Seaborn
* SciKitLearn (OneClassSVM, Isolation Forest & PCA)

## 🔻Results & Findings
* Both optimised machine learning methods were able to indentify the expected range of anomalies (1-5%).
* While the IQR method, when combined with a rule, produced results within the expected range, the multivariate machine learning methods (SVM and Isolation Forest) were more comprehensive in identifying anomalies by considering the relationships between features.
* The identified anomalies can serve as a basis for further investigation by qualified engineers and service personnel to determine the root cause and necessary maintenance.
