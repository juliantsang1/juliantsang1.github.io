---
title: "Data Science Projects"
permalink: /projects/
---

### [Air Traffic Departure Delay Prediction](https://github.com/juliantsang1/W261_airport_delays.ipynb)
In this exercise of predicting airport departure delays, we explore airline data, engineer features, and perform model selection.
We found that creating new features that corresponded to airport delay state or tail number delay state led to the greatest performance gains. We found that the following features were most predictive of departure delays:
  PRIOR_DEL15 (binary variable) - indicates if there was a prior delay of at least 15 minutes during a time window starting eight hours before scheduled departure and ending two hours before scheduled departure time.
  PRIOR_DEP_DELAY (minutes) - same definition as above the the variable is expressed in minutes
  AVG_ORIGIN_DELAY (minutes) - indicates the average delay in minutes of the origin airport occurring between three and two hours prior to a flight's scheduled departure time
These flight-related features were considered the most important and predictive of the target label and we were surprised to learn that weather features were generally not considered important by our models. There are some possible reasons for the effectiveness of prior delay state. The air travel system is an interconnected network, with earlier flights affecting later flights. A delay that occurs early in the day at one airport can contribute to later delays at the same or different airports. It’s also possible that an airport’s average delay metric acted as a proxy for weather or other conditions that caused delays.

The final model selected was an XGBoost model trained on a dataset consisting of all flights occurring from 2015-2018 and evaluated on a test set containing 2019 flights. Delay F1 Score was 0.5495 and Non-Delay F1 Score was 0.8659. Since the dataset was heavily imbalanced, with non-delays outnumbering delays by approximately a 5:1 ratio, we also evaluated against Area Under Precision Recall Curve (AUPRC), which takes into account of precision and recall of the positive class. AUPRC was 0.62.

![Model Results Chart](/images/airport_delay_model_results.png)



### [Effect of Learning Feedback Styles on Learning Outcomes](https://github.com/juliantsang1/W241_Final_Report_Battle_Khoury_Hung_Tsang.pdf)
Feedback interventions are pervasive to professional environments. The aim of this study is to assess the effectiveness of different types of feedback. We use a controlled experiment and ask subjects to classify X-Ray images for healthy or penumonia-sick lungs. 333 participants recruited on Amazon’s Mechanical Turk analyzed three sets of X-Ray lung images on an online survey. After a pre-treatment test, participants are randomly assigned to five different feedback groups (one control and four types of feedback) and received feedback in between each set of X-Ray images (twice in total).

We found that expert-driven feedback was statistically significant and led to some of the highest improvements in X-Ray analysis. Furthermore, self-reflective feedback techniques were shown to be just as significant and effective. In quick, recognition-based tasks, focusing on negative feedback (i.e. what is wrong) may not be an effective strategy to improve performance. We also found that the marginal improvements in scores from a second feedback session are not significant and may not be worthwhile for shorter duration jobs. Lastly, feedback was found to be more impactful for low achieving performers. High performers do not exhibit any increased boost from feedback and may have been just as successful regardless of feedback sessions.

![Experiment Result Chart](/images/task_experiment_result_chart.png)


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
