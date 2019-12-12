
# Simple Weather Forcasting Model

### Introduction 

Weather forecast is essential in modern society. People acquire weather information every day and everywhere to make plans on traveling and events. Weather forecasting helps people be prepared when a storm comes. In Iowa and some other agricultural states, weather is also significant in agricultural production, plotting time, spraying time, and harvest time, all determined by weather. 

This program aims at predicting the weather conditions in Ames, including but not limited to temperature, relative humidity, “feels like” temperature, wind speed, precipitation, and visibility, on an hourly basis. 

There are several models available online that aim at predicting temperature, RH values, etc. However, some of them only use historical data with a single factor or two or three factors to project the goal. This project, however, takes advantage of five factors to predict the remaining one, potentially increasing the reliability and accuracy of the model. 

### Workflow

![GitHub Logo](/images/DataExploration.png)
Format: ![Raw Data](url)

### Data Preprocessing

Although weather data is abundant, finding the right range of data that fits the specific problem sometimes can be challenging. In this project, the weather data are acquired from Iowa Environmental Mesonet’s ASOS Network. The range of data is from December 1, 2018 to December 1, 2019. The data is aquired in the format of txt files, and they were recorded on an hourly or half-hourly basis.

Here a link to my Python Notebooks. 

### Data Analysis

The main model used for this project is Random Forest. 

There are six weather factors in the dataset: air temperature (F), relative humidity (%), "feel-like" temperature, wind speed, hourly p recipitation, and visibility. To predict temperature, the rest of the five factors are set as input for training. Same principles apply to the other five factors, i.e. to predict relative humidity, temperature, "feel-like" temperature, wind speed, precipitation and visibility are all used to train the model to achieve better prediction results. As mentioned in the introduction, there are numerous factors that influence the weather, and at the same time, these factors are interlated and interacting with each other. 

### Results
The prediction for temperature earns a regression score of 0.969
The score for RH prediction is 
The score for "feels-like" prediction is 


### Limitations

Only one year of weather data was applied in training the model, which may not be sufficient 

### Class Exercise

An example class exercise can be found here. 
https://nbviewer.jupyter.org/github/pyli2019/516x-pli/blob/master/Weather%20Forcasting_Assignment.ipynb
