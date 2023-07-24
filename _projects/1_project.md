---
layout: page
title: RADAR-based Moving Object Segmentation
description: 
img: assets/img/mine/radar_results.png
importance: 1
category: work
---

Recognizing the static and dynamic elements in its surroundings is a crucial undertaking for an autonomous vehicle. Within the realm of Computer Vision, proficiently identifying moving objects within a scene assumes a momentous role. 
This capability greatly contributes to various downstream applications, such as path planning, collision avoidance, scene flow estimation, and predicting future states of agents within the environment.


Despite possessing unique and valuable attributes, the RADAR sensor remains relatively underutilized in this field. It offers distinct advantages that other aforementioned sensors lack, including exceptional reliability in challenging weather conditions such as fog, rain, or snow, and a comparatively cost-effective nature. One noteworthy capability of RADARs is their ability to directly measure the radial velocity of objects within the field of view using the Doppler effect, making them a crucial and promising candidate for addressing this specific task.

In this work, we developed a Transformer based architecture to process the sequence of RADAR scans to segment the moving points.

The diagram below gives the Qualitative analysis of our approach.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/mine/radar_results.png" title="Qualitative Results" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Qualitative results of our approach. A) are the raw scans, B) is the MOS prediction of our model, where green denotes the moving
objects and gray is static, C) shows the ground truth labels.
</div>

