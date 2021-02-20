---
layout: page
title: Political Memes
description: A fun project to explore to compare memes from three political subreddits 
img: https://i.redd.it/x1cmqf7gmfb41.jpg
importance: 7
bitbucket: https://bitbucket.org/nomem/politicalmemes/
tags: [python]
---

I analyze three political subreddits --- <a href="https://www.reddit.com/r/ChapoTrapHouse/" target="_blank">r/chapotraphouse</a>, <a href="https://www.reddit.com/r/neoliberal/" target="_blank">r/neoliberal</a>, <a href="https://www.reddit.com/r/the_donald/" target="_blank">r/the_donald</a> --- on the month of february'2020, during US election primaries. Using <a href="https://bigquery.cloud.google.com/dataset/fh-bigquery:reddit_comments" target="_blank">BigQuery Reddit Dataset</a>, I have collected the image URLs which were later downloaded. Below, we show example images. Using <a href="https://cloud.google.com/vision/docs/ocr" target="_blank">Google Cloud Vision API</a>, I converted the memes to text which were later analyzed using spacy.



<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'https://i.redd.it/5yq06gs0avb41.jpg' }}" alt="" title="example image from from chapotraphouse"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'https://i.redd.it/rb3lamt01ej41.jpg' }}" alt="" title="example image from neoliberal"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ 'https://i.redd.it/x1cmqf7gmfb41.jpg' }}" alt="" title="example image from the_donald"/>
    </div>
</div>
<div class="caption">
    Example meme images from this dataset -- chapotraphouse (left), neoliberal (center) and the_donald (right).
</div>
