---
permalink: /rscd/
title:  "RSCD"
categories: jekyll update
header:
  image: /assets/images/RSCD-head.jpg
layout: splash
---
<br>

## Works based on RSCD
-   Oct./2024  Mohammad Otoofi used RSCD for aiding segmentation and friction estimation in *[FrictionSegNet](https://ieeexplore.ieee.org/abstract/document/10705359)*.
-   Aug./2024  Binglin Li proposed *[Improved MobileNet V3](https://www.mdpi.com/1424-8220/24/17/5613)* for road adhesion identification.
-   July/2024  Ioannis V. Vondikakis proposed *[FedRSC](https://ieeexplore.ieee.org/document/10606293)*, inspiring wider applications in intelligent transportation systems.
-   May/2024  T. Ahmed proposed *[EdgeFusionViT](https://ieeexplore.ieee.org/abstract/document/10510402)*.
-   Jan./2024  We proposed a method to [infer friction coefficient](https://doi.org/10.1016/j.ymssp.2023.111019) with RSCD.
-   Sep./2023  Y.H. Guo proposed *[Attention-ReXNet](https://ieeexplore.ieee.org/abstract/document/10256482)* based on RSCD.
-   Sep./2023  J. Wilson used RSCD in his [Master's thesis](https://ecommons.cornell.edu/items/08ae9478-d8f2-4440-8242-19de382464e0) in Cornell Univ.
-   Aug./2023  We first proposed the baseline [classification model](https://ieeexplore.ieee.org/abstract/document/10101715).

# Road Surface Classification Dataset

The prior knowledge of road surface states is essential for improving the safety and ride comfort of autonomous vehicles. Previewing road conditions with vision sensor is verified to be an effective solution. We release this **R**oad **S**urface **C**lassification **D**ataset (RSCD), which is the first dataset in this field containing 1 million image samples with detailed road `material`, `friction` and `unevenness` level annotations.


## Data Acquisition
<p style="text-align: justify;">
Original pictures are captured with a 2M monocular camera. To ensure high resolution of road surface area, the camera is mounted on bonnet with a certain pitch angle.
We acquire real-world data under as diverse working conditions as possible. Experiments lasted from January to July, 2022 in Beijing and covered about 700 kilometers of roads. The generalization capability of models to be developed is enlarged at the dataset level.
</p>

<p style="text-align: justify;">
Considering the fact that only the road area that tires pass would affect vehicle response, we crop the road surface area of the original pictures into patches of size 360*240px. The patches are labeled manually according to the class definition below.
</p>

<figure class="align-center" style="width: 40%; margin-top: 0;">
  <a href="/assets/images/crop.jpg">
  <img src="/assets/images/crop.jpg" alt=""></a>
  <figcaption>Patches are cropped from the complete scene.</figcaption>
</figure>

## Class Definition
<figure class="align-right" style="width: 40%; margin-top: 0;">
  <a href="/assets/images/class.png">
  <img src="/assets/images/class.png" alt=""></a>
  <figcaption>Road properties and the subclasses.</figcaption>
</figure>

The `friction` level, `material`, and `unevenness` properties of roads are essential for chassis control and driving assistance.

-   The friction level property contains six subclasses corresponding to different weather conditions, i.e. `dry`, `wet`, `water`, `fresh snow`, `melted snow`, and `ice`.
-   The road material property consists of `asphalt`, `concrete`, `dirt/mud`, and `gravel`.
-   The road unevenness is divided into `smooth`, `slight` unevenness, and `severe` unevenness according to the amplitude of the road undulation.

The subclasses of the three road properties are combined to form the class definition of the dataset. But we donot demonstrate that it must be modeled as a single-label classification. Finally, we get **27** combined classes. Also, researchers can use part of the labeled properties to develop their own applications.
**Note** that the road material and unevenness are not annotated when the friction levels are `fresh snow`, `melted snow`, or `ice`. Also, the unevenness is not labeled for `dirt/mud` or `gravel` roads.


## Samples and Statistics
<figure class="align-right" style="width: 40%; margin-top: 0;">
  <a href="/assets/images/classification_sample.jpeg">
  <img src="/assets/images/classification_sample.jpeg" alt=""></a>
  <figcaption>Sample images of part of the classes. (a). dry-asphalt-smooth (b). dry-asphalt-slight (c). dry-asphalt-severe (d). water-asphalt-severe (e) wet-asphalt-slight (f). wet-concrete-smooth (g). wet-concrete-severe (h). water-concrete-slight (i). water-mud (j). dry-gravel (k). melted snow (l). ice.</figcaption>
</figure>

The dataset is divided into train-set(~**960k** samples), validation-set(~**20k** samples), test-set(~**50k** samples). The images belonging to the same class are in the same directory in the train set. The test and validation datasets are randomly sampled and approximately obeys independent identical distribution with the train set. We also provide the true labels for the test set.

Note： Since the experiments under rainy days are hard to conduct & label and also, the severely damaged roads are deficient, there is an inter-class imbalance problem of this dataset. The count of samples for these classes in the validation and test set are also less than others. We are concentrating on solving this problem, and the data collection for these classes are still ongoing.

<figure class='align-center' style="width: 80%;">
  <a href="/assets/images/counts-RSCD.jpeg">
  <img src="/assets/images/counts-RSCD.jpeg" alt=""></a>
  <figcaption>Number of images for each class.</figcaption>
</figure>

## Demo Video for road classification
[<img src="https://img.youtube.com/vi/kp6mNrUpJEo/hqdefault.jpg" width="600" height="450"/>](https://www.youtube.com/embed/kp6mNrUpJEo)

## Demo Video for road friction estimation
[<img src="https://img.youtube.com/vi/XYsDKpCLgVs/hqdefault.jpg" width="600" height="450"/>](https://www.youtube.com/embed/XYsDKpCLgVs)


## Citation
```bibtex
@ARTICLE{10101715,
  author={Zhao, Tong and He, Junxiang and Lv, Jingcheng and Min, Delei and Wei, Yintao},
  journal={IEEE Transactions on Intelligent Transportation Systems}, 
  title={A Comprehensive Implementation of Road Surface Classification for Vehicle Driving Assistance: Dataset, Models, and Deployment}, 
  year={2023},
  volume={24},
  number={8},
  pages={8361-8370},
  doi={10.1109/TITS.2023.3264588}}
```
```bibtex
@article{ZHAO2024111019,
title = {Road friction estimation based on vision for safe autonomous driving},
journal = {Mechanical Systems and Signal Processing},
volume = {208},
pages = {111019},
year = {2024},
doi = {https://doi.org/10.1016/j.ymssp.2023.111019},
author = {Tong Zhao and Peilin Guo and Yintao Wei}}
```




