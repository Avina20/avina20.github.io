---
layout: page
title: Normalization of ESA’s ENVISAT ocean satellite images
description: Research internship in Image Processing under Dr. Santhi V funded by ISRO
img: assets/img/inp1.jpg
importance: 3
category: work
---

The decrease of backscatter in the range direction of the signal received by sensors while radar imaging results in a progressive reduction of brightness over images from near to far range. Mostly HH and VV polarizations are affected by this phenomenon. This affects the detection and classification of sea surface features and activities in SAR images. In this paper, we proposed an algorithm to normalize the satellite images obtained by radar remote sensing. The backscatter of waves results in gradual decrease of brightness along the nadir, from near range to far range, and to minimize the effects of the backscatter the images was be normalized to a reference angle, and thereby producing in higher quality image with easier object detection in them. We implemented the incidence angle normalization using an inverse profile to normalize the image. The inverse profile is simply an image in which the direction of progressive decrease of brightness is reversed. The inverse profile is created in a way that on merging with the input image, it results in an image with normalized backscatter. The normalized image can be used to monitor the activities in the ocean, like oil spill, currents, eddies, etc. or can be used to improve the quality of raw data for further research on SAR images and detect various oceanographic activities.

    Python
    Image Processing
    Satellite Images
    Big Data
    Machine Learning
    Java Swing
    Research


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/inp1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/inv.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/out1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    (a) Original image; (b) Inverse profile generated of the original image; (c) Normalized image
</div>

In order to assess the performance of the algorithm, various metrics were used. They gave mathematical proof of the efficiency of the normalization. The value obtained by running metrics on the output images not only demonstrated the magnitude of normalization, but provided us quantitative results, as an evidence to the quality of our results. Also, Built Java GUI and integrated four other Satellite images  processing projects, for interactive user experience.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/normalization.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Architecture
</div>
