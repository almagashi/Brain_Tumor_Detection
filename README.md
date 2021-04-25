# Brain Tumor Detection - Visualization


This project contains multiple classification models for brain tumor detection.
The data set contains images of healthy brains and tumor brains with glioma, meningioma and pituitary tumors.
The data had to be manipulated to achieve class balance by undersampling.

We first use binary classification (Each tumor vs Healthy brains), by using these methods:

* Binary classification:
  * Logistic Regression.
  * Logistic Regression + PCA
  * Support Vector Machines
                                                        

Then, we use neural networks for multiclass-classification (Tell which class a tumor belongs to).

When classifying tumors, we need the accuracy to be high, and the false positives/negatives to be low.
Thus, we observe these metrics across classifications.

Classes           | Best classification method  | Accuracy |
-------------     | -------------           | -------|
Glioma vs Healthy | Support Vector Machines | ~91% |
Meningioma vs Healthy | Support Vector Machines and Logistic Regression| ~85  |
Glioma vs Healthy | Logistic Regression | ~96%  |
Multi-class| Neural Networks - Sequential | ~65%  |

Glioma vs Healthy - False Positives/Negatives (Support Vector Machines):

![image](https://user-images.githubusercontent.com/41328970/116010690-63728a00-a5d5-11eb-9c59-995d247fcd06.png)

Meningioma vs Healthy - False Positives/Negatives (Logistic Regression/SVM - same results):

![image](https://user-images.githubusercontent.com/41328970/116010685-548bd780-a5d5-11eb-8666-f711122a4999.png)


Pituitary vs Healthy - False Positives/Negatives (Logistic Regression):

![image](https://user-images.githubusercontent.com/41328970/116010637-11316900-a5d5-11eb-9f2f-c025c27b4b96.png)
