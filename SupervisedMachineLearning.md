![polynomial](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/polynomial.png) <br>
![polynomial example](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/polynomial2.png) <br>
![polynomial example](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/polynomial3.png) <br>
![Non linear](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/nonlinear.png) <br>

### CLASSIFICATION
|One vs ALL strategy|One vs One strategy|
|--|--|
|**In the One-vs-All approach:** <br> + The algorithm trains a single binary classifier for each class.<br> + Each classifier learns to distinguish a single class from all the others combined.<br> + If there are k classes, k classifiers are trained.<br> + During prediction, the algorithm evaluates all classifiers on each input, and selects the class with the highest confidence score as the predicted class.<br>**Advantages:**<br> + Simpler and more efficient in terms of the number of classifiers (k)<br>Easier to implement for algorithms that naturally provide confidence scores (e.g., logistic regression, SVM).<br> **Disadvantages:**<br> + Classifiers may struggle with class imbalance since each binary classifier must distinguish between one class and the rest.<br>Requires the classifier to perform well even with highly imbalanced datasets, as the "all" group typically contains more samples than the "one" class.| **In the One-vs-One approach:** <br> + The algorithm trains a binary classifier for every pair of classes in the dataset.<br>If there are k classes, this results in classifiers.<br> + Each classifier is trained to distinguish between two specific classes, ignoring the rest.<br> + During prediction, all classifiers are used, and a "voting" mechanism decides the final class by selecting the class that wins the majority of pairwise comparisons.<br>**Advantages:** <br> + Suitable for algorithms that are computationally expensive to train on many samples because each binary classifier deals with a smaller dataset (only samples from two classes).<br> + Can be more accurate in some cases since classifiers focus on distinguishing between two specific classes at a time.<br> **Disadvantages:** <br> + Computationally expensive for datasets with a large number of classes due to the large number of classifiers required.<br>May lead to ambiguous predictions if voting results in a tie.|

![SVM](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/svm.png) <br>
![SVM](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/svm2.png) <br>
![SVM](https://github.com/jeannieteo/IBMProfessionalCertDataSceience/blob/main/images/svm3.png) <br>

### Scikit-Learn Kernel Function
+ Linear
+ PolyNomial
+ RBF
+ Sigmoid
