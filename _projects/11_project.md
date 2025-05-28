---
layout: page
title: IntelliForexVision
description: AI-based real-time Forex market analysis and Long/Short trading strategies 
img: assets/img/forex/1.jpg
importance: 1
category: ai
related_publications: false
---

IntelliForexVision is an AI-powered real-time foreign exchange (FX) market analysis. 

<h1>FOREX CLASSIFICATION</h1>

Forex classification engine uses strategic financial market analysis and time series forecasting to optimize trading strategies in dynamic markets. It leverages data acquisition, database management, feature engineering, machine learning (regression and classification), and algorithmic trading strategy implementation.
  

This project leverages real-time forex transaction data to:

    ● Calculate inter-currency correlations

    ● Extract advanced statistical features like Volatility, Keltner Bands and Fractal Dimension (FD)

    ● Classify currency pairs as Forecastable, Partially Forecastable, or Non-Forecastable

    ● Optimize financial decision-making through machine learning (PyCaret) pipelines

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/forex/2.jpg" title="example image" class="img-fluid rounded z-depth-1"%}
    </div>
</div>

Tech Stack

    ● Data Source -  Polygon.io API
    ● Database - MongoDB, SQLite, ArcitcDB
    ● Machine Learning - PyCaret - Regression and Classification
    ● Deep Learning - Neural Networks
    ● Libraries - Visualization - Matplotlib, Seaborn
    ● Scheduling - RepeatedTimer
    ● Pandas, NumPy, Scikit

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/forex/4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/forex/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<h2>Architecture</h2>
Real-time data was collected for 10 currency pairs from Polygon.io website. The dataset we used deals with real-world forex transactions. We used PyCaret to compare 15+ classifiers and selected the best model using metrics like Accuracy, F1, Recall, Auc, etc. Since the forex markets are open only 5 days a week, there are ranges of data with missing values. Moreover, even during working hours there can be missing data for hours. This can lead to inconsistencies in data, affect our calculations, make the model biased and overall affect the result of our model. Built a regression model for base currency pairs (EURUSD, GBPCHF, and USDCAD) using real-time data from Polygon, followed by a classification task for the remaining currency pairs.Correlation with BTC was calculated and added as a feature to replicate macroeconomic influence.

<h2>Results:</h2>

Two regression models were trained using PyCaret's regression module.
    1 - FD
    Model used: Extreme Gradient Boosting (XGBoost)
        ○ MAE: 0.3955
        ○ MSE: 0.1669
        ○ RMSE: 0.4086
        ○ R²: -1.9437 (indicating poor model fit)
    2 - Volatility
    Decision Tree Regressor:
        ○ MAE: 0.1601
        ○ MSE: 0.0350
        ○ RMSE: 0.1870
        ○ R²: -0.0024 (model explains little variance)

These results show that while the Decision Tree for volatility performed moderately better than FD prediction, overall regression models require more data and better feature engineering for improved performance.

Classification

Average results:
    ○ No currency was strictly forecastable (both FD and VOL < 0.5).
    ○ Most currencies fell into the Partially Forecastable category due to mixed FD and VOL results.






<h1>Long-Short Trading</h1>

Implemented & optimized a Long/Short trading strategy to profit from anticipated price movements.

Going Long ("Buying"):
<ul>
    <li> Expectation: Base currency appreciation.</li>
    <li> Mechanic: Buy the pair. Goal: Buy low, sell high.</li>
</ul>
Going Short ("Selling"):
<ul>
    <li> Expectation: Base currency depreciation.</li>
    <li> Mechanic: Sell the pair. Goal: Sell high, buy back low.</li>
</ul>

Executed the L/S strategy over several hours, adjusting for price ratios, and calculated Profit/Loss (P/L)


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/forex/3.jpg" title="example image" class="img-fluid rounded z-depth-1"%}
    </div>
</div>

<h2>Architecture</h2>


The code for the web app can be found here : <a href="https://github.com/Avina20/classmate-io">Code</a>

Additional code for NLP implementations for text summarization and improved MCQ generation can be found here <a href="https://github.com/Avina20/MCQ-generator">Here</a>