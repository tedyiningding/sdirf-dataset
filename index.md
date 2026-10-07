---
layout: default
# title: Dataset
---
<style>
.wrapper { max-width: 1200px; padding-left: 24px; padding-right: 24px; }
</style>

<h1 style="text-align: center;">SDIRF Dataset</h1>

<div style="text-align:center;">
  <img src="https://github.com/SenseRoboticsLab/estimating-fog-parameters/blob/main/assets/thick_1.gif?raw=true" alt="" style="margin: 6px;">
  <img src="https://github.com/SenseRoboticsLab/estimating-fog-parameters/blob/main/assets/thin_1.gif?raw=true" alt="" style="margin: 6px;">
  <img src="https://github.com/SenseRoboticsLab/estimating-fog-parameters/blob/main/assets/thick_2.gif?raw=true" alt="" style="margin: 6px;">
  <img src="https://github.com/SenseRoboticsLab/estimating-fog-parameters/blob/main/assets/thin_2.gif?raw=true" alt="" style="margin: 6px;">
</div>

<div style="text-align:center;">
  <a href="https://ieeexplore.ieee.org/document/11218959">
    <img alt="IEEEXplore Paper" src="https://img.shields.io/badge/IEEE_Xplore-Paper-blue">
  </a>
  <a href="https://ieeexplore.ieee.org/document/11218959/media#media">
    <img alt="IEEEXplore Supplementary Material" src="https://img.shields.io/badge/IEEE_Xplore-Supplementary_Material-blue">
  </a>
  <a href="https://arxiv.org/abs/2511.20865">
    <img alt="arXiv Paper" src="https://img.shields.io/badge/arXiv-Paper-red">
  </a>
  <a href="https://github.com/SenseRoboticsLab/estimating-fog-parameters">
    <img alt="GitHub Repo" src="https://img.shields.io/badge/GitHub-Repo-black">
  </a>
  <a href="">
    <img alt="Pure Data" src="https://img.shields.io/badge/Pure-Data-silver">
  </a>
</div>

<div style="margin-top: 24px;"></div>

To-dos:
- [ ] Add Pure link where the dataset can be donwloaded from: the index page and the download subpage

---

We present the **S**tereo **D**riving **I**n **R**eal **F**og (SDIRF) dataset, which we created to address the gap in autonomous driving research that most existing datasets place limited emphasis on foggy scenarios.

SDIRF
- consists of high-quality, consecutive stereo frames of real, foggy road scenes under a variety of visibility conditions, totalling over 40 minutes and 34,000 frames;
- contains the camera's photometric parameters calibrated in a lab environment (a first-of-its-kind), which is a prerequisite for correctly applying the atmospheric scattering model to foggy images;
- includes the counterpart clear data of the same routes recorded in overcast weather, which is useful for companion work in image defogging and depth reconstruction.

<!-- Please visit the [Download]({{ site.baseurl }}/download/) page. -->

By making SDIRF publicly available, we hope to help advance the research on visual perception in fog.

# Estimating fog parameters from a sequence of stereo images

<!-- ![Overview](https://github.com/SenseRoboticsLab/estimating-fog-parameters/blob/main/assets/method.png?raw=true) -->

We also propose a method for estimating and dynamically updating the parameters of the atmospheric scattering model from a sequence of stereo foggy images.

Our algorithm 
- simultaneously estimates all the parameters by solving a novel optimisation problem, in contrast with previous approaches that estimate the parameters sequentially and thus are prone to error propagation 
- effectively handles real-world fog, which is often globally inhomogeneous, by assuming that fog is only locally homogeneous
- can be easily used as an add-on module in existing visual SLAM or odometry systems in the presence of fog

Extensive experiments we conducted using both synthetic foggy data and real foggy sequences from SDIRF demonstrate the superiority of the proposed algorithm over prior methods.

# Citation
Our work was accepted by *IEEE Transactions on Pattern Analysis and Machine Intelligence* in October 2025.

Please consider citing it if you find either the SDIRF dataset or our fog parameter estimation method useful for your research.
<div class="citation-box">
  <pre><code>@article{ding2025estimating,
  author={Ding, Yining and Mota, João F. C. and Wallace, Andrew M. and Wang, Sen},
  journal={IEEE Transactions on Pattern Analysis and Machine Intelligence}, 
  title={Estimating Fog Parameters From a Sequence of Stereo Images}, 
  year={2026},
  volume={48},
  number={3},
  pages={2154-2169},
  keywords={Atmospheric modeling;Parameter estimation;Scattering;Cameras;Estimation;Autonomous vehicles;Visualization;Accuracy;Visual perception;Synthetic data;Fog parameter estimation;atmospheric scattering model;foggy dataset;photometric calibration;vehicular perception;image defogging;depth reconstruction},
  doi={10.1109/TPAMI.2025.3626275}
}</code></pre>
</div>

# License
This project is released under the [GPL-3.0 License]({{ site.baseurl }}/LICENSE).
