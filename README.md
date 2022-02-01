# mercedes-benz-test-time
**Reduce the time a Mercedes-Benz spends on the test bench.**

Problem Statement Scenario: Since the first automobile, the Benz Patent Motor Car in 1886, Mercedes-Benz has stood for important automotive innovations. These include the passenger safety cell with a crumple zone, the airbag, and intelligent assistance systems. Mercedes-Benz applies for nearly 2000 patents per year, making the brand the European leader among premium carmakers. Mercedes-Benz is the leader in the premium car industry. With a huge selection of features and options, customers can choose the customized Mercedes-Benz of their dreams.

To ensure the safety and reliability of every unique car configuration before they hit the road, the company’s engineers have developed a robust testing system. As one of the world’s biggest manufacturers of premium cars, safety and efficiency are paramount on Mercedes-Benz’s production lines. However, optimizing the speed of their testing system for many possible feature combinations is complex and time-consuming without a powerful algorithmic approach.

You are required to reduce the time that cars spend on the test bench. Others will work with a dataset representing different permutations of features in a Mercedes-Benz car to predict the time it takes to pass testing. Optimal algorithms will contribute to faster testing, resulting in lower carbon dioxide emissions without reducing Mercedes-Benz’s standards.

**Following actions are performed:**

*i)Check for null values and unique values:*

No null values. Following are the categorical and unique values for test and train data

Number of Categorical features:  Index(['X0', 'X1', 'X2', 'X3', 'X4', 'X5', 'X6', 'X8'], dtype='object')
Number of Categorical features:  Index(['X0', 'X1', 'X2', 'X3', 'X4', 'X5', 'X6', 'X8'], dtype='object')

unique values of train dataset:
 ['a' 'aa' 'ab' 'ac' 'ad' 'ae' 'af' 'ag' 'ah' 'ai' 'aj' 'ak' 'al' 'am' 'an'
 'ao' 'ap' 'aq' 'ar' 'as' 'at' 'au' 'av' 'aw' 'ax' 'ay' 'az' 'b' 'ba' 'bc'
 'c' 'd' 'e' 'f' 'g' 'h' 'i' 'j' 'k' 'l' 'm' 'n' 'o' 'p' 'q' 'r' 's' 't'
 'u' 'v' 'w' 'x' 'y' 'z']
 
---------------------------------------------------------------------------------------------------------------------
unique values of test dataset:
 ['a' 'aa' 'ab' 'ac' 'ad' 'ae' 'af' 'ag' 'ah' 'ai' 'aj' 'ak' 'al' 'am' 'an'
 'ao' 'ap' 'aq' 'as' 'at' 'au' 'av' 'aw' 'ax' 'ay' 'az' 'b' 'ba' 'bb' 'bc'
 'c' 'd' 'e' 'f' 'g' 'h' 'i' 'j' 'k' 'l' 'm' 'n' 'o' 'p' 'q' 'r' 's' 't'
 'u' 'v' 'w' 'x' 'y' 'z']
 
 *ii)Target Value Distribution*
 
![image](https://user-images.githubusercontent.com/64850346/152009778-dd784edb-9fa9-463a-9e84-16abddb92728.png)

![image](https://user-images.githubusercontent.com/64850346/152009898-dc9f87c3-1edf-4a53-8e63-3128391b8631.png)

Data is found continous

*iii) Plotting scalled data after performing label encoder*

![image](https://user-images.githubusercontent.com/64850346/152010214-efd53769-8653-4c67-b46c-b9dc2ed34601.png)

![image](https://user-images.githubusercontent.com/64850346/152010242-1f2bf74b-ddf6-441c-9555-dcdfa3bdf035.png)

*iv) Plotting scaled data after dimensionality reduction using PCA*

![image](https://user-images.githubusercontent.com/64850346/152010524-e6092470-2c7b-48fe-aa47-3e094222705e.png)

![image](https://user-images.githubusercontent.com/64850346/152010550-e09d43be-b4d6-4aef-9c90-d2b2c61f245f.png)

Cumulative explained variance found same in both the cases. Defining 100 variables for getting 80% accuracy and plotting the transformed data set after PCA

![image](https://user-images.githubusercontent.com/64850346/152011734-657169bc-84f2-434a-951a-2d4fea8e94eb.png)

Percentage of variance attributed to PCA1(train): 0.8417194463821848

Percentage of variance attributed to PCA1(test): 0.8502486806728594

*v) Performing lasso, Ridge, Elastic net and xg boost*

***RIDGE REGRESSION MODEL***

RMSE Value for train dataset:  12.319223108715557

RMSE Value for test dataset:  12.319223108715557

R2Value/Coefficient of Determination:-0.07249730297576118

***LASSO REGRESSION MODEL***

RMSE Value for train dataset:  12.334148280983978

RMSE Value for test dataset:  12.334148280983978

R2Value/Coefficient of Determination:-0.05203781450209367

***ELASTIC NET REGRESSION MODEL***

RMSE Value for train dataset:  12.498268858407224

RMSE Value for test dataset:  12.498268858407224

R2Value/Coefficient of Determination:-0.009613566304350618

***XG BOOST***

XGBoost score on training set:  0.27629523806940715

It is found that xgboost performed better than other models and prediction on test data can be generated.
