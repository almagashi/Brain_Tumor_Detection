# Brain Tumor Detection - Visualization

To learn more about tumors, please check the _Brain_Tumor.pdf_ file, where I analyze holistically the neuroscience behind tumors.

This project contains multiple classification models for brain tumor detection.
The data set contains images of healthy brains and tumor brains with glioma, meningioma and pituitary tumors.

![image](https://user-images.githubusercontent.com/41328970/116011333-4d66c880-a5d9-11eb-8085-9d768764a205.png)

# Data Manipulation and Algorithms
The data had to be manipulated to achieve class balance by undersampling.

To avoid overfitting, I used cross-validation in binary classification, and modified the layers in the neural network; as well as augmented the images with ImageGenerator.

![image](https://user-images.githubusercontent.com/41328970/116011368-7dae6700-a5d9-11eb-9f47-e2bcde8d7a9b.png)


We first use binary classification (Each tumor vs Healthy brains), by using these methods:

* Binary classification:
  * Logistic Regression.
  * Logistic Regression + PCA
  * Support Vector Machines
                                                        

Then, we use neural networks for multiclass-classification (Tell which class a tumor belongs to).

# Metrics of performance

When classifying tumors, we need the accuracy to be high, and the false positives/negatives to be low.
Thus, we observe these metrics across classifications.

Classes           | Best classification method  | Accuracy |
-------------     | -------------           | -------|
Glioma vs Healthy | Support Vector Machines | ~91% |
Meningioma vs Healthy | Support Vector Machines and Logistic Regression| ~85  |
Glioma vs Healthy | Logistic Regression | ~96%  |
Multi-class| Neural Networks - Sequential | ~65%  |

While the multi-class classification requires more intervention to classify better, we see that logistic regression and support vector machines tend to do best at classifying. The rates of false positives is more prevalent than false negatives, which in the context of tumors, it is better than the other way around. However, both false negatives and positives are detrimental for people with tumors. Let's take a look at all these False Positives/False Negatives.

Glioma vs Healthy - False Positives/Negatives (Support Vector Machines):

![image](https://user-images.githubusercontent.com/41328970/116010690-63728a00-a5d5-11eb-9c59-995d247fcd06.png)

Meningioma vs Healthy - False Positives/Negatives (Logistic Regression/SVM - same results):

![image](https://user-images.githubusercontent.com/41328970/116010685-548bd780-a5d5-11eb-8666-f711122a4999.png)


Pituitary vs Healthy - False Positives/Negatives (Logistic Regression):

![image](https://user-images.githubusercontent.com/41328970/116010637-11316900-a5d5-11eb-9f2f-c025c27b4b96.png)

