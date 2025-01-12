
# Simple Weather Forcasting Model

### Introduction 

Weather forecast is essential in modern society. People acquire weather information every day and everywhere to make plans on traveling and events. Weather forecasting helps people be prepared when a storm comes. In Iowa and some other agricultural states, weather is also significant in agricultural production, plotting time, spraying time, and harvest time, all determined by weather. 

This program aims at predicting the weather conditions in Ames, including but not limited to temperature, relative humidity, “feels like” temperature, wind speed, precipitation, and visibility, on an hourly basis. 

There are several models available online that aim at predicting temperature, RH values, etc. However, some of them only use historical data with a single factor or two or three factors to project the goal. This project, however, takes advantage of five factors to predict the remaining one, potentially increasing the reliability and accuracy of the model. 

![alt text](https://raw.githubusercontent.com/pyli2019/516x-pli/master/forecast-reliability2.jpg?raw=true "forecast-reliability2")
(Source: https://scijinks.gov/forecast-reliability/)
### Data Preprocessing

Although weather data is abundant, finding the right range of data that fits the specific problem sometimes can be challenging. In this project, the weather data are acquired from Iowa Environmental Mesonet’s ASOS Network. The range of data is from December 1, 2018 to December 1, 2019. The data is aquired in the format of txt files, and they were recorded on an hourly or half-hourly basis.

#### Raw Data
![alt text](https://github.com/pyli2019/516x-pli/blob/master/Correlation%20heatmap.png?raw=true "Correlation%20heatmap")

Correlation Map 

![alt text](https://github.com/pyli2019/516x-pli/blob/master/temp_vs_date.png?raw=true "temp_vs_date")

Demo: Temperature change in a year. Plots on other factors over time are omitted.  


Here a link to my Python Notebooks. 

### Data Analysis

The main model used for this project is Random Forest. There are six weather factors in the dataset: air temperature (F), relative humidity (%), "feel-like" temperature, wind speed, hourly p recipitation, and visibility. To predict temperature, the rest of the five factors are set as input for training. Same principles apply to the other five factors, i.e. to predict relative humidity, temperature, "feel-like" temperature, wind speed, precipitation and visibility are all used to train the model to achieve better prediction results. As mentioned in the introduction, there are numerous factors that influence the weather, and at the same time, these factors are interlated and interacting with each other. 

### Results

The prediction for temperature has a correlation coefficient of 0.969

The coefficient for RH prediction is 0.314

The coefficient for "feels-like" prediction is 0.424

The coefficient for wind speed prediction is 0.0769

The coefficient for precipitation prediction is 0.0425

The coefficient for visbility prediction is 0.0944

![alt text](https://raw.githubusercontent.com/pyli2019/516x-pli/master/1.PNG?raw=true "1")

![alt text](https://raw.githubusercontent.com/pyli2019/516x-pli/master/2.PNG?raw=true "2")

![alt text](https://raw.githubusercontent.com/pyli2019/516x-pli/master/3.PNG?raw=true "3")

![alt text](https://raw.githubusercontent.com/pyli2019/516x-pli/master/4.png?raw=true "4")

![alt text](https://raw.githubusercontent.com/pyli2019/516x-pli/master/5.png?raw=true "5")

![alt text](https://raw.githubusercontent.com/pyli2019/516x-pli/master/6.png?raw=true "6")




### Limitations

The model is good at predicting temperature, since its correlation factor is 0.969. However, other predictions seem to fail in accuracy. The reason could be only one year of weather data was applied in training the model, which may not be sufficient. Another reason could be that the real weather forcasting model consists of numerous factors, and five factors are not representative enough to make a prediction.

### Class Exercise

An example class exercise can be found here. 
https://nbviewer.jupyter.org/github/pyli2019/516x-pli/blob/master/Weather%20Forcasting_Assignment.ipynb

Thank you for visiting. 
