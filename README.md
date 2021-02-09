# Predictive-Maintenance-for-Aircraft-Engine

My purpose is to focus on the functionality and performance of the systems, specifically the aircraft engine system. I analyze how the system will continue functioning, namely, to predict if the engine will fail within a certain time frame (for example days or cycles.) With forecasting, engineers can schedule maintenance, optimize operating efficiency, and avoid unplanned downtime.

The datasets are provided by NASA. Each dataset has a training set and testing set with a different number of engine units from run-to-failure. The training dataset has over 20,000 observations. The testing dataset has over 13,000 observations. The dataset consists of aircraft engine unit number, Cycles of each engine running, three operating settings, another 21 columns of sensors’ data such as temperature and pressure, which rise or fall over time with obvious signs of degradation.

![11](https://user-images.githubusercontent.com/32876600/107393103-637be700-6ac8-11eb-8e38-35f16a560113.JPG)

The data was clean, with no missing value, in a tidy format. All the data are numeric. I derive my target variable of Remaining useful life (RUL), which is the length of time an engine is likely to operate before it requires repair or replacement. For the feature engineering, I standardized my data to scale all the sensors with uniform observation interval. I made the boxplot to overview the engine’s life span dispersion. I plotted the operation settings over cycles. I decomposed all the sensors measurements to observe trends and filtered out Non-useful ones. I used heatmap to plot the correlations among sensors. 
For the model selection, I used Support Vector Machine (SVM) and Random Forest as my main models. I found the top important features for the forecasting. The results are well predicted by SVM with reasonable engine life range and high accuracy.  

![8](https://user-images.githubusercontent.com/32876600/107393227-8b6b4a80-6ac8-11eb-83dd-b141e9ae168d.png)

Decompose signal sensors:

![6](https://user-images.githubusercontent.com/32876600/107393272-9cb45700-6ac8-11eb-9212-3aa0ee70b95c.png)

Training and testing data:

![13](https://user-images.githubusercontent.com/32876600/107393550-ec931e00-6ac8-11eb-9f3c-6047b4816817.png)

My conclusion is the aircraft engine needs well maintenance after 160 to 180 flights. After 200 flights, we could consider replacing the engine with a brand new one for the safety concern.

Random Forest:

![rff](https://user-images.githubusercontent.com/32876600/107394159-8ce94280-6ac9-11eb-90a3-4ce81b215a75.JPG)

SVM:

![svmm](https://user-images.githubusercontent.com/32876600/107394215-9e324f00-6ac9-11eb-9d7c-366fe49c433c.JPG)

Top features:

![top features](https://user-images.githubusercontent.com/32876600/107394252-a9857a80-6ac9-11eb-84db-bba9a78752d3.JPG)
