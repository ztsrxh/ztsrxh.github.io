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

## Codes for reading data
```bash
import open3d as o3d
import numpy as np

pcd = o3d.t.io.read_point_cloud('XXX.pcd')
xyz = pcd.point.positions.numpy()
labels = pcd.point.label.numpy().reshape(-1).astype(np.int8)
# RGB information
b = pcd.point.b.numpy()/255.0
r = pcd.point.r.numpy()/255.0
g = pcd.point.g.numpy()/255.0
```

## Citation

```bibtex
@ARTICLE{10329453,
  author={Zhao, Tong and Guo, Peilin and He, Junxiang and Wei, Yintao},
  journal={IEEE Transactions on Intelligent Vehicles}, 
  title={A Hierarchical Scheme of Road Unevenness Perception With LiDAR for Autonomous Driving Comfort}, 
  year={2024},
  volume={9},
  number={1},
  pages={2439-2448},
  doi={10.1109/TIV.2023.3337236}}
```