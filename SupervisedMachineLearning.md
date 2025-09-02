![polynomial](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/polynomial.png) <br>
![polynomial example](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/polynomial2.png) <br>
![polynomial example](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/polynomial3.png) <br>
![Non linear](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/nonlinear.png) <br>

### CLASSIFICATION
|One vs ALL strategy|One vs One strategy|
|--|--|
|**In the One-vs-All approach:** <br> + The algorithm trains a single binary classifier for each class.<br> + Each classifier learns to distinguish a single class from all the others combined.<br> + If there are k classes, k classifiers are trained.<br> + During prediction, the algorithm evaluates all classifiers on each input, and selects the class with the highest confidence score as the predicted class.<br>**Advantages:**<br> + Simpler and more efficient in terms of the number of classifiers (k)<br>Easier to implement for algorithms that naturally provide confidence scores (e.g., logistic regression, SVM).<br> **Disadvantages:**<br> + Classifiers may struggle with class imbalance since each binary classifier must distinguish between one class and the rest.<br>Requires the classifier to perform well even with highly imbalanced datasets, as the "all" group typically contains more samples than the "one" class.| **In the One-vs-One approach:** <br> + The algorithm trains a binary classifier for every pair of classes in the dataset.<br>If there are k classes, this results in classifiers.<br> + Each classifier is trained to distinguish between two specific classes, ignoring the rest.<br> + During prediction, all classifiers are used, and a "voting" mechanism decides the final class by selecting the class that wins the majority of pairwise comparisons.<br>**Advantages:** <br> + Suitable for algorithms that are computationally expensive to train on many samples because each binary classifier deals with a smaller dataset (only samples from two classes).<br> + Can be more accurate in some cases since classifiers focus on distinguishing between two specific classes at a time.<br> **Disadvantages:** <br> + Computationally expensive for datasets with a large number of classes due to the large number of classifiers required.<br>May lead to ambiguous predictions if voting results in a tie.|

## Support Vector Machines (SVM) 

![SVM](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/svm.png) <br>
![SVM](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/svm2.png) <br>
![SVM](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/svm3.png) <br>

SVM can be applied to regression tasks through a variant known as Support Vector Regression (SVR). 
Here’s how it works:
Objective: The goal of SVR is to find a function that approximates the relationship between input features and a continuous output variable. Instead of focusing on classifying data points, SVR aims to predict a continuous value.
![SVM](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/svm4.png) <br>
Epsilon Tube: SVR introduces a margin of tolerance, called the epsilon tube. This tube defines a region around the predicted function where errors are acceptable. Points that fall within this tube are considered to be correctly predicted, while points outside the tube are treated as errors.

Loss Function: SVR uses a loss function that penalizes points outside the epsilon tube. The objective is to minimize the number of points that fall outside this margin while also keeping the model as flat as possible. This is achieved by minimizing the coefficients of the function, which helps prevent overfitting.

Kernel Trick: Just like in classification tasks, SVR can also use kernel functions to handle non-linear relationships. By transforming the input features into a higher-dimensional space, SVR can fit complex curves that better capture the underlying patterns in the data.

Model Training: During training, SVR identifies the support vectors, which are the data points that lie closest to the epsilon tube. These support vectors are crucial for defining the regression function, while other points do not influence the model.
In summary, SVR applies the principles of SVM to regression tasks by focusing on fitting a function that predicts continuous values while allowing for some margin of error. If you have any further questions or need more details, feel free to ask!

### Scikit-Learn Kernel Function
+ Linear
+ PolyNomial
+ RBF
+ Sigmoid
