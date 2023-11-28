---
permalink: /
title:  "Home"
categories: jekyll update
header:
  image: /assets/images/home-head.jpg
---


<div align='center'>
    <span style="font-family: Georgia, serif; font-size: 50px">Are current autonomous vehicles really safe and comfort? </span>
</div>
<div align='center'>
    <span  style="font-family: Georgia, serif; font-size: 50px">No! Their feet and legs are in the air. </span>
</div>
<br>


## What RSXD?
<p style="text-align: justify;">
The current perception research for autonomous driving (AD) mainly concentrates on the traffic environment understanding, such as obstacle
detection & tracking, lane & drivable area detection,  traffic light & sign recognition, and motion prediction. These perception pipelines contributes to realize motion control.
In high-speed and harsh driving environments, the dynamics characteristics of tire-road interactions is still the last security moat. 
Road is the only component in the physical world that vehicles have contact with. However, we know little about the road itself. 
Vehicle's feet and legs float in the air.
</p>

To fill this gap, we build and release **RSXD**, consisting of **R**oad **S**urface **C**lassification **D**ataset 
and **R**oad **S**urface **R**econstruction **D**ataset. 

<p style="text-align: justify;">
With the two datasets, we can obtain a comprehensive understanding of road conditions, especially the most important friction and unevenness. 
Road condition preview contributes to both the advanced driving assistance systems and L4+ AD vehicles. The accuracy and performance of trajectory planning and tracking/control systems will be greatly enhanced. 
Meanwhile, the road condition information can also be utilized in applications such as road health monitoring and accident prevention. 
</p>

## Why RSXD?
<p style="text-align: justify;">
The existing datasets for AD perception (e.g. KITTI, Argoverse, and nuScenes) captures the whole surrounding scene, leaving a small area for road surface. 
The resolution and definition of road surface in the images are poor; the accuracy and density of road surface in the point clouds are low.
Most significantly, they offer no detailed ground-truth information about road surface conditions.
</p>

Our **RSXD** is the first dataset specifically for road surface perception.The **RSCD** is an image dataset for classifying road conditions, providing
detailed road friction, material, and unevenness level annotations. The **RSRD** is a multi-modal dataset for road reconstruction, providing recitfied stereo images, stereo disparity, depth, point cloud, and location/pose labels. 

## How RSXD?
For practical engineering applications, we make great efforts in expanding the dataset diversity and promoting label accuracy. We conduct experiments in various weather/seasons, urban/rural areas, 
and roads with different material, service age, and traffic flow. The **RSCD** contains **1million** image samples of **360*240px** size, covering about **700km** roads. The **RSRD** contains **2800** pairs with dense labels, and **13K** pairs with sparse labels.

<p style="text-align: justify;">
All the data is processed by initial annotation and further quality inspection. The accuracy requirement and decision boundary are strictly defined, thus minimizing the subjective bias and label noise.
</p>


## Usage and Citations
The RSXD (including RSCD and RSRD) is licensed under the permissive CC BY-NC. The datasets are released based on the resources of Tsinghua University, who possesses the complete copy right.

The RSXD is only open to academic research, not for any commercial use. If your works use the dataset, please cite the following papers.<br>

RSCD:
  - T. Zhao, et.al. <a href="https://ieeexplore.ieee.org/abstract/document/10101715">"A Comprehensive Implementation of Road Surface Classification for Vehicle Driving Assistance: Dataset, Models, and Deployment". </a> *IEEE Transactions on Intelligent Transportation Systems*, 2023.<br>
  - T. Zhao, et al. <a href="https://doi.org/10.1016/j.dib.2022.108483"> "A road surface image dataset with detailed annotations for driving assistance applications". </a> *Data in Brief*, 2022.<br>

---
RSRD:
  - T. Zhao, et al. <a href="https://arxiv.org/abs/2310.02262"> "RSRD: A Road Surface Reconstruction Dataset and Benchmark for Safe and Comfortable Autonomous Driving". </a> *arXiv:2310.02262*, 2023.<br>

---
RSRD-segmentation:
  - T. Zhao, et.al. <a href="https://ieeexplore.ieee.org/document/10329453"> "A Hierarchical Scheme of Road Unevenness Perception with LiDAR for Autonomous Driving Comfort". </a> *IEEE Transactions on Intelligent Vehicles*, 2022. <br>
