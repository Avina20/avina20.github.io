---
layout: page
title: Stock Price Prediction 
description: Time series forecasting in stock markets using Deep Learning
img: assets/img/stock/5.jpg
importance: 2
category: ai
giscus_comments: false
---

Predicting stock market trends has always been a challenging problem due to the complex and
dynamic nature of financial markets. Stock prices are influenced by numerous factors such as
economic indicators, investor sentiment, and company performance. While traditional methods
use statistical models, machine learning techniques like LSTM have emerged as a powerful tool
for handling sequential data.

<p>
This research implements LSTM networks for three tasks:
<ol>
    <li> Predicting future stock prices based on historical data </li>
    <li> Forecasting stock returns, calculated as the percentage change in prices </li>
    <li> Classifying the directional movement (up or down) of stock prices using binary classification </li>
</ol>
<br>

The goal is to assess the performance of LSTMs in predicting stock-related variables and
identify the challenges involved in financial sequence modeling.</p>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stock/2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stock/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stock/4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

    Tensorflow
    Neural Networks
    RNN
    LSTM
    Adam optimizer
    Classification
    MSE
    Pooling

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stock/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Long Short-Term Memory (LSTM) networks are a specialized type of
Recurrent Neural Network (RNN) designed to address the vanishing gradient problem. Unlike
standard RNNs, which struggle to retain long-term dependencies in sequential data, LSTMs use
a unique architecture that incorporates memory cells, enabling them to remember information
over extended time steps.
</div>

<p> The code for the project can be found : <a href = "https://github.com/Avina20/Stock-Returns-Prediction"> Here </a> </p>

