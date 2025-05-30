---
layout: page
title: OpenFoodFacts
description: Exploring Global Food Quality Patterns through a Visual Dashboard
img: assets/img/openfood/5.png
importance: 2
category: web
related_publications: false
---

I built an interactive dashboard using Dash library to explore the OpenFoodFacts dataset, which contains nutritional information about food products from around the world. This open-source database includes details on ingredients, nutritional content, additives, processing levels, and quality scores for products across different countries.

The OpenFoodFacts data includes various nutritional metrics, with key variables including:
<ul>
<li>Nutrition grade (A-E scale, with A being healthiest)</li>
<li>NOVA group (1-4 scale of processing level, with 1 being least processed)</li>
<li>Nutritional content (fat, sugar, salt, protein, carbohydrates)</li>
<li>Additives count</li>
<li>Country of origin</li>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/openfood/1.jpg" title="dashboard 1" class="img-fluid rounded z-depth-1"%}
    </div>
</div>


I formulated two primary research questions to guide my visual analysis:
<ol>
    <li>How does food processing level (NOVA classification) relate to nutritional quality across different countries?</li>
    <li>Is there a relationship between a country's economic development (GDP per capita) and the nutritional quality of its food products?</li>
</ol>    

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/openfood/2.jpg" title="dashboard 1" class="img-fluid rounded z-depth-1"%}
    </div>
</div>

<h2>VISUALIZATIONS</h2>

<ol>
<li>Visualization 1: Nutrition Grade Distribution by Country
    The visualization immediately revealed interesting patterns:
    <ul>
    <li>France has a higher proportion of Grade A products compared to other countries</li>
    <li>The United States has more Grade D and E products</li>
    <li>Germany shows a relatively balanced distribution</li></ul>
</li>
<li>Visualization 2: Food Processing Level Distribution (NOVA Classification)
This visualization revealed:
    <ul>
    <li>Countries with better nutrition grades tend to have more Group 1 and 2 products</li>
    <li>The United States has the highest proportion of ultra-processed (Group 4) foods</li>
    <li>This aligns with the nutrition grade findings and suggests processing level could be a key factor in overall food quality</li></ul>
</li>
<li>Visualization 3: Average Macronutrient Content by Country
    Key observations:
    <ul>
    <li>Countries with higher nutrition grades generally have lower sugar and salt content</li>
    <li>Protein content varies less dramatically across countries</li>
    <li>The United States and United Kingdom products show higher fat content on average</li></ul>
</li>
<li>Visualization 4: Relationship Between Additives and Nutrition Score
    The visualization revealed:
    <ul>
    <li>A negative correlation between additives count and nutrition score (more additives = lower nutrition quality)</li>
    <li>Clear clustering of countries, with some having consistently higher additive counts</li>
    <li>Products with the highest number of ingredients often have more additives</li></ul>
</li>
<li>Visualization 5: Economic Development vs Food Quality
This visualization provided fascinating insights:
    <ul>
    <li>Higher GDP countries don't necessarily have better nutrition scores</li>
    <li>There appears to be an inverted U-relationship: middle-income countries often have the highest nutrition scores</li>
    <li>Lower GDP countries tend to have fewer additives but middle NOVA groups</li>
    <li>The highest GDP countries have more additives and higher processing levels</li></ul>
</li>
<li>Visualization 6: Processing Level Distribution by Country
    The findings were striking:
    <ul>
    <li>Countries like France and Italy have significantly higher percentages of Group 1 and 2 foods</li>
    <li>The United States and United Kingdom have over 60% of products in the ultra-processed Group 4 category</li>
    <li>This visualization clearly demonstrates that food systems in different countries prioritize different levels of processing, which directly impacts nutritional quality</li></ul>
</li>
</ol>

<br>
<h2>Theories of Data Visualization</h2>
In the OpenFoodFacts Explorer project, several fundamental theories and principles of data visualization were carefully applied to maximize the effectiveness of the visualizations. These principles guided design decisions and enhanced the communicative power of the analysis.

    1. Gestalt Principles
    2. Pre-attentive Processing
    3. Color Theory
    4. Tufte's Principle
    5. Shneiderman's Mantra: "Overview first, zoom and filter, then details-on-demand"
    6. Bertin's Visual Variables
    7. Cognitive Load Theory
    8. Cleveland and McGill's Graphical Perception

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/openfood/3.jpg" title="dashboard 1" class="img-fluid rounded z-depth-1"%}
    </div>
</div>

The code for the web app can be found here : <a href="https://github.com/Avina20/openfood">Code</a>

