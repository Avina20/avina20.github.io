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

<h2>FOREX CLASSIFICATION</h2>

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

<h3>Architecture</h3>
Real-time data was collected for 10 currency pairs from Polygon.io website. The dataset we used deals with real-world forex transactions. We used PyCaret to compare 15+ classifiers and selected the best model using metrics like Accuracy, F1, Recall, Auc, etc. Since the forex markets are open only 5 days a week, there are ranges of data with missing values. Moreover, even during working hours there can be missing data for hours. This can lead to inconsistencies in data, affect our calculations, make the model biased and overall affect the result of our model. Built a regression model for base currency pairs (EURUSD, GBPCHF, and USDCAD) using real-time data from Polygon, followed by a classification task for the remaining currency pairs.Correlation with BTC was calculated and added as a feature to replicate macroeconomic influence.


<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/forex/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/forex/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>



<h3>Results:</h3>

Two regression models were trained using PyCaret's regression module.
<ul>
<li>1 - FD : Best Model: Extreme Gradient Boosting (XGBoost)</li>
<li>2 - Volatility: Best model: Decision Tree Regressor</li>
</ul>

These results show that while the Decision Tree for volatility performed moderately better than FD prediction, overall regression models require more data and better feature engineering for improved performance.

Classification

<ul>
<li>No currency was strictly forecastable (both FD and VOL < 0.5).</li>
<li>Most currencies fell into the Partially Forecastable category due to mixed FD and VOL results.</li>
</ul>



<br>


<h2>LONG-SHORT TRADING</h2>

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

<h3>Architecture</h3>
The L/S is done on 1 hour data after adjusting the ration of the two currency pairs. Choose the Long and Short CPs using univariable time series regression. Repeated this at the end of each hour, for atleast 3 hours

<h4> Optimization strategies:</h4>
<ol>
<li>Threshold - Instead of constantly being in a long or short position, the strategy only becomes active after a specific signal or indicator crosses a predefined level (the threshold). We defined threshold and tried on different threshold to get maximum profit This makes the strategy more selective. It aims to filter out noise and only trade when the signal is considered strong enough (having crossed the threshold). It can reduce the number of trades but potentially increase the quality of signals acted upon.</li>
<li> Prioritizing short term trends- This implies the strategy makes decisions based only on the very latest data point(s), ignoring older data in the series. The one hour data has 3600 data points, but to capture the latest trend it is better to just use the last 1500-2000 rows. This makes the strategy extremely reactive to the most recent price action. It can capture very short-term moves but might be prone to "whipsaws" (getting stopped out by small, random fluctuations) because it ignores the broader trend or context provided by older data. It simplifies calculations significantly.</li>
</ol>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/forex/4.jpg" title="example image" class="img-fluid rounded z-depth-1"%}
    </div>
</div>
<br>
The code for the web app can be found here : <a href="https://github.com/Avina20/ForexVision">Code</a>