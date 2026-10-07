---
layout: default  # Or another layout if you have one
title: Data Anonymisation
permalink: /data_anonymisation/ 
---
<style>
.wrapper { max-width: 1200px; padding-left: 24px; padding-right: 24px; }
</style>

To comply with the UK General Data Protection Regulation (UK GDPR), we publish only images in which personally identifiable information (PII) has been removed. Specifically, we blur **human faces** and **vehicle licence plates** while preserving the remaining scene content. This approach minimises the impact of anonymisation on the visual information in the images and maximises the reproducibility of the experimental results reported in Section V-E of our [paper](https://ieeexplore.ieee.org/document/11218959).

The anonymisation process consists of the following steps:

1. Apply the [YOLOv11 model](https://docs.ultralytics.com/models/yolo11/) with pre-trained weights to detect [human faces](https://github.com/YapaLab/yolo-face) and [vehicle licence plates](https://huggingface.co/morsetechlab/yolov11-license-plate-detection).
2. Import and visualise the detection results in [CVAT](https://www.cvat.ai/) for inspection and manually refine the detected regions where necessary.
3. Apply blurring to the refined face and licence plate regions.
