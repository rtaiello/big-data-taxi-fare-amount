# BigData-Taxi-Fare-Amount

## Description

This repository contains the code used to face the kaggle challenge - Taxi Fare Amount organized by Google Cloud & Coursera.<br>
This is a regression task, the goal is to be able to create a model capable of predicting the taxi fare in New York.<br>
We presented this project during the Big Data exam at Sapienza University of Rome.

For further details you can use the presentation slides.


#### Metrics

The metrics used is the Root Mean Square Error
```math
RMSE = \sqrt{\frac{1}{n}\sum_{i=1}^{n}(y_{i} - \hat{y_{i}})^{2}}
```
## Framework used:

The technologies used to tackle the task are:
The main framework used is Spark, for data management and for Machine Learning algorithms.

We have used Google Maps APIs (of which the code is not present), the Waze APIs (present code) and OpenStreetMap APIs.

We have used the Light Gradient Boosting Machine Regressor as a model since the implementation of Microsoft Azure.

## Real distance:
For us the distance between two points is considered real if it meets 2 conditions:
1. It takes into account the shape of our planet
2. It takes into account the roads and their signs that can be crossed by a car

To calculate this distance we start first using the Haversine Distance formula which calculates the air distance, but it does not take into account the type of vehicle and the presence of roads. We use the Haversine Distance as heuristic.

Then we move to the Open Street Map routing project. We instanciate our OSMR API - Docker server and we calculate the real distance between two points.





## Authors

*   **Riccardo Taiello**  - [github](https://github.com/riccardinho22)
*   **Andrea Bacciu**  - [github](https://github.com/andreabac3)