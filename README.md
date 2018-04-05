**Description**
----------------------------------------------------------------------------------------------------------------
This analysis was done to understand how student performance various across different courses in a Virtual Learning environment and how the student performance and course quality together can influence a student's withdrawal, failure or pass rate. This analysis helped figure the important variables for understanding student engagement and how these features can help design appropriate courses in future.  
The open source dataset was obtained from: [Open University Analytics dataset](https://analyse.kmi.open.ac.uk/open_dataset)  

*Citation: Kuzilek, J. et al. Open University Learning Analytics dataset Sci. Data 4:170171 doi: 10.1038/sdata.2017.171 (2017).*

**Notes**
----------------------------------------------------------------------------------------------------------------
- The code has been written used Python3 using Jupiter notebook as interface

- The code needs to be executed in a sequential fashion as in certain cases previously created tables are referred to later

**Approach**
-----------------------------------------------------------------------------------------------------------------
Exploration of data using descriptive statistics and visual representations helped understand the data discrepancies and how different variables within the dataset effect student engagement and performance.  
[Decision Tree classifier](https://en.wikipedia.org/wiki/Decision_tree) was also used here to see variable importances for determining student performance and if it conforms with the insights obtained from Exploratory Data analysis.  

Due to the huge class imbalance, [Logistic regression](https://en.wikipedia.org/wiki/Logistic_regression) was applied on downsampled data to classify a student's overall performance as Pass, Fail, Withdrawal according to its engagement with the course and previous marks obtained. Confusion matrix was used as an evaluation criteria and the following plot was obtained for the same:  
<img src="https://github.com/charvi5/VirtualLearning-Analysis-Classification/blob/master/image1.png" height="300" width = "450">

This performance was compared with classification model built using [Random Forest](https://en.wikipedia.org/wiki/Random_forest) as it handles imbalanced classes well. Following confusion matrix was obtained for Random Forest:  
<img src="https://github.com/charvi5/VirtualLearning-Analysis-Classification/blob/master/image2.png" height ="300" width = "450"> 

Visual representation of evaluation criteria help us better understand the ongoings of model and helps evaluate the tradeoff between [Type I and TypeII errors](https://en.wikipedia.org/wiki/Type_I_and_type_II_errors).

This analysis can be useful for both course instructors and companies offering online courses to understand how to measure a courses's and student's success rate and the factors to most focus on.  
The analysis can be further improved by applying more sophisticated classification models to increase model accuracy.  
Clustering can also be employed here to identify similar students on the basis of their demographics and engagement.

**Installing libraries and packages**
-----------------------------------------------------------------------------------------------------------------
To run the notebook, following list of packages must be installed in the system:
-  Pandas
-  Numpy
-  matplotlib
-  sklearn

scikit-learn is the base library used to import following modeling packages:
-  tree
-  LogisticRegression
-  metrics
-  linearmodel
-  train_test_split
-  confusion_matrix
-  classification_report
-  resample
-  RandomForestClassifier
-  accuracy_score

The above packages can be loaded using the command ```from sklearn import <package-name>```

**Mac OS:**
- To download libraries and packages being loaded in first block of the code, go to Terminal and download packages using 
```pip install package-name ```
- If pip throws an error due to packages not being a part of pip anymore, use ```condo install package-name``` , this is an Anaconda command and directly downloads packages in Anaconda

**Windows:**
- Open Windows command prompt and enter ```py -3.6 -m pip install package-name```



