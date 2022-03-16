# Soil-Organic-Carbon

The dataset consists of spectroscopic measurements (readings of NIR and UVVis sensors) (feature columns prefixed with nir_ or uv_, the number after the prefix is the measuring wavelength in nm) identified by a unique measurement ID (measurement_ID). Sensor readings were performed with stenon FarmLab devices directly in the soil on three different fields (see column location) in the US. Coordinate pairs (see columns lat and lng; WGS84) specify the location where the soil readings were performed. Column soc_percent_labval contains soil organic carbon content in % determined by soil sampling of the soil layer of 0-30 cm depth close to the position of a FarmLab device reading.

This notebook implements the PLSR model, Ridge as well as CNN model.

I have used two below references to understand the study:

Basically here I have used the NIR spectroscopic measurements to predict the soil organic carbon content. I have also referred some analysis functions I found from the spectroscopy blog, nirpyresearch: [Reference1](https://nirpyresearch.com/two-scatter-correction-techniques-nir-spectroscopy-python)

The PLSR and CNN models are foundings as per the paper "Modern practical convolutional neural networks for multivariate regression: Applications to NIR calibration": [Reference2](https://www.sciencedirect.com/science/article/abs/pii/S0169743918301382?via%3Dihub) 

There are two different notebooks. 
- One with the ML algorithms, understanding the problem, finding the resource location and distances, and going through various research papers and using appropriate models to find the solution.
- Other one with neural network based CNN model as per the Reference2 to compare with ML models and validate the performance.


Personal Note:
Both PLSR and CNN gives approximate scores. So we cannot say that CNN is better model here. The author in reference2 suggests that CNN can be a better fit but for that we need more findings, data and more details on the study. In the current study PLSR is much more straightforward and simple model with a good performance.
