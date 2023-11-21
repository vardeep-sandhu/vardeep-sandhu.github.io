---
layout: page
title: RADAR-based Moving Object Segmentation
description: 
img: assets/img/mine/radar_results.png
importance: 1
category: work
---
In this project, we were focusing on the problem of Moving Object Segmentation using RADAR sensor. Effectively solving MOS can assist in several downstream applications, such as path planning, collision avoidance, scene flow estimation, and predicting future states of agents within the environment.

Researchers in the past have explored this task with cameras and LiDAR sensors. Surprisingly, the RADAR sensor hasn't been widely used in this area, despite having distinctive and valuable features that the mentioned sensors lack. For instance, RADAR is reliable in challenging weather conditions like fog, rain, or snow, and it is comparatively cost-effective. Additionally, RADARs can naturally measure the radial velocity of objects in the field of view using the Doppler effect, making them a crucial choice for solving this task.

In this work, we use sequential RADAR scans to accomplish the task of moving object segmentation. We have proposed a feature encoding module that utilizes a sequence of N past scans and combines the feature information with the current scan using the attention mechanism to generate more informative features. These features are then passed to the adapted Stratified Transformer network to produce the segmentation results.

We utilize RadarScenes dataset to train and validate our proposed approach. The diagram below shows the Qualitative Analysis of our approach on the RadarScenes testset. It can be seen that the model is able to predict the moving points from the scene quite well.

Furthermore, we saw a improvement from the previous baseline by ~12 absolute percentage points of the IoU of the moving class. 

<div class="row justify-content-sm-center">
    <div class="col-sm-20 mt-5 mt-md-0">
        {% include figure.html path="assets/img/mine/radar_results.png" title="Qualitative Results" class="img-fluid rounded z-depth-1" style="width: 100%; height: auto;" %}
    </div>
</div>
<div class="caption">
    Qualitative results of our approach. A) are the raw scans, B) is the MOS prediction of our model, where green denotes the moving
    objects and gray is static, C) shows the ground truth labels.
</div>

<p><span style="color: red;">Note: This project was developed with CARIAD SE.</span></p>
