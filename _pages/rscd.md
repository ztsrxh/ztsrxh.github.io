---
permalink: /rscd/
title:  "RSCD"
categories: jekyll update
header:
  image: /assets/images/RSCD-head.jpg
layout: splash
---
<br>

# Road Surface Classification Dataset

The knowledge of the road surface states is essential for improving the safety and the ride comfort of autonomous vehicles. Previewing the road conditions with vision sensor is verified to be an effective solution. However, there is still a lack of a large-scale road surface image dataset. 
Therefore, we publish this **R**oad **S**urface **C**lassification **D**ataset (RSCD) containing 1 million image samples with detailed road `material`, `friction` and `unevenness` level annotations.


## Data Acquisition
<p style="text-align: justify;">
The original pictures are captured with the monocular camera. To ensure a high resolution of the road surface area, the camera is mounted on the bonnet and have a certain angle. The pictures are collected and stored with the acquisition platform.
Aiming at developing practical driving assistance applications, we conducted real-vehicle image acquisition under as many working conditions as possible. The generalization capability of the classification algorithm to be developed is enlarged at the dataset level. The experiments lasted from January to July, 2022 in Beijing and covered about 700 kilometers of roads.
</p>

<p style="text-align: justify;">
Considering the fact that only the road area that the tires pass would affect the vehicle response, we crop the road surface area of the original pictures into patches of size 360*240px. The patches are labeled manually according to the class definition below.
</p>

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

## Baseline
Please refer to our [paper](/#Usage and Citations) for more details.





