---
layout: page
title: Dining Concierge
description: Dining Concierge chatbot sends restaurant suggestions given a set of preferences that you provide through conversation
img: assets/img/chatbot.jpg
importance: 2
category: work
---

Customer Service is a core service for a lot of businesses around the world and it is getting disrupted now by Natural Language Processing-powered applications. 

Dining Concierge is a a serverless, microservice driven web application. It sends you restaurant suggestions given a set of preferences that you provide the chatbot through conversation. The application is completely built and deployed on AWS. The data for restaurants are scraped from yelp. We used the Yelp API to collect 5,000+ random restaurants from Manhattan.


    Amazon Web Services (AWS)
    S3
    HTML
    CSS
    Javascript
    API Gateway
    Lex
    Lambda
    Web scraping
    DynamoDB
    NoSql
    ElasticSearch
    SQS
    SNS
    CloudWatch



<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/chatbotArch.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Architecture diagram
</div>

Based on a conversation with the customer, the LEX chatbot will identify the customer’s preferences. It will search through ElasticSearch to find restaurant suggestions and find more information about the restaurants from DynamoDB and mail the customers.

Additionally, it remembers your last search for both location and category. When a user returns to the chat, they automatically receive a recommendation based on their previous search.


The live website can be found here :  <a href = ' http://frontend2-dining-concierge.s3-website-us-east-1.amazonaws.com/'>http://frontend2-dining-concierge.s3-website-us-east-1.amazonaws.com/</a>


The code for this can be found here : <a href="https://github.com/Avina20/Dining-Concierge">Here</a>