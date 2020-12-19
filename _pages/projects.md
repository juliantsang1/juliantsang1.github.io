---
title: "Data Science Projects"
permalink: /projects/
---


### [Diagnosing Pneumonia from Chest X-Rays](https://github.com/juliantsang1/Pneumonia-Xrays/blob/main/W207_Final_Project_Kaggle_compatability_v2_Apples_to_Apples.ipynb)
Using convolutional neural networks, we attempt to create a multi-class classifier that would be able to identify whether a given image of a chest x-ray is normal or has bacterial or viral pneumonia. Based on a [Kaggle dataset](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia) provided by Paul Mooney, we utilize preprocessing techniques to remove the diaphragm from the original x-ray images. This is because the diaphragm region in x-ray images are usually regions with the brightest pixels. Removing these high-intensity white areas may have a positive effect in distinguishing potential patterns of pneumonia in the lung areas. We've uploaded the preprocessed images into a new Kaggle dataset [here](https://www.kaggle.com/juliantsang1/xray-pneumonia-preprocessing). Using ensemble techniques with pre-trained architectures, we were able to achieve approximately 89% test accuracy.

![X-Ray Preprocessing Demo](/images/pneumonia_chest_xray_preprocessing.png)


### [Case Study: Is there a relationship between playground availability and household income in New York City?](https://github.com/juliantsang1/NYCIncomePlaygrounds/blob/master/IncomeVsPlayground%20-%20Final-revised.ipynb)
Using datasets provided by the IRS and NYC Open Data, I attempt to investigate whether household income has any relationship with playground and park availability in New York City. Using the folium library, I create an interactive map with multiple overlays illustrating the distribution of income, playgrounds, and park density according to zip codes.

![Interactive Map](/images/NYC_Parks_image.png)
[NYC Playground-Income Interactive Map](https://juliantsang1.github.io/NYC-Income-Playgrounds/NYC_Choropleth_Map.html)



### [San Francisco Bike Sharing Analysis](https://github.com/juliantsang1/SFBikeshare/blob/master/Project_1.ipynb)
Using Google BigQuery public datasets, I perform some exploratory analysis into Lyft's BayWheels Bikesharing Program. Afterwards, I describe some business recommendations that could be used to improve the service.

![SF Bikeshare chart](/images/sf_bikeshare_chart_image.png)
