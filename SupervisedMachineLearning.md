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


## Cheat Sheet
|Process Name|Description|Code|
|---|--|---|
|One vs One classifier (using logistic regression)||from sklearn.multiclass import OneVsOneClassifier<br>from sklearn.linear_model import LogisticRegression<br>model = OneVsOneClassifier(LogisticRegression())|
|One vs All classifier (using logistic regression)||from sklearn.multiclass import OneVsRestClassifier<br>from sklearn.linear_model import LogisticRegression<br>model = OneVsRestClassifier(LogisticRegression())<br>OR<br>from sklearn.linear_model import LogisticRegression<br>model_ova = LogisticRegression(multi_class='ovr')|
|Decision tree classifier||from sklearn.tree import DecisionTreeClassifier<br>model = DecisionTreeClassifier(max_depth=5)|
|Decision tree regressor||from sklearn.tree import DecisionTreeRegressor<br>model = DecisionTreeRegressor(max_depth=5)|
|Linear SVM classifier||from sklearn.svm import SVC<br>model = SVC(kernel='linear', C=1.0)|
|K-nearest neighbors classifier||from sklearn.neighbors import KNeighborsClassifier<br>model = KNeighborsClassifier(n_neighbors=5, weights='uniform')|
|Random Forest regressor||from sklearn.ensemble import RandomForestRegressor<br>model = RandomForestRegressor(n_estimators=100, max_depth=5)|
|XGBoost regressor||import xgboost as xgb<br>model = xgb.XGBRegressor(n_estimators=100, learning_rate=0.1, max_depth=5)|

## Associate Functions used
|Medthod Name|Descripton|Code Syntax|
|--|--|--|
|OneHotEncoder|Transforms categorical features into a one-hot encoded matrix.|from sklearn.preprocessing import OneHotEncoder<br>encoder = OneHotEncoder(sparse=False)<br>encoded_data = encoder.fit_transform(categorical_data)|
|accuracy_score|Computes the accuracy of a classifier by comparing predicted and true labels.|from sklearn.metrics import accuracy_score<br>accuracy = accuracy_score(y_true, y_pred)|
|LabelEncoder|Encodes labels (target variable) into numeric format.|from sklearn.preprocessing import LabelEncoder<br>encoder = LabelEncoder()<br>encoded_labels = encoder.fit_transform(labels)|
|plot_tree|PLots a decision tree for visualization.|from sklearn.tree import plot_tree<br>plot_tree(model, max_depth=3, filled=True)|
|normalize|Scales each feature to have zero mean and unit variance (standardization).|from sklearn.preprocessing import normalize<br>normalized_data = normalize(data, norm='l2')|
|compute_sample_weight|Computes the sample weights for imbalanced datasets.|from sklearn.utils.class_weight import compute_sample_weight<br>weights = compute_sample_weight(class_weight='balanced', y=y)|
|roc_auc_score|Computes the Area Under the Receiver Operating Characteristic Curve (AUC-ROC) for binary classification models.|from sklearn.metrics import roc_auc_score<br>auc = roc_auc_score(y_true, y_score)|
