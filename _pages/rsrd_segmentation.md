---
permalink: /rsrd_segmentation/
title:  "RSRD-segmentation"
categories: jekyll update
---
<br>

## RSRD-segmentation dataset
From RSRD, we pick out 63 point cloud samples with irregular unevenness such as bump/pothole. In the *pcd* files, the points belonging to bump/potholes are labeled as **1** (see the red points below). RGB values are also attached for points within image's perspective. This prototype dataset can be used for bump/pothole segmentation.

<figure class='align-center' style="width: 80%;">
  <a href="/assets/images/rsrd_seg.png">
  <img src="/assets/images/rsrd_seg.png" alt=""></a>
  <figcaption>Point clouds with irregular road unevenness annotations.</figcaption>
</figure>

As only road areas where tires pass will cause vehicle response, we further crop the complete road area into patches for the convenience of practical applications. There are **710** road point cloud patches in this prototype dataset. 

<figure class='align-center' style="width: 80%;">
  <a href="/assets/images/rsrd_seg_patch.jpg">
  <img src="/assets/images/rsrd_seg_patch.jpg" alt=""></a>
  <figcaption>Cropped point cloud patches. The length and width are about 6m, and 35cm respectively.</figcaption>
</figure>

## Baseline
Please refer to our [paper](https://ieeexplore.ieee.org/document/10329453) for more details.


