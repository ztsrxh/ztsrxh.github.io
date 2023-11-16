---
permalink: /rsrd_segmentation/
title:  "RSRD-segmentation"
categories: jekyll update
---
<br>

## RSRD-segmentation dataset
From RSRD, we pick out 63 point cloud samples with irregular unevenness such as bump/pothole. In the *pcd* files, the points belonging to bump/potholes are labeled as **1** (see the red points below), while **0** (the black points below) for the others. RGB values are also attached for every point. This prototype dataset can be used for bump/pothole segmentation.

<figure class='align-center' style="width: 80%;">
  <a href="/assets/images/rsrd_seg.png">
  <img src="/assets/images/rsrd_seg.png" alt=""></a>
  <figcaption>Point clouds with irregular road unevenness annotations.</figcaption>
</figure>

<figure class='align-center' style="width: 80%;">
  <a href="/assets/images/rsrd_seg_patch.jpg">
  <img src="/assets/images/rsrd_seg_patch.jpg" alt=""></a>
  <figcaption>Cropped point cloud patches. The length and width are about 6m, and 35cm respectively.</figcaption>
</figure>


