# IBMProfessionalCertDataSceience


### Data Analysis with Python
![image1](images/SciComputeLIBS1.png)
![image1](images/SciComputeLIBS2.png)
![image1](images/SciComputeLIBS3.png)

### EXPORT to different formats
|Data Format|Read|Save|
|----------|----|-----|
|csv|pandas.read_csv()|df.to_csv()|
|json|pandas.read_json()|df.to_json()|
|excel|pandas.read_excel()|df.to_excel()|
|sql|pandas.read_sql()|df.to_sql()|

### Data Visualization commands in Python
#### a. matplotlib
import matplotlib.pyplot as plt
from matplotlib import pyplot as plt
%matplotlib inline

|matplotlib functions|Syntax|
|-------------|-----------------|
|Standard line plot|plt.plot(x,y)|
|Scatter plot|plt.scatter(x,y)|
|Histogram|plt.hist(x,bins)|
|Bar plot|plt.bar(x,height)|
|Pseudo Color Plot|plt.pcolor(C)|

import seaborn as sns
|seaborn functions|Syntax|
|-------------|-----------------|
|Regression plot|sns.regplot(x = 'header_1',y = 'header_2',data= df)|
|Box and whisker plot|A box plot (or box-and-whisker plot) shows the distribution of quantitative data in a way that facilitates comparisons between variables or across levels of a categorical variable. The box shows the quartiles of the dataset while the whiskers extend to show the rest of the distribution, except for points that are determined to be "outliers".|
|Residual Plot|sns.residplot(data=df,x='header_1', y='header_2') \ sns.residplot(x=df['header_1'], y=df['header_2'])|
|KDE plot AKA Kernel Density Estimate (KDE) plot |sns.kdeplot(X)|
|Distribution Plot|sns.distplot(X,hist=False)|
