---
layout: page
title: Google Landmark Recognition Challenge
description: A project to compete in kaggle Google Landmark Recognition Challenge
img: /assets/img/sample_glrc.png
importance: 5
bitbucket: https://bitbucket.org/nomem/cs5525-google_landmark_recognition_challenge/
tags: [python]
---

In this class project, I compared four machine learning models --- VGG, Resnet-50 (trained only last layer), Inception-V4, Resnet-50 (trained the whole model) --- on Google Landmark Recognition Challenge. Result-wise, Resnet-50 (trained the whole model) recieved a standing of 129 on <a href="https://www.kaggle.com/c/landmark-recognition-challenge/leaderboard" target="_blank"> Kaggle</a>. I used a Google Cloud Compute machine with a K80 GPU for this project.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/sample_glrc.png' | relative_url }}" alt="" title="google landmark dataset example image"/>
    </div>
</div>
<div class="caption">
    Example image from this dataset. 
</div>

From my analysis, we see several interesting results. Training time-wise, resnet-50 (training only the last layer) had the least average time. However, resnet-50 where the whole model was trained outperformed everyone else in other aspects.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/glrc_result.png' | relative_url }}" alt="" title="model comparison"/>
    </div>
</div>
<div class="caption">
    Results from comparing the four models. 
</div>